# ipfs command reference

generated on 2016-05-30 12:23:24.847868

- [ipfs](#ipfs)
- [ipfs add](#ipfs-add)
- [ipfs bitswap](#ipfs-bitswap)
- [ipfs bitswap stat](#ipfs-bitswap-stat)
- [ipfs bitswap unwant](#ipfs-bitswap-unwant)
- [ipfs bitswap wantlist](#ipfs-bitswap-wantlist)
- [ipfs block](#ipfs-block)
- [ipfs block get](#ipfs-block-get)
- [ipfs block put](#ipfs-block-put)
- [ipfs block stat](#ipfs-block-stat)
- [ipfs bootstrap](#ipfs-bootstrap)
- [ipfs bootstrap add](#ipfs-bootstrap-add)
- [ipfs bootstrap list](#ipfs-bootstrap-list)
- [ipfs bootstrap rm](#ipfs-bootstrap-rm)
- [ipfs cat](#ipfs-cat)
- [ipfs commands](#ipfs-commands)
- [ipfs config](#ipfs-config)
- [ipfs config edit](#ipfs-config-edit)
- [ipfs config replace](#ipfs-config-replace)
- [ipfs config show](#ipfs-config-show)
- [ipfs daemon](#ipfs-daemon)
- [ipfs dht](#ipfs-dht)
- [ipfs dht findpeer](#ipfs-dht-findpeer)
- [ipfs dht findprovs](#ipfs-dht-findprovs)
- [ipfs dht get](#ipfs-dht-get)
- [ipfs dht put](#ipfs-dht-put)
- [ipfs dht query](#ipfs-dht-query)
- [ipfs diag](#ipfs-diag)
- [ipfs diag cmds](#ipfs-diag-cmds)
- [ipfs diag cmds clear](#ipfs-diag-cmds-clear)
- [ipfs diag cmds set-time](#ipfs-diag-cmds-set-time)
- [ipfs diag net](#ipfs-diag-net)
- [ipfs diag sys](#ipfs-diag-sys)
- [ipfs dns](#ipfs-dns)
- [ipfs file](#ipfs-file)
- [ipfs file ls](#ipfs-file-ls)
- [ipfs files](#ipfs-files)
- [ipfs files cp](#ipfs-files-cp)
- [ipfs files flush](#ipfs-files-flush)
- [ipfs files ls](#ipfs-files-ls)
- [ipfs files mkdir](#ipfs-files-mkdir)
- [ipfs files mv](#ipfs-files-mv)
- [ipfs files read](#ipfs-files-read)
- [ipfs files rm](#ipfs-files-rm)
- [ipfs files stat](#ipfs-files-stat)
- [ipfs files write](#ipfs-files-write)
- [ipfs get](#ipfs-get)
- [ipfs id](#ipfs-id)
- [ipfs init](#ipfs-init)
- [ipfs log](#ipfs-log)
- [ipfs log level](#ipfs-log-level)
- [ipfs log ls](#ipfs-log-ls)
- [ipfs log tail](#ipfs-log-tail)
- [ipfs ls](#ipfs-ls)
- [ipfs mount](#ipfs-mount)
- [ipfs name](#ipfs-name)
- [ipfs name publish](#ipfs-name-publish)
- [ipfs name resolve](#ipfs-name-resolve)
- [ipfs object](#ipfs-object)
- [ipfs object data](#ipfs-object-data)
- [ipfs object diff](#ipfs-object-diff)
- [ipfs object get](#ipfs-object-get)
- [ipfs object links](#ipfs-object-links)
- [ipfs object new](#ipfs-object-new)
- [ipfs object patch](#ipfs-object-patch)
- [ipfs object patch add-link](#ipfs-object-patch-add-link)
- [ipfs object patch append-data](#ipfs-object-patch-append-data)
- [ipfs object patch rm-link](#ipfs-object-patch-rm-link)
- [ipfs object patch set-data](#ipfs-object-patch-set-data)
- [ipfs object put](#ipfs-object-put)
- [ipfs object stat](#ipfs-object-stat)
- [ipfs pin](#ipfs-pin)
- [ipfs pin add](#ipfs-pin-add)
- [ipfs pin ls](#ipfs-pin-ls)
- [ipfs pin rm](#ipfs-pin-rm)
- [ipfs ping](#ipfs-ping)
- [ipfs refs](#ipfs-refs)
- [ipfs refs local](#ipfs-refs-local)
- [ipfs repo](#ipfs-repo)
- [ipfs repo fsck](#ipfs-repo-fsck)
- [ipfs repo gc](#ipfs-repo-gc)
- [ipfs repo stat](#ipfs-repo-stat)
- [ipfs resolve](#ipfs-resolve)
- [ipfs stats](#ipfs-stats)
- [ipfs stats bw](#ipfs-stats-bw)
- [ipfs swarm](#ipfs-swarm)
- [ipfs swarm addrs](#ipfs-swarm-addrs)
- [ipfs swarm addrs local](#ipfs-swarm-addrs-local)
- [ipfs swarm connect](#ipfs-swarm-connect)
- [ipfs swarm disconnect](#ipfs-swarm-disconnect)
- [ipfs swarm filters](#ipfs-swarm-filters)
- [ipfs swarm filters add](#ipfs-swarm-filters-add)
- [ipfs swarm filters rm](#ipfs-swarm-filters-rm)
- [ipfs swarm peers](#ipfs-swarm-peers)
- [ipfs tar](#ipfs-tar)
- [ipfs tar add](#ipfs-tar-add)
- [ipfs tar cat](#ipfs-tar-cat)
- [ipfs tour](#ipfs-tour)
- [ipfs tour list](#ipfs-tour-list)
- [ipfs tour next](#ipfs-tour-next)
- [ipfs tour restart](#ipfs-tour-restart)
- [ipfs update](#ipfs-update)
- [ipfs version](#ipfs-version)

## ipfs

```
USAGE
  ipfs - Global p2p merkle-dag filesystem.

SYNOPSIS

  ipfs [<flags>] <command> [<arg>] ...

OPTIONS

  -c,   --config string - Path to the configuration file to use.
  -D,   --debug  bool   - Operate in debug mode. Default: false.
  --help         bool   - Show the full command help text. Default: false.
  -h             bool   - Show a short version of the command help text. Default: false.
  -L,   --local  bool   - Run the command locally, instead of using the daemon. Default: false.
  --api          string - Use a specific API instance (defaults to /ip4/127.0.0.1/tcp/5001).

SUBCOMMANDS
  BASIC COMMANDS
    init          Initialize ipfs local configuration
    add <path>    Add a file to ipfs
    cat <ref>     Show ipfs object data
    get <ref>     Download ipfs objects
    ls <ref>      List links from an object
    refs <ref>    List hashes of links from an object
  
  DATA STRUCTURE COMMANDS
    block         Interact with raw blocks in the datastore
    object        Interact with raw dag nodes
    files         Interact with objects as if they were a unix filesystem
  
  ADVANCED COMMANDS
    daemon        Start a long-running daemon process
    mount         Mount an ipfs read-only mountpoint
    resolve       Resolve any type of name
    name          Publish or resolve IPNS names
    dns           Resolve DNS links
    pin           Pin objects to local storage
    repo          Manipulate the IPFS repository
  
  NETWORK COMMANDS
    id            Show info about ipfs peers
    bootstrap     Add or remove bootstrap peers
    swarm         Manage connections to the p2p network
    dht           Query the DHT for values or peers
    ping          Measure the latency of a connection
    diag          Print diagnostics
  
  TOOL COMMANDS
    config        Manage configuration
    version       Show ipfs version information
    update        Download and apply go-ipfs updates
    commands      List all available commands
  
  Use 'ipfs <command> --help' to learn more about each command.
  
  ipfs uses a repository in the local file system. By default, the repo is located
  at ~/.ipfs. To change the repo location, set the $IPFS_PATH environment variable:
  
    export IPFS_PATH=/path/to/ipfsrepo

  Use 'ipfs <subcmd> --help' for more information about each command.
```

## ipfs add

```
USAGE
  ipfs add <path>... - Add a file to ipfs.

ARGUMENTS

  <path>... - The path to a file to be added to IPFS.

OPTIONS

  -r,     --recursive           bool   - Add directory paths recursively.
  -q,     --quiet               bool   - Write minimal output. Default: false.
  --silent                      bool   - Write no output. Default: false.
  -p,     --progress            bool   - Stream progress data. Default: true.
  -t,     --trickle             bool   - Use trickle-dag format for dag generation. Default: false.
  -n,     --only-hash           bool   - Only chunk and hash - do not write to disk. Default: false.
  -w,     --wrap-with-directory bool   - Wrap files with a directory object. Default: false.
  -H,     --hidden              bool   - Include files that are hidden. Only takes effect on recursive add. Default: false.
  -s,     --chunker             string - Chunking algorithm to use.
  --pin                         bool   - Pin this object when adding. Default: true.

DESCRIPTION

  Adds contents of <path> to ipfs. Use -r to add directories.
  Note that directories are added recursively, to form the ipfs
  MerkleDAG.
  
  The wrap option, '-w', wraps the file (or files, if using the
  recursive option) in a directory. This directory contains only
  the files which have been added, and means that the file retains
  its filename. For example:
  
    > ipfs add example.jpg
    added QmbFMke1KXqnYyBBWxB74N4c5SBnJMVAiMNRcGu6x1AwQH example.jpg
    > ipfs add example.jpg -w
    added QmbFMke1KXqnYyBBWxB74N4c5SBnJMVAiMNRcGu6x1AwQH example.jpg
    added QmaG4FuMqEBnQNn3C8XJ5bpW8kLs7zq2ZXgHptJHbKDDVx
  
  You can now refer to the added file in a gateway, like so:
  
    /ipfs/QmaG4FuMqEBnQNn3C8XJ5bpW8kLs7zq2ZXgHptJHbKDDVx/example.jpg
```

## ipfs bitswap

```
USAGE
  ipfs bitswap - A set of commands to manipulate the bitswap agent.

SUBCOMMANDS
  ipfs bitswap unwant <key>... - Remove a given block from your wantlist.
  ipfs bitswap wantlist        - Show blocks currently on the wantlist.
  ipfs bitswap stat            - Show some diagnostic information on the bitswap agent.

  Use 'ipfs bitswap <subcmd> --help' for more information about each command.
```

## ipfs bitswap stat

```
USAGE
  ipfs bitswap stat - Show some diagnostic information on the bitswap agent.
```

## ipfs bitswap unwant

```
USAGE
  ipfs bitswap unwant <key>... - Remove a given block from your wantlist.

ARGUMENTS

  <key>... - Key(s) to remove from your wantlist.
```

## ipfs bitswap wantlist

```
USAGE
  ipfs bitswap wantlist - Show blocks currently on the wantlist.

OPTIONS

  -p, --peer string - Specify which peer to show wantlist for. Default: self.

DESCRIPTION

  Print out all blocks currently on the bitswap wantlist for the local peer.
```

## ipfs block

```
USAGE
  ipfs block - Manipulate raw IPFS blocks.

DESCRIPTION

  'ipfs block' is a plumbing command used to manipulate raw ipfs blocks.
  Reads from stdin or writes to stdout, and <key> is a base58 encoded
  multihash.

SUBCOMMANDS
  ipfs block put <data> - Stores input as an IPFS block.
  ipfs block stat <key> - Print information of a raw IPFS block.
  ipfs block get <key>  - Get a raw IPFS block.

  Use 'ipfs block <subcmd> --help' for more information about each command.
```

## ipfs block get

```
USAGE
  ipfs block get <key> - Get a raw IPFS block.

ARGUMENTS

  <key> - The base58 multihash of an existing block to get.

DESCRIPTION

  'ipfs block get' is a plumbing command for retrieving raw ipfs blocks.
  It outputs to stdout, and <key> is a base58 encoded multihash.
```

## ipfs block put

```
USAGE
  ipfs block put <data> - Stores input as an IPFS block.

ARGUMENTS

  <data> - The data to be stored as an IPFS block.

DESCRIPTION

  'ipfs block put' is a plumbing command for storing raw ipfs blocks.
  It reads from stdin, and <key> is a base58 encoded multihash.
```

## ipfs block stat

```
USAGE
  ipfs block stat <key> - Print information of a raw IPFS block.

ARGUMENTS

  <key> - The base58 multihash of an existing block to get.

DESCRIPTION

  'ipfs block stat' is a plumbing command for retrieving information
  on raw ipfs blocks. It outputs the following to stdout:
  
  	Key  - the base58 encoded multihash
  	Size - the size of the block in bytes
```

## ipfs bootstrap

```
USAGE
  ipfs bootstrap - Show or edit the list of bootstrap peers.

DESCRIPTION

  Running 'ipfs bootstrap' with no arguments will run 'ipfs bootstrap list'.
  
  SECURITY WARNING:
  
  The bootstrap command manipulates the "bootstrap list", which contains
  the addresses of bootstrap nodes. These are the *trusted peers* from
  which to learn about other peers in the network. Only edit this list
  if you understand the risks of adding or removing nodes from this list.

SUBCOMMANDS
  ipfs bootstrap rm [<peer>]...  - Removes peers from the bootstrap list.
  ipfs bootstrap list            - Show peers in the bootstrap list.
  ipfs bootstrap add [<peer>]... - Add peers to the bootstrap list.

  Use 'ipfs bootstrap <subcmd> --help' for more information about each command.
```

## ipfs bootstrap add

```
USAGE
  ipfs bootstrap add [<peer>]... - Add peers to the bootstrap list.

ARGUMENTS

  [<peer>]... - A peer to add to the bootstrap list (in the format '<multiaddr>/<peerID>')

OPTIONS

  --default bool - Add default bootstrap nodes. Default: false.

DESCRIPTION

  Outputs a list of peers that were added (that weren't already
  in the bootstrap list).
  
  SECURITY WARNING:
  
  The bootstrap command manipulates the "bootstrap list", which contains
  the addresses of bootstrap nodes. These are the *trusted peers* from
  which to learn about other peers in the network. Only edit this list
  if you understand the risks of adding or removing nodes from this list.
```

## ipfs bootstrap list

```
USAGE
  ipfs bootstrap list - Show peers in the bootstrap list.

DESCRIPTION

  Peers are output in the format '<multiaddr>/<peerID>'.
```

## ipfs bootstrap rm

```
USAGE
  ipfs bootstrap rm [<peer>]... - Removes peers from the bootstrap list.

ARGUMENTS

  [<peer>]... - A peer to add to the bootstrap list (in the format '<multiaddr>/<peerID>')

OPTIONS

  --all bool - Remove all bootstrap peers. Default: false.

DESCRIPTION

  Outputs the list of peers that were removed.
  
  SECURITY WARNING:
  
  The bootstrap command manipulates the "bootstrap list", which contains
  the addresses of bootstrap nodes. These are the *trusted peers* from
  which to learn about other peers in the network. Only edit this list
  if you understand the risks of adding or removing nodes from this list.
```

## ipfs cat

```
USAGE
  ipfs cat <ipfs-path>... - Show IPFS object data.

ARGUMENTS

  <ipfs-path>... - The path to the IPFS object(s) to be outputted.

DESCRIPTION

  Displays the data contained by an IPFS or IPNS object(s) at the given path.
```

## ipfs commands

```
USAGE
  ipfs commands - List all available commands.

OPTIONS

  -f, --flags bool - Show command flags. Default: false.

DESCRIPTION

  Lists all available commands (and subcommands) and exits.
```

## ipfs config

```
USAGE
  ipfs config <key> [<value>] - Get and set IPFS config values.

ARGUMENTS

  <key>     - The key of the config entry (e.g. "Addresses.API").
  [<value>] - The value to set the config entry to.

OPTIONS

  --bool bool - Set a boolean value. Default: false.
  --json bool - Parse stringified JSON. Default: false.

DESCRIPTION

  'ipfs config' controls configuration variables. It works
  much like 'git config'. The configuration values are stored in a config
  file inside your IPFS repository.
  
  Examples:
  
  Get the value of the 'datastore.path' key:
  
    $ ipfs config datastore.path
  
  Set the value of the 'datastore.path' key:
  
    $ ipfs config datastore.path ~/.ipfs/datastore

SUBCOMMANDS
  ipfs config replace <file> - Replaces the config with <file>.
  ipfs config show           - Outputs the content of the config file.
  ipfs config edit           - Opens the config file for editing in $EDITOR.

  Use 'ipfs config <subcmd> --help' for more information about each command.
```

## ipfs config edit

```
USAGE
  ipfs config edit - Opens the config file for editing in $EDITOR.

DESCRIPTION

  To use 'ipfs config edit', you must have the $EDITOR environment
  variable set to your preferred text editor.
```

## ipfs config replace

```
USAGE
  ipfs config replace <file> - Replaces the config with <file>.

ARGUMENTS

  <file> - The file to use as the new config.

DESCRIPTION

  Make sure to back up the config file first if neccessary, as this operation
  can't be undone.
```

## ipfs config show

```
USAGE
  ipfs config show - Outputs the content of the config file.

DESCRIPTION

  WARNING: Your private key is stored in the config file, and it will be
  included in the output of this command.
```

## ipfs daemon

```
USAGE
  ipfs daemon - Run a network-connected IPFS node.

OPTIONS

  --init                         bool   - Initialize IPFS with default settings if not already initialized. Default: false.
  --routing                      string - Overrides the routing option. Default: dht.
  --mount                        bool   - Mounts IPFS to the filesystem. Default: false.
  --writable                     bool   - Enable writing objects (with POST, PUT and DELETE). Default: false.
  --mount-ipfs                   string - Path to the mountpoint for IPFS (if using --mount). Defaults to config setting.
  --mount-ipns                   string - Path to the mountpoint for IPNS (if using --mount). Defaults to config setting.
  --unrestricted-api             bool   - Allow API access to unlisted hashes. Default: false.
  --disable-transport-encryption bool   - Disable transport encryption (for debugging protocols). Default: false.
  --enable-gc                    bool   - Enable automatic periodic repo garbage collection. Default: false.
  --manage-fdlimit               bool   - Check and raise file descriptor limits if needed. Default: false.

DESCRIPTION

  The daemon will start listening on ports on the network, which are
  documented in (and can be modified through) 'ipfs config Addresses'.
  For example, to change the 'Gateway' port:
  
      ipfs config Addresses.Gateway /ip4/127.0.0.1/tcp/8082
  
  The API address can be changed the same way:
  
     ipfs config Addresses.API /ip4/127.0.0.1/tcp/5002
  
  Make sure to restart the daemon after changing addresses.
  
  By default, the gateway is only accessible locally. To expose it to
  other computers in the network, use 0.0.0.0 as the ip address:
  
     ipfs config Addresses.Gateway /ip4/0.0.0.0/tcp/8080
  
  Be careful if you expose the API. It is a security risk, as anyone could
  control your node remotely. If you need to control the node remotely,
  make sure to protect the port as you would other services or database
  (firewall, authenticated proxy, etc).
  
  HTTP Headers
  
  IPFS supports passing arbitrary headers to the API and Gateway. You can
  do this by setting headers on the API.HTTPHeaders and Gateway.HTTPHeaders
  keys:
  
  	ipfs config --json API.HTTPHeaders.X-Special-Header '["so special :)"]'
  	ipfs config --json Gateway.HTTPHeaders.X-Special-Header '["so special :)"]'
  
  Note that the value of the keys is an _array_ of strings. This is because
  headers can have more than one value, and it is convenient to pass through
  to other libraries.
  
  CORS Headers (for API)
  
  You can setup CORS headers the same way:
  
  	ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin '["example.com"]'
  	ipfs config --json API.HTTPHeaders.Access-Control-Allow-Methods '["PUT", "GET", "POST"]'
  	ipfs config --json API.HTTPHeaders.Access-Control-Allow-Credentials '["true"]'
  
  Shutdown
  
  To shutdown the daemon, send a SIGINT signal to it (e.g. by pressing 'Ctrl-C')
  or send a SIGTERM signal to it (e.g. with 'kill'). It may take a while for the
  daemon to shutdown gracefully, but it can be killed forcibly by sending a
  second signal.
  
  IPFS_PATH environment variable
  
  ipfs uses a repository in the local file system. By default, the repo is located
  at ~/.ipfs. To change the repo location, set the $IPFS_PATH environment variable:
  
      export IPFS_PATH=/path/to/ipfsrepo
  
  DEPRECATION NOTICE
  
  Previously, IPFS used an environment variable as seen below:
  
     export API_ORIGIN="http://localhost:8888/"
  
  This is deprecated. It is still honored in this version, but will be removed in a
  future version, along with this notice. Please move to setting the HTTP Headers.
```

## ipfs dht

```
USAGE
  ipfs dht - Issue commands directly through the DHT.

SUBCOMMANDS
  ipfs dht query <peerID>...    - Find the closest Peer IDs to a given Peer ID by querying the DHT.
  ipfs dht findprovs <key>...   - Find peers in the DHT that can provide a specific value, given a key.
  ipfs dht findpeer <peerID>... - Query the DHT for all of the multiaddresses associated with a Peer ID.
  ipfs dht get <key>...         - Given a key, query the DHT for its best value.
  ipfs dht put <key> <value>    - Write a key/value pair to the DHT.

  Use 'ipfs dht <subcmd> --help' for more information about each command.
```

## ipfs dht findpeer

```
USAGE
  ipfs dht findpeer <peerID>... - Query the DHT for all of the multiaddresses associated with a Peer ID.

ARGUMENTS

  <peerID>... - The ID of the peer to search for.

OPTIONS

  -v, --verbose bool - Print extra information. Default: false.

DESCRIPTION

  Outputs a list of newline-delimited multiaddresses.
```

## ipfs dht findprovs

```
USAGE
  ipfs dht findprovs <key>... - Find peers in the DHT that can provide a specific value, given a key.

ARGUMENTS

  <key>... - The key to find providers for.

OPTIONS

  -v, --verbose bool - Print extra information. Default: false.

DESCRIPTION

  Outputs a list of newline-delimited provider Peer IDs.
```

## ipfs dht get

```
USAGE
  ipfs dht get <key>... - Given a key, query the DHT for its best value.

ARGUMENTS

  <key>... - The key to find a value for.

OPTIONS

  -v, --verbose bool - Print extra information. Default: false.

DESCRIPTION

  Outputs the best value for the given key.
  
  There may be several different values for a given key stored in the DHT; in this context 'best' means the record that is most desirable. There is no one metric for 'best': it depends entirely on the key type. For IPNS, 'best' is the record that is both valid and has the highest sequence number (freshest). Different key types can specify other 'best' rules.
```

## ipfs dht put

```
USAGE
  ipfs dht put <key> <value> - Write a key/value pair to the DHT.

ARGUMENTS

  <key>   - The key to store the value at.
  <value> - The value to store.

OPTIONS

  -v, --verbose bool - Print extra information. Default: false.

DESCRIPTION

  Given a key of the form /foo/bar and a value of any form, this will write that value to the DHT with that key.
  
  Keys have two parts: a keytype (foo) and the key name (bar). IPNS uses the /ipns keytype, and expects the key name to be a Peer ID. IPNS entries are specifically formatted (protocol buffer).
  
  You may only use keytypes that are supported in your ipfs binary: currently this is only /ipns. Unless you have a relatively deep understanding of the go-ipfs DHT internals, you likely want to be using 'ipfs name publish' instead of this.
  
  Value is arbitrary text. Standard input can be used to provide value.
  
  NOTE: A value may not exceed 2048 bytes.
```

## ipfs dht query

```
USAGE
  ipfs dht query <peerID>... - Find the closest Peer IDs to a given Peer ID by querying the DHT.

ARGUMENTS

  <peerID>... - The peerID to run the query against.

OPTIONS

  -v, --verbose bool - Print extra information. Default: false.

DESCRIPTION

  Outputs a list of newline-delimited Peer IDs.
```

## ipfs diag

```
USAGE
  ipfs diag - Generates diagnostic reports.

SUBCOMMANDS
  ipfs diag net  - Generates a network diagnostics report.
  ipfs diag sys  - Prints out system diagnostic information.
  ipfs diag cmds - List commands run on this ipfs node.

  Use 'ipfs diag <subcmd> --help' for more information about each command.
```

## ipfs diag cmds

```
USAGE
  ipfs diag cmds - List commands run on this ipfs node.

OPTIONS

  -v, --verbose bool - Print extra information. Default: false.

DESCRIPTION

  Lists running and recently run commands.

SUBCOMMANDS
  ipfs diag cmds clear           - Clear inactive requests from the log.
  ipfs diag cmds set-time <time> - Set how long to keep inactive requests in the log.

  Use 'ipfs diag cmds <subcmd> --help' for more information about each command.
```

## ipfs diag cmds clear

```
USAGE
  ipfs diag cmds clear - Clear inactive requests from the log.
```

## ipfs diag cmds set-time

```
USAGE
  ipfs diag cmds set-time <time> - Set how long to keep inactive requests in the log.

ARGUMENTS

  <time> - Time to keep inactive requests in log.
```

## ipfs diag net

```
USAGE
  ipfs diag net - Generates a network diagnostics report.

OPTIONS

  --vis string - Output format. One of: d3, dot, text. Default: text.

DESCRIPTION

  Sends out a message to each node in the network recursively
  requesting a listing of data about them including number of
  connected peers and latencies between them.
  
  The given timeout will be decremented 2s at every network hop, 
  ensuring peers try to return their diagnostics before the initiator's 
  timeout. If the timeout is too small, some peers may not be reached.
  30s and 60s are reasonable timeout values, though networks vary.
  The default timeout is 20 seconds.
  
  The 'vis' option may be used to change the output format.
  Three formats are supported:
   * text - Easy to read. Default.
   * d3 - json ready to be fed into d3view
   * dot - graphviz format
  
  The 'd3' format will output a json object ready to be consumed by
  the chord network viewer, available at the following hash:
  
      /ipfs/QmbesKpGyQGd5jtJFUGEB1ByPjNFpukhnKZDnkfxUiKn38
  
  To view your diag output, 'ipfs add' the d3 vis output, and
  open the following link:
  
  	http://gateway.ipfs.io/ipfs/QmbesKpGyQGd5jtJFUGEB1ByPjNFpukhnKZDnkfxUiKn38/chord#<your hash>
  
  The 'dot' format can be fed into graphviz and other programs
  that consume the dot format to generate graphs of the network.
```

## ipfs diag sys

```
USAGE
  ipfs diag sys - Prints out system diagnostic information.

DESCRIPTION

  Prints out information about your computer to aid in easier debugging.
```

## ipfs dns

```
USAGE
  ipfs dns <domain-name> - DNS link resolver.

ARGUMENTS

  <domain-name> - The domain-name name to resolve.

OPTIONS

  -r, --recursive bool - Resolve until the result is not a DNS link. Default: false.

DESCRIPTION

  Multihashes are hard to remember, but domain names are usually easy to
  remember.  To create memorable aliases for multihashes, DNS TXT
  records can point to other DNS links, IPFS objects, IPNS keys, etc.
  This command resolves those links to the referenced object.
  
  For example, with this DNS TXT record:
  
  	> dig +short TXT ipfs.io
  	dnslink=/ipfs/QmRzTuh2Lpuz7Gr39stNr6mTFdqAghsZec1JoUnfySUzcy
  
  The resolver will give:
  
  	> ipfs dns ipfs.io
  	/ipfs/QmRzTuh2Lpuz7Gr39stNr6mTFdqAghsZec1JoUnfySUzcy
  
  The resolver can recursively resolve:
  
  	> dig +short TXT recursive.ipfs.io
  	dnslink=/ipns/ipfs.io
  	> ipfs dns -r recursive.ipfs.io
  	/ipfs/QmRzTuh2Lpuz7Gr39stNr6mTFdqAghsZec1JoUnfySUzcy
```

## ipfs file

```
USAGE
  ipfs file - Interact with ipfs objects representing Unix filesystems.

SYNOPSIS

  ipfs file <command>

DESCRIPTION

  'ipfs file' provides a familiar interface to file systems represented
  by IPFS objects, which hides IPFS implementation details like layout
  objects (e.g. fanout and chunking).

SUBCOMMANDS
  ipfs file ls <ipfs-path>... - List directory contents for Unix filesystem objects.

  Use 'ipfs file <subcmd> --help' for more information about each command.
```

## ipfs file ls

```
USAGE
  ipfs file ls <ipfs-path>... - List directory contents for Unix filesystem objects.

SYNOPSIS

  ipfs file ls <path>

ARGUMENTS

  <ipfs-path>... - The path to the IPFS object(s) to list links from.

DESCRIPTION

  Displays the contents of an IPFS or IPNS object(s) at the given path.
  
  The JSON output contains size information. For files, the child size
  is the total size of the file contents. For directories, the child
  size is the IPFS link size.
  
  The path can be a prefixless ref; in this case, we assume it to be an
  /ipfs ref and not /ipns.
  
  Example:
  
      > ipfs file ls QmW2WQi7j6c7UgJTarActp7tDNikE4B2qXtFCfLPdsgaTQ
      cat.jpg
      > ipfs file ls /ipfs/QmW2WQi7j6c7UgJTarActp7tDNikE4B2qXtFCfLPdsgaTQ
      cat.jpg
```

## ipfs files

```
USAGE
  ipfs files - Manipulate unixfs files.

OPTIONS

  -f, --flush bool - Flush target and ancestors after write. Default: true.

DESCRIPTION

  Files is an API for manipulating IPFS objects as if they were a unix filesystem.
  
  NOTE:
  Most of the subcommands of 'ipfs files' accept the '--flush' flag. It defaults to
  true. Use caution when setting this flag to false. It will improve performance
  for large numbers of file operations, but it does so at the cost of consistency
  guarantees. If the daemon is unexpectedly killed before running 'ipfs files flush'
  on the files in question, then data may be lost. This also applies to running
  'ipfs repo gc' concurrently with '--flush=false' operations.

SUBCOMMANDS
  ipfs files read <path>         - Read a file in a given mfs.
  ipfs files mv <source> <dest>  - Move files.
  ipfs files mkdir <path>        - Make directories.
  ipfs files stat <path>         - Display file status.
  ipfs files write <path> <data> - Write to a mutable file in a given filesystem.
  ipfs files cp <source> <dest>  - Copy files into mfs.
  ipfs files ls [<path>]         - List directories.
  ipfs files rm <path>...        - Remove a file.
  ipfs files flush [<path>]      - Flush a given path's data to disk.

  Use 'ipfs files <subcmd> --help' for more information about each command.
```

## ipfs files cp

```
USAGE
  ipfs files cp <source> <dest> - Copy files into mfs.

ARGUMENTS

  <source> - Source object to copy.
  <dest>   - Destination to copy object to.
```

## ipfs files flush

```
USAGE
  ipfs files flush [<path>] - Flush a given path's data to disk.

ARGUMENTS

  [<path>] - Path to flush. Default: '/'.

DESCRIPTION

  Flush a given path to disk. This is only useful when other commands
  are run with the '--flush=false'.
```

## ipfs files ls

```
USAGE
  ipfs files ls [<path>] - List directories.

ARGUMENTS

  [<path>] - Path to show listing for. Defaults to '/'.

OPTIONS

  -l bool - Use long listing format.

DESCRIPTION

  List directories.
  
  Examples:
  
      $ ipfs files ls /welcome/docs/
      about
      contact
      help
      quick-start
      readme
      security-notes
  
      $ ipfs files ls /myfiles/a/b/c/d
      foo
      bar
```

## ipfs files mkdir

```
USAGE
  ipfs files mkdir <path> - Make directories.

ARGUMENTS

  <path> - Path to dir to make.

OPTIONS

  -p, --parents bool - No error if existing, make parent directories as needed.

DESCRIPTION

  Create the directory if it does not already exist.
  
  NOTE: All paths must be absolute.
  
  Examples:
  
      $ ipfs mfs mkdir /test/newdir
      $ ipfs mfs mkdir -p /test/does/not/exist/yet
```

## ipfs files mv

```
USAGE
  ipfs files mv <source> <dest> - Move files.

ARGUMENTS

  <source> - Source file to move.
  <dest>   - Destination path for file to be moved to.

DESCRIPTION

  Move files around. Just like traditional unix mv.
  
  Example:
  
      $ ipfs files mv /myfs/a/b/c /myfs/foo/newc
```

## ipfs files read

```
USAGE
  ipfs files read <path> - Read a file in a given mfs.

ARGUMENTS

  <path> - Path to file to be read.

OPTIONS

  -o, --offset int - Byte offset to begin reading from.
  -n, --count  int - Maximum number of bytes to read.

DESCRIPTION

  Read a specified number of bytes from a file at a given offset. By default, will
  read the entire file similar to unix cat.
  
  Examples:
  
      $ ipfs files read /test/hello
      hello
```

## ipfs files rm

```
USAGE
  ipfs files rm <path>... - Remove a file.

ARGUMENTS

  <path>... - File to remove.

OPTIONS

  -r, --recursive bool - Recursively remove directories.

DESCRIPTION

  Remove files or directories.
  
      $ ipfs files rm /foo
      $ ipfs files ls /bar
      cat
      dog
      fish
      $ ipfs files rm -r /bar
```

## ipfs files stat

```
USAGE
  ipfs files stat <path> - Display file status.

ARGUMENTS

  <path> - Path to node to stat.

OPTIONS

  --format string - Print statistics in given format. Allowed tokens: <hash> <size> <cumulsize> <type> <childs>. Conflicts with other format options. Default: <hash>
  Size: <size>
  CumulativeSize: <cumulsize>
  ChildBlocks: <childs>
  Type: <type>.
  --hash   bool   - Print only hash. Implies '--format=<hash>. Conflicts with other format options. Default: false.
  --size   bool   - Print only size. Implies '--format=<cumulsize>. Conflicts with other format options. Default: false.
```

## ipfs files write

```
USAGE
  ipfs files write <path> <data> - Write to a mutable file in a given filesystem.

ARGUMENTS

  <path> - Path to write to.
  <data> - Data to write.

OPTIONS

  -o, --offset   int  - Byte offset to begin writing at.
  -e, --create   bool - Create the file if it does not exist.
  -t, --truncate bool - Truncate the file to size zero before writing.
  -n, --count    int  - Maximum number of bytes to read.

DESCRIPTION

  Write data to a file in a given filesystem. This command allows you to specify
  a beginning offset to write to. The entire length of the input will be written.
  
  If the '--create' option is specified, the file will be created if it does not
  exist. Nonexistant intermediate directories will not be created.
  
  If the '--flush' option is set to false, changes will not be propogated to the
  merkledag root. This can make operations much faster when doing a large number
  of writes to a deeper directory structure.
  
  EXAMPLE:
  
      echo "hello world" | ipfs files write --create /myfs/a/b/file
      echo "hello world" | ipfs files write --truncate /myfs/a/b/file
  
  WARNING:
  
      Usage of the '--flush=false' option does not guarantee data durability until
  	the tree has been flushed. This can be accomplished by running 'ipfs files stat'
  	on the file or any of its ancestors.
```

## ipfs get

```
USAGE
  ipfs get <ipfs-path> - Download IPFS objects.

ARGUMENTS

  <ipfs-path> - The path to the IPFS object(s) to be outputted.

OPTIONS

  -o, --output            string - The path where the output should be stored.
  -a, --archive           bool   - Output a TAR archive. Default: false.
  -C, --compress          bool   - Compress the output with GZIP compression. Default: false.
  -l, --compression-level int    - The level of compression (1-9). Default: -1.

DESCRIPTION

  Stores to disk the data contained an IPFS or IPNS object(s) at the given path.
  
  By default, the output will be stored at './<ipfs-path>', but an alternate path
  can be specified with '--output=<path>' or '-o=<path>'.
  
  To output a TAR archive instead of unpacked files, use '--archive' or '-a'.
  
  To compress the output with GZIP compression, use '--compress' or '-C'. You
  may also specify the level of compression by specifying '-l=<1-9>'.
```

## ipfs id

```
USAGE
  ipfs id [<peerid>] - Show IPFS Node ID info.

ARGUMENTS

  [<peerid>] - Peer.ID of node to look up.

OPTIONS

  -f, --format string - Optional output format.

DESCRIPTION

  Prints out information about the specified peer.
  If no peer is specified, prints out information for local peers.
  
  'ipfs id' supports the format option for output with the following keys:
  <id> : The peers id.
  <aver>: Agent version.
  <pver>: Protocol version.
  <pubkey>: Public key.
  <addrs>: Addresses (newline delimited).
  
  EXAMPLE:
  
      ipfs id Qmece2RkXhsKe5CRooNisBTh4SK119KrXXGmoK6V3kb8aH -f="<addrs>\n"
```

## ipfs init

```
USAGE
  ipfs init - Initializes IPFS config file.

OPTIONS

  -b, --bits       int  - Number of bits to use in the generated RSA private key. Default: 2048.
  -e, --empty-repo bool - Don't add and pin help files to the local storage. Default: false.

DESCRIPTION

  Initializes IPFS configuration files and generates a new keypair.
  
  ipfs uses a repository in the local file system. By default, the repo is located
  at ~/.ipfs. To change the repo location, set the $IPFS_PATH environment variable:
  
      export IPFS_PATH=/path/to/ipfsrepo
```

## ipfs log

```
USAGE
  ipfs log - Interact with the daemon log output.

DESCRIPTION

  'ipfs log' contains utility commands to affect or read the logging
  output of a running daemon.

SUBCOMMANDS
  ipfs log level <subsystem> <level> - Change the logging level.
  ipfs log ls                        - List the logging subsystems.
  ipfs log tail                      - Read the logs.

  Use 'ipfs log <subcmd> --help' for more information about each command.
```

## ipfs log level

```
USAGE
  ipfs log level <subsystem> <level> - Change the logging level.

ARGUMENTS

  <subsystem> - The subsystem logging identifier. Use 'all' for all subsystems.
  <level>     - The log level, with 'debug' the most verbose and 'critical' the least verbose.
  			One of: debug, info, notice, warning, error, critical.
  		

DESCRIPTION

  'ipfs log level' is a utility command used to change the logging
  output of a running daemon.
```

## ipfs log ls

```
USAGE
  ipfs log ls - List the logging subsystems.

DESCRIPTION

  'ipfs log ls' is a utility command used to list the logging
  subsystems of a running daemon.
```

## ipfs log tail

```
USAGE
  ipfs log tail - Read the logs.

DESCRIPTION

  'ipfs log tail' is a utility command used to read log output as it is written.
```

## ipfs ls

```
USAGE
  ipfs ls <ipfs-path>... - List links from an object.

ARGUMENTS

  <ipfs-path>... - The path to the IPFS object(s) to list links from.

OPTIONS

  -v, --headers bool - Print table headers (Hash, Size, Name). Default: false.

DESCRIPTION

  Displays the links an IPFS or IPNS object(s) contains, with the following format:
  
    <link base58 hash> <link size in bytes> <link name>
```

## ipfs mount

```
USAGE
  ipfs mount - Mounts IPFS to the filesystem (read-only).

SYNOPSIS

  ipfs mount [-f <ipfs mount path>] [-n <ipns mount path>]

OPTIONS

  -f, --ipfs-path string - The path where IPFS should be mounted.
  -n, --ipns-path string - The path where IPNS should be mounted.

DESCRIPTION

  Mount ipfs at a read-only mountpoint on the OS. The default, /ipfs and /ipns,
  are set in the configutation file, but can be overriden by the options.
  All ipfs objects will be accessible under this directory. Note that the
  root will not be listable, as it is virtual. Access known paths directly.
  
  You may have to create /ipfs and /ipns before using 'ipfs mount':
  
  > sudo mkdir /ipfs /ipns
  > sudo chown `whoami` /ipfs /ipns
  > ipfs daemon &
  > ipfs mount
  
  Example:
  
  # setup
  > mkdir foo
  > echo "baz" > foo/bar
  > ipfs add -r foo
  added QmWLdkp93sNxGRjnFHPaYg8tCQ35NBY3XPn6KiETd3Z4WR foo/bar
  added QmSh5e7S6fdcu75LAbXNZAFY2nGyZUJXyLCJDvn2zRkWyC foo
  > ipfs ls QmSh5e7S6fdcu75LAbXNZAFY2nGyZUJXyLCJDvn2zRkWyC
  QmWLdkp93sNxGRjnFHPaYg8tCQ35NBY3XPn6KiETd3Z4WR 12 bar
  > ipfs cat QmWLdkp93sNxGRjnFHPaYg8tCQ35NBY3XPn6KiETd3Z4WR
  baz
  
  # mount
  > ipfs daemon &
  > ipfs mount
  IPFS mounted at: /ipfs
  IPNS mounted at: /ipns
  > cd /ipfs/QmSh5e7S6fdcu75LAbXNZAFY2nGyZUJXyLCJDvn2zRkWyC
  > ls
  bar
  > cat bar
  baz
  > cat /ipfs/QmSh5e7S6fdcu75LAbXNZAFY2nGyZUJXyLCJDvn2zRkWyC/bar
  baz
  > cat /ipfs/QmWLdkp93sNxGRjnFHPaYg8tCQ35NBY3XPn6KiETd3Z4WR
  baz
```

## ipfs name

```
USAGE
  ipfs name - IPFS namespace (IPNS) tool.

DESCRIPTION

  IPNS is a PKI namespace, where names are the hashes of public keys, and
  the private key enables publishing new (signed) values. In both publish
  and resolve, the default value of <name> is your own identity public key.
  
  
  Examples:
  
  Publish an <ipfs-path> to your identity name:
  
    > ipfs name publish /ipfs/QmatmE9msSfkKxoffpHwNLNKgwZG8eT9Bud6YoPab52vpy
    Published to QmbCMUZw6JFeZ7Wp9jkzbye3Fzp2GGcPgC3nmeUjfVF87n: /ipfs/QmatmE9msSfkKxoffpHwNLNKgwZG8eT9Bud6YoPab52vpy
  
  Publish an <ipfs-path> to another public key:
  
    > ipfs name publish /ipfs/QmatmE9msSfkKxoffpHwNLNKgwZG8eT9Bud6YoPab52vpy QmbCMUZw6JFeZ7Wp9jkzbye3Fzp2GGcPgC3nmeUjfVF87n
    Published to QmbCMUZw6JFeZ7Wp9jkzbye3Fzp2GGcPgC3nmeUjfVF87n: /ipfs/QmatmE9msSfkKxoffpHwNLNKgwZG8eT9Bud6YoPab52vpy
  
  Resolve the value of your identity:
  
    > ipfs name resolve
    /ipfs/QmatmE9msSfkKxoffpHwNLNKgwZG8eT9Bud6YoPab52vpy
  
  Resolve the value of another name:
  
    > ipfs name resolve QmaCpDMGvV2BGHeYERUEnRQAwe3N8SzbUtfsmvsqQLuvuJ
    /ipfs/QmSiTko9JZyabH56y2fussEt1A5oDqsFXB3CkvAqraFryz
  
  Resolve the value of a reference:
  
    > ipfs name resolve ipfs.io
    /ipfs/QmaBvfZooxWkrv7D3r8LS9moNjzD2o525XMZze69hhoxf5

SUBCOMMANDS
  ipfs name publish <ipfs-path> - Publish an object to IPNS.
  ipfs name resolve [<name>]    - Gets the value currently published at an IPNS name.

  Use 'ipfs name <subcmd> --help' for more information about each command.
```

## ipfs name publish

```
USAGE
  ipfs name publish <ipfs-path> - Publish an object to IPNS.

ARGUMENTS

  <ipfs-path> - IPFS path of the object to be published.

OPTIONS

  --resolve           bool   - Resolve given path before publishing. Default: true.
  -t,      --lifetime string - Time duration that the record will be valid for. Default: 24h.
      This accepts durations such as "300s", "1.5h" or "2h45m". Valid time units are
      "ns", "us" (or "µs"), "ms", "s", "m", "h".
  --ttl               string - Time duration this record should be cached for (caution: experimental).

DESCRIPTION

  IPNS is a PKI namespace, where names are the hashes of public keys, and
  the private key enables publishing new (signed) values. In publish, the
  default value of <name> is your own identity public key.
  
  Examples:
  
  Publish an <ipfs-path> to your identity name:
  
    > ipfs name publish /ipfs/QmatmE9msSfkKxoffpHwNLNKgwZG8eT9Bud6YoPab52vpy
    Published to QmbCMUZw6JFeZ7Wp9jkzbye3Fzp2GGcPgC3nmeUjfVF87n: /ipfs/QmatmE9msSfkKxoffpHwNLNKgwZG8eT9Bud6YoPab52vpy
  
  Publish an <ipfs-path> to another public key (not implemented):
  
    > ipfs name publish /ipfs/QmatmE9msSfkKxoffpHwNLNKgwZG8eT9Bud6YoPab52vpy QmbCMUZw6JFeZ7Wp9jkzbye3Fzp2GGcPgC3nmeUjfVF87n
    Published to QmbCMUZw6JFeZ7Wp9jkzbye3Fzp2GGcPgC3nmeUjfVF87n: /ipfs/QmatmE9msSfkKxoffpHwNLNKgwZG8eT9Bud6YoPab52vpy
```

## ipfs name resolve

```
USAGE
  ipfs name resolve [<name>] - Gets the value currently published at an IPNS name.

ARGUMENTS

  [<name>] - The IPNS name to resolve. Defaults to your node's peerID.

OPTIONS

  -r, --recursive bool - Resolve until the result is not an IPNS name. Default: false.
  -n, --nocache   bool - Do not used cached entries. Default: false.

DESCRIPTION

  IPNS is a PKI namespace, where names are the hashes of public keys, and
  the private key enables publishing new (signed) values. In resolve, the
  default value of <name> is your own identity public key.
  
  
  Examples:
  
  Resolve the value of your identity:
  
    > ipfs name resolve
    /ipfs/QmatmE9msSfkKxoffpHwNLNKgwZG8eT9Bud6YoPab52vpy
  
  Resolve the value of another name:
  
    > ipfs name resolve QmaCpDMGvV2BGHeYERUEnRQAwe3N8SzbUtfsmvsqQLuvuJ
    /ipfs/QmSiTko9JZyabH56y2fussEt1A5oDqsFXB3CkvAqraFryz
  
  Resolve the value of a reference:
  
    > ipfs name resolve ipfs.io
    /ipfs/QmaBvfZooxWkrv7D3r8LS9moNjzD2o525XMZze69hhoxf5
```

## ipfs object

```
USAGE
  ipfs object - Interact with ipfs objects.

DESCRIPTION

  'ipfs object' is a plumbing command used to manipulate DAG objects
  directly.

SUBCOMMANDS
  ipfs object links <key>          - Outputs the links pointed to by the specified object.
  ipfs object new [<template>]     - Creates a new object from an ipfs template.
  ipfs object patch                - Create a new merkledag object based on an existing one.
  ipfs object put <data>           - Stores input as a DAG object, outputs its key.
  ipfs object stat <key>           - Get stats for the DAG node named by <key>.
  ipfs object data <key>           - Outputs the raw bytes in an IPFS object.
  ipfs object diff <obj_a> <obj_b> - Takes a diff of the two given objects.
  ipfs object get <key>            - Get and serialize the DAG node named by <key>.

  Use 'ipfs object <subcmd> --help' for more information about each command.
```

## ipfs object data

```
USAGE
  ipfs object data <key> - Outputs the raw bytes in an IPFS object.

ARGUMENTS

  <key> - Key of the object to retrieve, in base58-encoded multihash format.

DESCRIPTION

  'ipfs object data' is a plumbing command for retrieving the raw bytes stored in
  a DAG node. It outputs to stdout, and <key> is a base58 encoded
  multihash.
  
  Note that the "--encoding" option does not affect the output, since the
  output is the raw data of the object.
```

## ipfs object diff

```
USAGE
  ipfs object diff <obj_a> <obj_b> - Takes a diff of the two given objects.

ARGUMENTS

  <obj_a> - Object to diff against.
  <obj_b> - Object to diff.

OPTIONS

  -v, --verbose bool - Print extra information.

DESCRIPTION

  'ipfs object diff' is a command used to show the differences between
  two ipfs objects.
  
  Example:
  
     > ls foo
     bar baz/ giraffe
     > ipfs add -r foo
     ...
     Added QmegHcnrPgMwC7tBiMxChD54fgQMBUecNw9nE9UUU4x1bz foo
     > OBJ_A=QmegHcnrPgMwC7tBiMxChD54fgQMBUecNw9nE9UUU4x1bz
     > echo "different content" > foo/bar
     > ipfs add -r foo
     ...
     Added QmcmRptkSPWhptCttgHg27QNDmnV33wAJyUkCnAvqD3eCD foo
     > OBJ_B=QmcmRptkSPWhptCttgHg27QNDmnV33wAJyUkCnAvqD3eCD
     > ipfs object diff -v $OBJ_A $OBJ_B
     Changed "bar" from QmNgd5cz2jNftnAHBhcRUGdtiaMzb5Rhjqd4etondHHST8 to QmRfFVsjSXkhFxrfWnLpMae2M4GBVsry6VAuYYcji5MiZb.
```

## ipfs object get

```
USAGE
  ipfs object get <key> - Get and serialize the DAG node named by <key>.

ARGUMENTS

  <key> - Key of the object to retrieve, in base58-encoded multihash format.

DESCRIPTION

  'ipfs object get' is a plumbing command for retrieving DAG nodes.
  It serializes the DAG node to the format specified by the "--encoding"
  flag. It outputs to stdout, and <key> is a base58 encoded multihash.
  
  This command outputs data in the following encodings:
    * "protobuf"
    * "json"
    * "xml"
  (Specified by the "--encoding" or "-enc" flag)
```

## ipfs object links

```
USAGE
  ipfs object links <key> - Outputs the links pointed to by the specified object.

ARGUMENTS

  <key> - Key of the object to retrieve, in base58-encoded multihash format.

OPTIONS

  -v, --headers bool - Print table headers (Hash, Size, Name). Default: false.

DESCRIPTION

  'ipfs object links' is a plumbing command for retrieving the links from
  a DAG node. It outputs to stdout, and <key> is a base58 encoded
  multihash.
```

## ipfs object new

```
USAGE
  ipfs object new [<template>] - Creates a new object from an ipfs template.

ARGUMENTS

  [<template>] - Template to use. Optional.

DESCRIPTION

  'ipfs object new' is a plumbing command for creating new DAG nodes.
  By default it creates and returns a new empty merkledag node, but
  you may pass an optional template argument to create a preformatted
  node.
  
  Available templates:
  	* unixfs-dir
```

## ipfs object patch

```
USAGE
  ipfs object patch - Create a new merkledag object based on an existing one.

DESCRIPTION

  'ipfs object patch <root> <cmd> <args>' is a plumbing command used to
  build custom DAG objects. It mutates objects, creating new objects as a
  result. This is the Merkle-DAG version of modifying an object.

SUBCOMMANDS
  ipfs object patch append-data <root> <data>    - Append data to the data segment of a dag node.
  ipfs object patch add-link <root> <name> <ref> - Add a link to a given object.
  ipfs object patch rm-link <root> <link>        - Remove a link from an object.
  ipfs object patch set-data <root> <data>       - Set the data field of an ipfs object.

  Use 'ipfs object patch <subcmd> --help' for more information about each command.
```

## ipfs object patch add-link

```
USAGE
  ipfs object patch add-link <root> <name> <ref> - Add a link to a given object.

ARGUMENTS

  <root> - The hash of the node to modify.
  <name> - Name of link to create.
  <ref>  - IPFS object to add link to.

OPTIONS

  -p, --create bool - Create intermediary nodes. Default: false.

DESCRIPTION

  Add a Merkle-link to the given object and return the hash of the result.
  
  Example:
  
      $ EMPTY_DIR=$(ipfs object new unixfs-dir)
      $ BAR=$(echo "bar" | ipfs add -q)
      $ ipfs object patch $EMPTY_DIR add-link foo $BAR
  
  This takes an empty directory, and adds a link named 'foo' under it, pointing to
  a file containing 'bar', and returns the hash of the new object.
```

## ipfs object patch append-data

```
USAGE
  ipfs object patch append-data <root> <data> - Append data to the data segment of a dag node.

ARGUMENTS

  <root> - The hash of the node to modify.
  <data> - Data to append.

DESCRIPTION

  Append data to what already exists in the data segment in the given object.
  
  Example:
  
  	$ echo "hello" | ipfs object patch $HASH append-data
  
  NOTE: This does not append data to a file - it modifies the actual raw
  data within an object. Objects have a max size of 1MB and objects larger than
  the limit will not be respected by the network.
```

## ipfs object patch rm-link

```
USAGE
  ipfs object patch rm-link <root> <link> - Remove a link from an object.

ARGUMENTS

  <root> - The hash of the node to modify.
  <link> - Name of the link to remove.

DESCRIPTION

  Removes a link by the given name from root.
```

## ipfs object patch set-data

```
USAGE
  ipfs object patch set-data <root> <data> - Set the data field of an ipfs object.

ARGUMENTS

  <root> - The hash of the node to modify.
  <data> - The data to set the object to.

DESCRIPTION

  Set the data of an ipfs object from stdin or with the contents of a file.
  
  Example:
  
      $ echo "my data" | ipfs object patch $MYHASH set-data
```

## ipfs object put

```
USAGE
  ipfs object put <data> - Stores input as a DAG object, outputs its key.

ARGUMENTS

  <data> - Data to be stored as a DAG object.

OPTIONS

  --inputenc     string - Encoding type of input data. One of: {"protobuf", "json"}. Default: json.
  --datafieldenc string - Encoding type of the data field, either "text" or "base64". Default: text.

DESCRIPTION

  'ipfs object put' is a plumbing command for storing DAG nodes.
  It reads from stdin, and the output is a base58 encoded multihash.
  
  Data should be in the format specified by the --inputenc flag.
  --inputenc may be one of the following:
  	* "protobuf"
  	* "json" (default)
  
  Examples:
  
  	$ echo '{ "Data": "abc" }' | ipfs object put
  
  This creates a node with the data 'abc' and no links. For an object with links,
  create a file named 'node.json' with the contents:
  
      {
          "Data": "another",
          "Links": [ {
              "Name": "some link",
              "Hash": "QmXg9Pp2ytZ14xgmQjYEiHjVjMFXzCVVEcRTWJBmLgR39V",
              "Size": 8
          } ]
      }
  
  And then run:
  
  	$ ipfs object put node.json
```

## ipfs object stat

```
USAGE
  ipfs object stat <key> - Get stats for the DAG node named by <key>.

ARGUMENTS

  <key> - Key of the object to retrieve, in base58-encoded multihash format.

DESCRIPTION

  'ipfs object stat' is a plumbing command to print DAG node statistics.
  <key> is a base58 encoded multihash. It outputs to stdout:
  
  	NumLinks        int number of links in link table
  	BlockSize       int size of the raw, encoded data
  	LinksSize       int size of the links segment
  	DataSize        int size of the data segment
  	CumulativeSize  int cumulative size of object and its references
```

## ipfs pin

```
USAGE
  ipfs pin - Pin (and unpin) objects to local storage.

SUBCOMMANDS
  ipfs pin ls [<ipfs-path>]... - List objects pinned to local storage.
  ipfs pin add <ipfs-path>...  - Pins objects to local storage.
  ipfs pin rm <ipfs-path>...   - Removes the pinned object from local storage.

  Use 'ipfs pin <subcmd> --help' for more information about each command.
```

## ipfs pin add

```
USAGE
  ipfs pin add <ipfs-path>... - Pins objects to local storage.

ARGUMENTS

  <ipfs-path>... - Path to object(s) to be pinned.

OPTIONS

  -r, --recursive bool - Recursively pin the object linked to by the specified object(s). Default: true.

DESCRIPTION

  Stores an IPFS object(s) from a given path locally to disk.
```

## ipfs pin ls

```
USAGE
  ipfs pin ls [<ipfs-path>]... - List objects pinned to local storage.

ARGUMENTS

  [<ipfs-path>]... - Path to object(s) to be listed.

OPTIONS

  -t, --type  string - The type of pinned keys to list. Can be "direct", "indirect", "recursive", or "all". Default: all.
  -q, --quiet bool   - Write just hashes of objects. Default: false.

DESCRIPTION

  Returns a list of objects that are pinned locally.
  By default, all pinned objects are returned, but the '--type' flag or arguments can restrict that to a specific pin type or to some specific objects respectively.
  
  Use --type=<type> to specify the type of pinned keys to list. Valid values are:
      * "direct": pin that specific object.
      * "recursive": pin that specific object, and indirectly pin all its decendants
      * "indirect": pinned indirectly by an ancestor (like a refcount)
      * "all"
  
  With arguments, the command fails if any of the arguments is not a pinned object.
  And if --type=<type> is additionally used, the command will also fail if any of the arguments is not of the specified type.
  
  Example:
  	$ echo "hello" | ipfs add -q
  	QmZULkCELmmk5XNfCgTnCyFgAVxBRBXyDHGGMVoLFLiXEN
  	$ ipfs pin ls
  	QmZULkCELmmk5XNfCgTnCyFgAVxBRBXyDHGGMVoLFLiXEN recursive
  	# now remove the pin, and repin it directly
  	$ ipfs pin rm QmZULkCELmmk5XNfCgTnCyFgAVxBRBXyDHGGMVoLFLiXEN
  	unpinned QmZULkCELmmk5XNfCgTnCyFgAVxBRBXyDHGGMVoLFLiXEN
  	$ ipfs pin add -r=false QmZULkCELmmk5XNfCgTnCyFgAVxBRBXyDHGGMVoLFLiXEN
  	pinned QmZULkCELmmk5XNfCgTnCyFgAVxBRBXyDHGGMVoLFLiXEN directly
  	$ ipfs pin ls --type=direct
  	QmZULkCELmmk5XNfCgTnCyFgAVxBRBXyDHGGMVoLFLiXEN direct
  	$ ipfs pin ls QmZULkCELmmk5XNfCgTnCyFgAVxBRBXyDHGGMVoLFLiXEN
  	QmZULkCELmmk5XNfCgTnCyFgAVxBRBXyDHGGMVoLFLiXEN direct
```

## ipfs pin rm

```
USAGE
  ipfs pin rm <ipfs-path>... - Removes the pinned object from local storage.

ARGUMENTS

  <ipfs-path>... - Path to object(s) to be unpinned.

OPTIONS

  -r, --recursive bool - Recursively unpin the object linked to by the specified object(s). Default: true.

DESCRIPTION

  Removes the pin from the given object allowing it to be garbage
  collected if needed. (By default, recursively. Use -r=false for direct pins)
```

## ipfs ping

```
USAGE
  ipfs ping <peer ID>... - Send echo request packets to IPFS hosts.

SYNOPSIS

  ipfs ping <peerId> [--count <int>| -n]

ARGUMENTS

  <peer ID>... - ID of peer to be pinged.

OPTIONS

  -n, --count int - Number of ping messages to send. Default: 10.

DESCRIPTION

  'ipfs ping' is a tool to test sending data to other nodes. It finds nodes
  via the routing system, sends pings, waits for pongs, and prints out round-
  trip latency information.
```

## ipfs refs

```
USAGE
  ipfs refs <ipfs-path>... - Lists links (references) from an object.

ARGUMENTS

  <ipfs-path>... - Path to the object(s) to list refs from.

OPTIONS

  --format            string - Emit edges with given format. Available tokens: <src> <dst> <linkname>. Default: <dst>.
  -e,     --edges     bool   - Emit edge format: `<from> -> <to>`. Default: false.
  -u,     --unique    bool   - Omit duplicate refs from output. Default: false.
  -r,     --recursive bool   - Recursively list links of child nodes. Default: false.

DESCRIPTION

  Lists the hashes of all the links an IPFS or IPNS object(s) contains,
  with the following format:
  
    <link base58 hash>
  
  NOTE: List all references recursively by using the flag '-r'.

SUBCOMMANDS
  ipfs refs local - Lists all local references.

  Use 'ipfs refs <subcmd> --help' for more information about each command.
```

## ipfs refs local

```
USAGE
  ipfs refs local - Lists all local references.

DESCRIPTION

  Displays the hashes of all local objects.
```

## ipfs repo

```
USAGE
  ipfs repo - Manipulate the IPFS repo.

DESCRIPTION

  'ipfs repo' is a plumbing command used to manipulate the repo.

SUBCOMMANDS
  ipfs repo gc   - Perform a garbage collection sweep on the repo.
  ipfs repo stat - Get stats for the currently used repo.
  ipfs repo fsck - Removes repo lockfiles.

  Use 'ipfs repo <subcmd> --help' for more information about each command.
```

## ipfs repo fsck

```
USAGE
  ipfs repo fsck - Removes repo lockfiles.

DESCRIPTION

  'ipfs repo fsck' is a plumbing command that will remove repo and level db
  lockfiles, as well as the api file. This command can only run when no ipfs
  daemons are running.
```

## ipfs repo gc

```
USAGE
  ipfs repo gc - Perform a garbage collection sweep on the repo.

OPTIONS

  -q, --quiet bool - Write minimal output. Default: false.

DESCRIPTION

  'ipfs repo gc' is a plumbing command that will sweep the local
  set of stored objects and remove ones that are not pinned in
  order to reclaim hard disk space.
```

## ipfs repo stat

```
USAGE
  ipfs repo stat - Get stats for the currently used repo.

OPTIONS

  --human bool - Output RepoSize in MiB. Default: false.

DESCRIPTION

  'ipfs repo stat' is a plumbing command that will scan the local
  set of stored objects and print repo statistics. It outputs to stdout:
  NumObjects      int Number of objects in the local repo.
  RepoPath        string The path to the repo being currently used.
  RepoSize        int Size in bytes that the repo is currently taking.
```

## ipfs resolve

```
USAGE
  ipfs resolve <name> - Resolve the value of names to IPFS.

ARGUMENTS

  <name> - The name to resolve.

OPTIONS

  -r, --recursive bool - Resolve until the result is an IPFS name. Default: false.

DESCRIPTION

  There are a number of mutable name protocols that can link among
  themselves and into IPNS. For example IPNS references can (currently)
  point at an IPFS object, and DNS links can point at other DNS links, IPNS
  entries, or IPFS objects. This command accepts any of these
  identifiers and resolves them to the referenced item.
  
  EXAMPLES
  
  Resolve the value of your identity:
  
    $ ipfs resolve /ipns/QmatmE9msSfkKxoffpHwNLNKgwZG8eT9Bud6YoPab52vpy
    /ipfs/Qmcqtw8FfrVSBaRmbWwHxt3AuySBhJLcvmFYi3Lbc4xnwj
  
  Resolve the value of another name:
  
    $ ipfs resolve /ipns/QmbCMUZw6JFeZ7Wp9jkzbye3Fzp2GGcPgC3nmeUjfVF87n
    /ipns/QmatmE9msSfkKxoffpHwNLNKgwZG8eT9Bud6YoPab52vpy
  
  Resolve the value of another name recursively:
  
    $ ipfs resolve -r /ipns/QmbCMUZw6JFeZ7Wp9jkzbye3Fzp2GGcPgC3nmeUjfVF87n
    /ipfs/Qmcqtw8FfrVSBaRmbWwHxt3AuySBhJLcvmFYi3Lbc4xnwj
  
  Resolve the value of an IPFS DAG path:
  
    $ ipfs resolve /ipfs/QmeZy1fGbwgVSrqbfh9fKQrAWgeyRnj7h8fsHS1oy3k99x/beep/boop
    /ipfs/QmYRMjyvAiHKN9UTi8Bzt1HUspmSRD8T8DwxfSMzLgBon1
```

## ipfs stats

```
USAGE
  ipfs stats - Query ipfs statistics.

SYNOPSIS

  ipfs stats <command>

DESCRIPTION

  'ipfs stats' is a set of commands to help look at statistics for your ipfs node.

SUBCOMMANDS
  ipfs stats bw - Print ipfs bandwidth information.

  Use 'ipfs stats <subcmd> --help' for more information about each command.
```

## ipfs stats bw

```
USAGE
  ipfs stats bw - Print ipfs bandwidth information.

SYNOPSIS

  ipfs stats bw [--peer <peerId> | -p] [--proto <protocol> | -t] [--poll] [--interval <timeInterval> | -i]

OPTIONS

  -p,   --peer     string - Specify a peer to print bandwidth for.
  -t,   --proto    string - Specify a protocol to print bandwidth for.
  --poll           bool   - Print bandwidth at an interval. Default: false.
  -i,   --interval string - Time interval to wait between updating output, if 'poll' is true.
  
      This accepts durations such as "300s", "1.5h" or "2h45m". Valid time units are:
      "ns", "us" (or "µs"), "ms", "s", "m", "h". Default: 1s.

DESCRIPTION

  'ipfs stats bw' prints bandwidth information for the ipfs daemon.
  It displays: TotalIn, TotalOut, RateIn, RateOut.
  
  By default, overall bandwidth and all protocols are shown. To limit bandwidth to
  a particular peer, use the 'peer' option along with that peer's multihash id. To
  specify a specific protocol, use the 'proto' option. The 'peer' and 'proto'
  options cannot be specified simultaneously. The protocols that be queried using
  this method are outlined in the specification: https://github.com/ipfs/specs/blob/master/libp2p/7-properties.md#757-protocol-multicodecs
  
  Example protocol options:
    - /ipfs/id/1.0.0
    - /ipfs/bitswap
    - /ipfs/dht
  
  Example:
  
      > ipfs stats bw -t /ipfs/bitswap
      Bandwidth
      TotalIn: 5.0MB
      TotalOut: 0B
      RateIn: 343B/s
      RateOut: 0B/s
      > ipfs stats bw -p QmepgFW7BHEtU4pZJdxaNiv75mKLLRQnPi1KaaXmQN4V1a
      Bandwidth
      TotalIn: 4.9MB
      TotalOut: 12MB
      RateIn: 0B/s
      RateOut: 0B/s
```

## ipfs swarm

```
USAGE
  ipfs swarm - Swarm inspection tool.

DESCRIPTION

  'ipfs swarm' is a tool to manipulate the network swarm. The swarm is the
  component that opens, listens for, and maintains connections to other
  ipfs peers in the internet.

SUBCOMMANDS
  ipfs swarm peers                   - List peers with open connections.
  ipfs swarm addrs                   - List known addresses. Useful for debugging.
  ipfs swarm connect <address>...    - Open connection to a given address.
  ipfs swarm disconnect <address>... - Close connection to a given address.
  ipfs swarm filters                 - Manipulate address filters.

  Use 'ipfs swarm <subcmd> --help' for more information about each command.
```

## ipfs swarm addrs

```
USAGE
  ipfs swarm addrs - List known addresses. Useful for debugging.

DESCRIPTION

  'ipfs swarm addrs' lists all addresses this node is aware of.

SUBCOMMANDS
  ipfs swarm addrs local - List local addresses.

  Use 'ipfs swarm addrs <subcmd> --help' for more information about each command.
```

## ipfs swarm addrs local

```
USAGE
  ipfs swarm addrs local - List local addresses.

OPTIONS

  --id bool - Show peer ID in addresses. Default: false.

DESCRIPTION

  'ipfs swarm addrs local' lists all local addresses the node is listening on.
```

## ipfs swarm connect

```
USAGE
  ipfs swarm connect <address>... - Open connection to a given address.

ARGUMENTS

  <address>... - Address of peer to connect to.

DESCRIPTION

  'ipfs swarm connect' opens a new direct connection to a peer address.
  
  The address format is an ipfs multiaddr:
  
  ipfs swarm connect /ip4/104.131.131.82/tcp/4001/ipfs/QmaCpDMGvV2BGHeYERUEnRQAwe3N8SzbUtfsmvsqQLuvuJ
```

## ipfs swarm disconnect

```
USAGE
  ipfs swarm disconnect <address>... - Close connection to a given address.

ARGUMENTS

  <address>... - Address of peer to disconnect from.

DESCRIPTION

  'ipfs swarm disconnect' closes a connection to a peer address. The address format
  is an ipfs multiaddr:
  
  ipfs swarm disconnect /ip4/104.131.131.82/tcp/4001/ipfs/QmaCpDMGvV2BGHeYERUEnRQAwe3N8SzbUtfsmvsqQLuvuJ
  
  The disconnect is not permanent; if ipfs needs to talk to that address later, it will reconnect.
```

## ipfs swarm filters

```
USAGE
  ipfs swarm filters - Manipulate address filters.

DESCRIPTION

  'ipfs swarm filters' will list out currently applied filters. Its subcommands can be used
  to add or remove said filters. Filters are specified using the multiaddr-filter format:
  
  example:
  
      /ip4/192.168.0.0/ipcidr/16
  
  Where the above is equivalent to the standard CIDR:
  
      192.168.0.0/16
  
  Filters default to those specified under the "Swarm.AddrFilters" config key.

SUBCOMMANDS
  ipfs swarm filters rm <address>...  - Remove an address filter.
  ipfs swarm filters add <address>... - Add an address filter.

  Use 'ipfs swarm filters <subcmd> --help' for more information about each command.
```

## ipfs swarm filters add

```
USAGE
  ipfs swarm filters add <address>... - Add an address filter.

ARGUMENTS

  <address>... - Multiaddr to filter.

DESCRIPTION

  'ipfs swarm filters add' will add an address filter to the daemons swarm.
  Filters applied this way will not persist daemon reboots, to achieve that,
  add your filters to the ipfs config file.
```

## ipfs swarm filters rm

```
USAGE
  ipfs swarm filters rm <address>... - Remove an address filter.

ARGUMENTS

  <address>... - Multiaddr filter to remove.

DESCRIPTION

  'ipfs swarm filters rm' will remove an address filter from the daemons swarm.
  Filters removed this way will not persist daemon reboots, to achieve that,
  remove your filters from the ipfs config file.
```

## ipfs swarm peers

```
USAGE
  ipfs swarm peers - List peers with open connections.

OPTIONS

  -v, --verbose bool - Also display latency along with peer information in the following form: <peer address> <latency>.

DESCRIPTION

  'ipfs swarm peers' lists the set of peers this node is connected to.
```

## ipfs tar

```
USAGE
  ipfs tar - Utility functions for tar files in IPFS.

SUBCOMMANDS
  ipfs tar add <file> - Import a tar file into ipfs.
  ipfs tar cat <path> - Export a tar file from IPFS.

  Use 'ipfs tar <subcmd> --help' for more information about each command.
```

## ipfs tar add

```
USAGE
  ipfs tar add <file> - Import a tar file into ipfs.

ARGUMENTS

  <file> - Tar file to add.

DESCRIPTION

  'ipfs tar add' will parse a tar file and create a merkledag structure to represent it.
```

## ipfs tar cat

```
USAGE
  ipfs tar cat <path> - Export a tar file from IPFS.

ARGUMENTS

  <path> - IPFS path of archive to export.

DESCRIPTION

  'ipfs tar cat' will export a tar file from a previously imported one in IPFS.
```

## ipfs tour

```
USAGE
  ipfs tour [<id>] - An introduction to IPFS.

ARGUMENTS

  [<id>] - The id of the topic you would like to tour.

DESCRIPTION

  This is a tour that takes you through various IPFS concepts,
  features, and tools to make sure you get up to speed with
  IPFS very quickly. To start, run:
  
      ipfs tour

SUBCOMMANDS
  ipfs tour list    - Show a list of IPFS Tour topics.
  ipfs tour next    - Show the next IPFS Tour topic.
  ipfs tour restart - Restart the IPFS Tour.

  Use 'ipfs tour <subcmd> --help' for more information about each command.
```

## ipfs tour list

```
USAGE
  ipfs tour list - Show a list of IPFS Tour topics.
```

## ipfs tour next

```
USAGE
  ipfs tour next - Show the next IPFS Tour topic.
```

## ipfs tour restart

```
USAGE
  ipfs tour restart - Restart the IPFS Tour.
```

## ipfs update

```
NAME:
   ipfs-update - update ipfs

USAGE:
   ipfs-update [global options] command [command options] [arguments...]
   
VERSION:
   0.1.0
   
COMMANDS:
   versions	print out all available versions
   version	print out currently installed version
   install	install a version of ipfs
   stash	stashes copy of currently installed ipfs binary
   revert	revert to previously installed version of ipfs
   fetch	fetch a given (default: latest) version of ipfs
   help, h	Shows a list of commands or help for one command
   
GLOBAL OPTIONS:
   --verbose		print verbose output
   --help, -h		show help
   --version, -v	print the version
```

## ipfs version

```
USAGE
  ipfs version - Shows ipfs version information.

OPTIONS

  -n,     --number bool - Only show the version number. Default: false.
  --commit         bool - Show the commit hash. Default: false.
  --repo           bool - Show repo version. Default: false.

DESCRIPTION

  Returns the current version of ipfs and exits.
```

