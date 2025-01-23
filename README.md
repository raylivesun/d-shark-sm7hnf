<!DOCTYPE html>
<html lang="en"><head>
<meta http-equiv="content-type" content="text/html; charset=UTF-8">
<meta charset="UTF-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="generator" content="Asciidoctor 2.0.16">
<title>wireshark(1)</title>
<link rel="stylesheet" href="README_files/ws.css">
</head>
<body class="manpage">
<div id="header">
<h1>wireshark(1) Manual Page</h1>
<h2 id="_name">NAME</h2>
<div class="sectionbody">
<p>wireshark - Interactively dump and analyze network traffic</p>
</div>
</div>
<div id="content">
<div class="sect1">
<h2 id="_synopsis">SYNOPSIS</h2>
<div class="sectionbody">
<div class="paragraph">
<p><span class="nowrap"><strong>wireshark</strong></span>
<span class="nowrap">[ <strong>-i</strong> &lt;capture interface&gt;|- ]</span>
<span class="nowrap">[ <strong>-f</strong> &lt;capture filter&gt; ]</span>
<span class="nowrap">[ <strong>-Y</strong> &lt;display filter&gt; ]</span>
<span class="nowrap">[ <strong>-w</strong> &lt;outfile&gt; ]</span>
<span class="nowrap">[ <strong>options</strong> ]</span>
<span class="nowrap">[ &lt;infile&gt; ]</span></p>
</div>
</div>
</div>
<div class="sect1">
<h2 id="_description">DESCRIPTION</h2>
<div class="sectionbody">
<div class="paragraph">
<p><strong>Wireshark</strong> is a GUI network protocol analyzer.  It lets you
interactively browse packet data from a live network or from a
previously saved capture file.  <strong>Wireshark</strong>'s native capture file
formats are <strong>pcapng</strong> format and <strong>pcap</strong> format; it can read and write
both formats..  <strong>pcap</strong> format is also the format used by <strong>tcpdump</strong> and
various other tools; <strong>tcpdump</strong>, when using newer verions of the
<strong>libpcap</strong> library, can also read some pcapng files, and, on newer
versions of macOS, can read all pcapng files and can write them as well.</p>
</div>
<div class="paragraph">
<p><strong>Wireshark</strong> can also read / import the following file formats:</p>
</div>
<div class="ulist">
<ul>
<li>
<p>Oracle (previously Sun) <strong>snoop</strong> and <strong>atmsnoop</strong> captures</p>
</li>
<li>
<p>Finisar (previously Shomiti) <strong>Surveyor</strong> captures</p>
</li>
<li>
<p>Microsoft <strong>Network Monitor</strong> captures</p>
</li>
<li>
<p>Novell <strong>LANalyzer</strong> captures</p>
</li>
<li>
<p>AIX’s <strong>iptrace</strong> captures</p>
</li>
<li>
<p>Cinco Networks <strong>NetXRay</strong> captures</p>
</li>
<li>
<p>NETSCOUT (previously Network Associates/Network General) Windows-based
<strong>Sniffer</strong> captures</p>
</li>
<li>
<p>Network General/Network Associates DOS-based <strong>Sniffer</strong> captures
(compressed or uncompressed)</p>
</li>
<li>
<p>LiveAction (previously WildPackets/Savvius) <strong>*Peek</strong>/<strong>EtherHelp</strong>/<strong>PacketGrabber</strong> captures</p>
</li>
<li>
<p><strong>RADCOM</strong>'s WAN/LAN analyzer captures</p>
</li>
<li>
<p>Viavi (previously Network Instruments) <strong>Observer</strong> captures</p>
</li>
<li>
<p><strong>Lucent/Ascend</strong> router debug output</p>
</li>
<li>
<p>captures from HP-UX <strong>nettl</strong></p>
</li>
<li>
<p><strong>Toshiba’s</strong> ISDN routers dump output</p>
</li>
<li>
<p>the output from <strong>i4btrace</strong> from the ISDN4BSD project</p>
</li>
<li>
<p>traces from the <strong>EyeSDN</strong> USB S0</p>
</li>
<li>
<p>the <strong>IPLog</strong> format output from the Cisco Secure Intrusion Detection System</p>
</li>
<li>
<p><strong>pppd logs</strong> (pppdump format)</p>
</li>
<li>
<p>the output from VMS’s <strong>TCPIPtrace</strong>/<strong>TCPtrace</strong>/<strong>UCX$TRACE</strong> utilities</p>
</li>
<li>
<p>the text output from the <strong>DBS Etherwatch</strong> VMS utility</p>
</li>
<li>
<p>Visual Networks' <strong>Visual UpTime</strong> traffic capture</p>
</li>
<li>
<p>the output from <strong>CoSine</strong> L2 debug</p>
</li>
<li>
<p>the output from InfoVista (previously Accellent) <strong>5View</strong> LAN agents</p>
</li>
<li>
<p>Endace Measurement Systems' ERF format captures</p>
</li>
<li>
<p>Linux Bluez Bluetooth stack <strong>hcidump -w</strong> traces</p>
</li>
<li>
<p>Catapult DCT2000 .out files</p>
</li>
<li>
<p>Gammu generated text output from Nokia DCT3 phones in Netmonitor mode</p>
</li>
<li>
<p>IBM Series (OS/400) Comm traces (ASCII &amp; UNICODE)</p>
</li>
<li>
<p>Juniper Netscreen snoop files</p>
</li>
<li>
<p>Symbian OS btsnoop files</p>
</li>
<li>
<p>TamoSoft CommView files</p>
</li>
<li>
<p>Tektronix K12xx 32bit .rf5 format files</p>
</li>
<li>
<p>Tektronix K12 text file format captures</p>
</li>
<li>
<p>Apple PacketLogger files</p>
</li>
<li>
<p>Captures from Aethra Telecommunications' PC108 software for their test
instruments</p>
</li>
<li>
<p>Citrix NetScaler Trace files</p>
</li>
<li>
<p>Android Logcat binary and text format logs</p>
</li>
<li>
<p>Colasoft Capsa and PacketBuilder captures</p>
</li>
<li>
<p>Micropross mplog files</p>
</li>
<li>
<p>Unigraf DPA-400 DisplayPort AUX channel monitor traces</p>
</li>
<li>
<p>802.15.4 traces from Daintree’s Sensor Network Analyzer</p>
</li>
<li>
<p>MPEG-2 Transport Streams as defined in ISO/IEC 13818-1</p>
</li>
<li>
<p>Log files from the <em>candump</em> utility</p>
</li>
<li>
<p>Logs from the BUSMASTER tool</p>
</li>
<li>
<p>Ixia IxVeriWave raw captures</p>
</li>
<li>
<p>Rabbit Labs CAM Inspector files</p>
</li>
<li>
<p><em>systemd</em> journal files</p>
</li>
<li>
<p>3GPP TS 32.423 trace files</p>
</li>
</ul>
</div>
<div class="paragraph">
<p>There is no need to tell <strong>Wireshark</strong> what type of
file you are reading; it will determine the file type by itself.
<strong>Wireshark</strong> is also capable of reading any of these file formats if they
are compressed using gzip.  <strong>Wireshark</strong> recognizes this directly from
the file; the '.gz' extension is not required for this purpose.</p>
</div>
<div class="paragraph">
<p>Like other protocol analyzers, <strong>Wireshark</strong>'s main window shows 3 views
of a packet.  It shows a summary line, briefly describing what the
packet is.  A packet details display is shown, allowing you to drill
down to exact protocol or field that you interested in.  Finally, a hex
dump shows you exactly what the packet looks like when it goes over the
wire.</p>
</div>
<div class="paragraph">
<p>In addition, <strong>Wireshark</strong> has some features that make it unique.  It can
assemble all the packets in a TCP conversation and show you the ASCII
(or EBCDIC, or hex) data in that conversation.  Display filters in
<strong>Wireshark</strong> are very powerful; more fields are filterable in <strong>Wireshark</strong>
than in other protocol analyzers, and the syntax you can use to create
your filters is richer.  As <strong>Wireshark</strong> progresses, expect more and more
protocol fields to be allowed in display filters.</p>
</div>
<div class="paragraph">
<p>Packet capturing is performed with the pcap library.  The capture filter
syntax follows the rules of the pcap library.  This syntax is different
from the display filter syntax.</p>
</div>
<div class="paragraph">
<p>Compressed file support uses (and therefore requires) the zlib library.
If the zlib library is not present, <strong>Wireshark</strong> will compile, but will
be unable to read compressed files.</p>
</div>
<div class="paragraph">
<p>The pathname of a capture file to be read can be specified with the
<strong>-r</strong> option or can be specified as a command-line argument.</p>
</div>
</div>
</div>
<div class="sect1">
<h2 id="_options">OPTIONS</h2>
<div class="sectionbody">
<div class="paragraph">
<p>Most users will want to start <strong>Wireshark</strong> without options and configure
it from the menus instead.  Those users may just skip this section.</p>
</div>
<div class="dlist">
<dl>
<dt class="hdlist1">-a|--autostop  &lt;capture autostop condition&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Specify a criterion that specifies when <strong>Wireshark</strong> is to stop writing
to a capture file.  The criterion is of the form <em>test:value</em>,
where <em>test</em> is one of:</p>
</div>
<div class="paragraph">
<p><strong>duration</strong>:<em>value</em> Stop writing to a capture file after <em>value</em> seconds have
elapsed. Floating point values (e.g. 0.5) are allowed.</p>
</div>
<div class="paragraph">
<p><strong>files</strong>:<em>value</em> Stop writing to capture files after <em>value</em> number of files
were written.</p>
</div>
<div class="paragraph">
<p><strong>filesize</strong>:<em>value</em> Stop writing to a capture file after it reaches a size of
<em>value</em> kB.  If this option is used together with the -b option, Wireshark
will stop writing to the current capture file and switch to the next one if
filesize is reached.  Note that the filesize is limited to a maximum value of
2 GiB.</p>
</div>
<div class="paragraph">
<p><strong>packets</strong>:<em>value</em> Stop writing to a capture file after it contains <em>value</em>
packets. Same as <strong>-c</strong>&lt;capture packet count&gt;.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-b|--ring-buffer  &lt;capture ring buffer option&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Cause <strong>Wireshark</strong> to run in "multiple files" mode.  In "multiple files" mode,
<strong>Wireshark</strong> will write to several capture files.  When the first capture file
fills up, <strong>Wireshark</strong> will switch writing to the next file and so on.</p>
</div>
<div class="paragraph">
<p>The created filenames are based on the filename given with the <strong>-w</strong> flag,
the number of the file and on the creation date and time,
e.g. outfile_00001_20220714120117.pcap, outfile_00002_20220714120523.pcap, …​</p>
</div>
<div class="paragraph">
<p>With the <em>files</em> option it’s also possible to form a "ring buffer".
This will fill up new files until the number of files specified,
at which point <strong>Wireshark</strong> will discard the data in the first file and start
writing to that file and so on.  If the <em>files</em> option is not set,
new files filled up until one of the capture stop conditions match (or
until the disk is full).</p>
</div>
<div class="paragraph">
<p>The criterion is of the form <em>key:value</em>,
where <em>key</em> is one of:</p>
</div>
<div class="paragraph">
<p><strong>duration</strong>:<em>value</em> switch to the next file after <em>value</em> seconds have
elapsed, even if the current file is not completely filled up. Floating
point values (e.g. 0.5) are allowed.</p>
</div>
<div class="paragraph">
<p><strong>files</strong>:<em>value</em> begin again with the first file after <em>value</em> number of
files were written (form a ring buffer).  This value must be less than 100000.
Caution should be used when using large numbers of files: some filesystems do
not handle many files in a single directory well.  The <strong>files</strong> criterion
requires one of the other criteria to be specified to
control when to go to the next file.  It should be noted that each <strong>-b</strong>
parameter takes exactly one criterion; to specify two criteria, each must be
preceded by the <strong>-b</strong> option.</p>
</div>
<div class="paragraph">
<p><strong>filesize</strong>:<em>value</em> switch to the next file after it reaches a size of
<em>value</em> kB.  Note that the filesize is limited to a maximum value of 2 GiB.</p>
</div>
<div class="paragraph">
<p><strong>interval</strong>:<em>value</em> switch to the next file when the time is an exact
multiple of <em>value</em> seconds.</p>
</div>
<div class="paragraph">
<p><strong>packets</strong>:<em>value</em> switch to the next file after it contains <em>value</em>
packets.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-b filesize:1000 -b files:5</strong> results in a ring buffer of five files
of size one megabyte each.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-B|--buffer-size  &lt;capture buffer size&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Set capture buffer size (in MiB, default is 2 MiB).  This is used by
the capture driver to buffer packet data until that data can be written
to disk.  If you encounter packet drops while capturing, try to increase
this size.  Note that, while <strong>Wireshark</strong> attempts to set the buffer size
to 2 MiB by default, and can be told to set it to a larger value, the
system or interface on which you’re capturing might silently limit the
capture buffer size to a lower value or raise it to a higher value.</p>
</div>
<div class="paragraph">
<p>This is available on UNIX systems with libpcap 1.0.0 or later and on
Windows.  It is not available on UNIX systems with earlier versions of
libpcap.</p>
</div>
<div class="paragraph">
<p>This option can occur multiple times.  If used before the first
occurrence of the <strong>-i</strong> option, it sets the default capture buffer size.
If used after an <strong>-i</strong> option, it sets the capture buffer size for
the interface specified by the last <strong>-i</strong> option occurring before
this option.  If the capture buffer size is not set specifically,
the default capture buffer size is used instead.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-c  &lt;capture packet count&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Set the maximum number of packets to read when capturing live
data. Same as <strong>-a packets:</strong>&lt;capture packet count&gt;.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-C  &lt;configuration profile&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Start with the given configuration profile.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">--capture-comment &lt;comment&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>When performing a capture file from the command line, with the <strong>-k</strong>
flag, add a capture comment to the output file, if supported by the
capture format.</p>
</div>
<div class="paragraph">
<p>This option may be specified multiple times.  Note that Wireshark
currently only displays the first comment of a capture file.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-d  &lt;layer type&gt;==&lt;selector&gt;,&lt;decode-as protocol&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Like Wireshark’s <strong>Decode As…​</strong> feature, this lets you specify how a
layer type should be dissected.  If the layer type in question (for example,
<strong>tcp.port</strong> or <strong>udp.port</strong> for a TCP or UDP port number) has the specified
selector value, packets should be dissected as the specified protocol.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-d tcp.port==8888,http</strong> will decode any traffic running over
TCP port 8888 as HTTP.</p>
</div>
<div class="paragraph">
<p>See the <a href="file:///usr/share/wireshark/tshark.html">tshark</a>(1) manual page for more examples.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-D|--list-interfaces</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Print a list of the interfaces on which <strong>Wireshark</strong> can capture, and
exit.  For each network interface, a number and an
interface name, possibly followed by a text description of the
interface, is printed.  The interface name or the number can be supplied
to the <strong>-i</strong> flag to specify an interface on which to capture.</p>
</div>
<div class="paragraph">
<p>This can be useful on systems that don’t have a command to list them
(UNIX systems lacking <strong>ifconfig -a</strong> or Linux systems lacking
<strong>ip link show</strong>). The number can be useful on Windows systems, where
the interface name might be a long name or a GUID.</p>
</div>
<div class="paragraph">
<p>Note that "can capture" means that <strong>Wireshark</strong> was able to open
that device to do a live capture; if, on your system, a program doing a
network capture must be run from an account with special privileges (for
example, as root), then, if <strong>Wireshark</strong> is run with the <strong>-D</strong> flag and
is not run from such an account, it will not list any interfaces.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">--display &lt;X display to use&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Specifies the X display to use.  A hostname and screen (otherhost:0.0)
or just a screen (:0.0) can be specified.  This option is not available
under Windows.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">--disable-protocol &lt;proto_name&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Disable dissection of proto_name.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">--disable-heuristic &lt;short_name&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Disable dissection of heuristic protocol.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">--enable-protocol &lt;proto_name&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Enable dissection of proto_name.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">--enable-heuristic &lt;short_name&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Enable dissection of heuristic protocol.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-f  &lt;capture filter&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Set the capture filter expression.</p>
</div>
<div class="paragraph">
<p>This option can occur multiple times.  If used before the first
occurrence of the <strong>-i</strong> option, it sets the default capture filter expression.
If used after an <strong>-i</strong> option, it sets the capture filter expression for
the interface specified by the last <strong>-i</strong> option occurring before
this option.  If the capture filter expression is not set specifically,
the default capture filter expression is used if provided.</p>
</div>
<div class="paragraph">
<p>Pre-defined capture filter names, as shown in the GUI menu item Capture→Capture Filters,
can be used by prefixing the argument with "predef:".
Example: <strong>-f "predef:MyPredefinedHostOnlyFilter"</strong></p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">--fullscreen</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Start Wireshark in full screen mode (kiosk mode). To exit from fullscreen mode,
open the View menu and select the Full Screen option. Alternatively, press the
F11 key (or Ctrl + Cmd + F for macOS).</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-g  &lt;packet number&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>After reading in a capture file using the <strong>-r</strong> flag, go to the given <em>packet number</em>.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-h|--help</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Print the version number and options and exit.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-H</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Hide the capture info dialog during live packet capture.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-i|--interface  &lt;capture interface&gt;|-</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Set the name of the network interface or pipe to use for live packet
capture.</p>
</div>
<div class="paragraph">
<p>Network interface names should match one of the names listed in
"<strong>wireshark -D</strong>" (described above); a number, as reported by
"<strong>wireshark -D</strong>", can also be used.  If you’re using UNIX, "<strong>netstat
 -i</strong>", "<strong>ifconfig -a</strong>" or "<strong>ip link</strong>" might also work to list interface names,
although not all versions of UNIX support the <strong>-a</strong> option to <strong>ifconfig</strong>.</p>
</div>
<div class="paragraph">
<p>If no interface is specified, <strong>Wireshark</strong> searches the list of
interfaces, choosing the first non-loopback interface if there are any
non-loopback interfaces, and choosing the first loopback interface if
there are no non-loopback interfaces.  If there are no interfaces at all,
<strong>Wireshark</strong> reports an error and doesn’t start the capture.</p>
</div>
<div class="paragraph">
<p>Pipe names should be either the name of a FIFO (named pipe) or "-" to
read data from the standard input.  On Windows systems, pipe names must be
of the form "\\pipe\.*pipename*".  Data read from pipes must be in
standard pcapng or pcap format. Pcapng data must have the same
endianness as the capturing host.</p>
</div>
<div class="paragraph">
<p>"TCP@&lt;host&gt;:&lt;port&gt;" causes <strong>Wireshark</strong> to attempt to connect to the
specified port on the specified host and read pcapng or pcap data.</p>
</div>
<div class="paragraph">
<p>This option can occur multiple times. When capturing from multiple
interfaces, the capture file will be saved in pcapng format.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-I|--monitor-mode</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Put the interface in "monitor mode"; this is supported only on IEEE
802.11 Wi-Fi interfaces, and supported only on some operating systems.</p>
</div>
<div class="paragraph">
<p>Note that in monitor mode the adapter might disassociate from the
network with which it’s associated, so that you will not be able to use
any wireless networks with that adapter.  This could prevent accessing
files on a network server, or resolving host names or network addresses,
if you are capturing in monitor mode and are not connected to another
network with another adapter.</p>
</div>
<div class="paragraph">
<p>This option can occur multiple times.  If used before the first
occurrence of the <strong>-i</strong> option, it enables the monitor mode for all interfaces.
If used after an <strong>-i</strong> option, it enables the monitor mode for
the interface specified by the last <strong>-i</strong> option occurring before
this option.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-j</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Use after <strong>-J</strong> to change the behavior when no exact match is found for
the filter.  With this option select the first packet before.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-J  &lt;jump filter&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>After reading in a capture file using the <strong>-r</strong> flag, jump to the packet
matching the filter (display filter syntax).  If no exact match is found
the first packet after that is selected.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-k</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Start the capture session immediately.  If the <strong>-i</strong> flag was
specified, the capture uses the specified interface.  Otherwise,
<strong>Wireshark</strong> searches the list of interfaces, choosing the first
non-loopback interface if there are any non-loopback interfaces, and
choosing the first loopback interface if there are no non-loopback
interfaces; if there are no interfaces, <strong>Wireshark</strong> reports an error and
doesn’t start the capture.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-K  &lt;keytab&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Load kerberos crypto keys from the specified keytab file.
This option can be used multiple times to load keys from several files.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-K krb5.keytab</strong></p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-l</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Turn on automatic scrolling if the packet display is being updated
automatically as packets arrive during a capture (as specified by the
<strong>-S</strong> flag).</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-L|--list-data-link-types</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>List the data link types supported by the interface and exit.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">--list-time-stamp-types</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>List time stamp types supported for the interface. If no time stamp type can be
set, no time stamp types are listed.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-n</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Disable network object name resolution (such as hostname, TCP and UDP port
names), the <strong>-N</strong> flag might override this one.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-N  &lt;name resolving flags&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Turn on name resolving only for particular types of addresses and port
numbers, with name resolving for other types of addresses and port
numbers turned off.  This flag overrides <strong>-n</strong> if both <strong>-N</strong> and <strong>-n</strong> are
present.  If both <strong>-N</strong> and <strong>-n</strong> flags are not present, all name resolutions
are turned on.</p>
</div>
<div class="paragraph">
<p>The argument is a string that may contain the letters:</p>
</div>
<div class="paragraph">
<p><strong>m</strong> to enable MAC address resolution</p>
</div>
<div class="paragraph">
<p><strong>n</strong> to enable network address resolution</p>
</div>
<div class="paragraph">
<p><strong>N</strong> to enable using external resolvers (e.g., DNS) for network address
resolution</p>
</div>
<div class="paragraph">
<p><strong>t</strong> to enable transport-layer port number resolution</p>
</div>
<div class="paragraph">
<p><strong>d</strong> to enable resolution from captured DNS packets</p>
</div>
<div class="paragraph">
<p><strong>v</strong> to enable VLAN IDs to names resolution</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-o  &lt;preference/recent setting&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Set a preference or recent value, overriding the default value and any value
read from a preference/recent file.  The argument to the flag is a string of
the form <em>prefname:value</em>, where <em>prefname</em> is the name of the
preference/recent value (which is the same name that would appear in the
preference/recent file), and <em>value</em> is the value to which it should be set.
Since <strong>Ethereal</strong> 0.10.12, the recent settings replaces the formerly used
-B, -P and -T flags to manipulate the GUI dimensions.</p>
</div>
<div class="paragraph">
<p>If <em>prefname</em> is "uat", you can override settings in various user access
tables using the form uat*:*<em>uat filename</em>:<em>uat record</em>.  <em>uat filename</em>
must be the name of a UAT file, e.g. <em>user_dlts</em>.  <em>uat_record</em> must be in
the form of a valid record for that file, including quotes.  For instance, to
specify a user DLT from the command line, you would use</p>
</div>
<div class="literalblock">
<div class="content">
<pre>-o "uat:user_dlts:\"User 0 (DLT=147)\",\"cops\",\"0\",\"\",\"0\",\"\""</pre>
</div>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-p|--no-promiscuous-mode</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p><em>Don’t</em> put the interface into promiscuous mode.  Note that the
interface might be in promiscuous mode for some other reason; hence,
<strong>-p</strong> cannot be used to ensure that the only traffic that is captured is
traffic sent to or from the machine on which <strong>Wireshark</strong> is running,
broadcast traffic, and multicast traffic to addresses received by that
machine.</p>
</div>
<div class="paragraph">
<p>This option can occur multiple times.  If used before the first
occurrence of the <strong>-i</strong> option, no interface will be put into the
promiscuous mode.
If used after an <strong>-i</strong> option, the interface specified by the last <strong>-i</strong>
option occurring before this option will not be put into the
promiscuous mode.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-P &lt;path setting&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Special path settings usually detected automatically.  This is used for
special cases, e.g. starting Wireshark from a known location on an USB stick.</p>
</div>
<div class="paragraph">
<p>The criterion is of the form <em>key:path</em>, where <em>key</em> is one of:</p>
</div>
<div class="paragraph">
<p><strong>persconf</strong>:<em>path</em> path of personal configuration files, like the
preferences files.</p>
</div>
<div class="paragraph">
<p><strong>persdata</strong>:<em>path</em> path of personal data files, it’s the folder initially
opened.  After the very first initialization, the recent file will keep the
folder last used.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-r|--read-file  &lt;infile&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Read packet data from <em>infile</em>, can be any supported capture file format
(including gzipped files).  It’s not possible to use named pipes or stdin
here! To capture from a pipe or from stdin use <strong>-i -</strong></p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-R|--read-filter  &lt;read (display) filter&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>When reading a capture file specified with the <strong>-r</strong> flag, causes the
specified filter (which uses the syntax of display filters, rather than
that of capture filters) to be applied to all packets read from the
capture file; packets not matching the filter are discarded.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-s|--snapshot-length  &lt;capture snaplen&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Set the default snapshot length to use when capturing live data.
No more than <em>snaplen</em> bytes of each network packet will be read into
memory, or saved to disk.  A value of 0 specifies a snapshot length of
262144, so that the full packet is captured; this is the default.</p>
</div>
<div class="paragraph">
<p>This option can occur multiple times.  If used before the first
occurrence of the <strong>-i</strong> option, it sets the default snapshot length.
If used after an <strong>-i</strong> option, it sets the snapshot length for
the interface specified by the last <strong>-i</strong> option occurring before
this option.  If the snapshot length is not set specifically,
the default snapshot length is used if provided.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-S</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Automatically update the packet display as packets are coming in.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-t  a|ad|adoy|d|dd|e|r|u|ud|udoy</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Set the format of the packet timestamp displayed in the packet list
window.  The format can be one of:</p>
</div>
<div class="paragraph">
<p><strong>a</strong> absolute: The absolute time, as local time in your time zone,
is the actual time the packet was captured, with no date displayed</p>
</div>
<div class="paragraph">
<p><strong>ad</strong> absolute with date: The absolute date, displayed as YYYY-MM-DD,
and time, as local time in your time zone, is the actual time and date
the packet was captured</p>
</div>
<div class="paragraph">
<p><strong>adoy</strong> absolute with date using day of year: The absolute date,
displayed as YYYY/DOY, and time, as local time in your time zone,
is the actual time and date the packet was captured</p>
</div>
<div class="paragraph">
<p><strong>d</strong> delta: The delta time is the time since the previous packet was
captured</p>
</div>
<div class="paragraph">
<p><strong>dd</strong> delta_displayed: The delta_displayed time is the time since the
previous displayed packet was captured</p>
</div>
<div class="paragraph">
<p><strong>e</strong> epoch: The time in seconds since epoch (Jan 1, 1970 00:00:00)</p>
</div>
<div class="paragraph">
<p><strong>r</strong> relative: The relative time is the time elapsed between the first packet
and the current packet</p>
</div>
<div class="paragraph">
<p><strong>u</strong> UTC: The absolute time, as UTC, is the actual time the packet was
captured, with no date displayed</p>
</div>
<div class="paragraph">
<p><strong>ud</strong> UTC with date: The absolute date, displayed as YYYY-MM-DD,
and time, as UTC, is the actual time and date the packet was captured</p>
</div>
<div class="paragraph">
<p><strong>udoy</strong> UTC with date using day of year: The absolute date, displayed
as YYYY/DOY, and time, as UTC, is the actual time and date the packet
was captured</p>
</div>
<div class="paragraph">
<p>The default format is relative.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">--time-stamp-type &lt;type&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Change the interface’s timestamp method. See --list-time-stamp-types.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-u &lt;s|hms&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Output format of seconds (def: s: seconds)</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-v|--version</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Print the full version information and exit.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-w  &lt;outfile&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Set the default capture file name, or '-' for standard output.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-X &lt;eXtension options&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Specify an option to be passed to an <strong>Wireshark</strong> module.  The eXtension option
is in the form <em>extension_key:value</em>, where <em>extension_key</em> can be:</p>
</div>
<div class="paragraph">
<p><strong>lua_script</strong>:<em>lua_script_filename</em> tells <strong>Wireshark</strong> to load the given script in addition to the
default Lua scripts.</p>
</div>
<div class="paragraph">
<p><strong>lua_script</strong><em>num</em>:<em>argument</em> tells <strong>Wireshark</strong> to pass the given argument
to the lua script identified by 'num', which is the number indexed order of the 'lua_script' command.
For example, if only one script was loaded with '-X lua_script:my.lua', then '-X lua_script1:foo'
will pass the string 'foo' to the 'my.lua' script.  If two scripts were loaded, such as '-X lua_script:my.lua'
and '-X lua_script:other.lua' in that order, then a '-X lua_script2:bar' would pass the string 'bar' to the second lua
script, namely 'other.lua'.</p>
</div>
<div class="paragraph">
<p><strong>read_format</strong>:<em>file_format</em> tells <strong>Wireshark</strong> to use the given file format to read in the
file (the file given in the <strong>-r</strong> command option).</p>
</div>
<div class="paragraph">
<p><strong>stdin_descr</strong>:<em>description</em> tells <strong>Wireshark</strong> to use the given description when
capturing from standard input (<strong>-i -</strong>).</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-y|--linktype  &lt;capture link type&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>If a capture is started from the command line with <strong>-k</strong>, set the data
link type to use while capturing packets.  The values reported by <strong>-L</strong>
are the values that can be used.</p>
</div>
<div class="paragraph">
<p>This option can occur multiple times.  If used before the first
occurrence of the <strong>-i</strong> option, it sets the default capture link type.
If used after an <strong>-i</strong> option, it sets the capture link type for
the interface specified by the last <strong>-i</strong> option occurring before
this option.  If the capture link type is not set specifically,
the default capture link type is used if provided.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-Y|--display-filter  &lt;displaY filter&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Start with the given display filter.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">-z  &lt;statistics&gt;</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Get <strong>Wireshark</strong> to collect various types of statistics and display the result
in a window that updates in semi-real time.</p>
</div>
<div class="paragraph">
<p>Some of the currently implemented statistics are:</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z help</strong></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Display all possible values for <strong>-z</strong>.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> afp,srt[,<em>filter</em>]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Show Apple Filing Protocol service response time statistics.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> conv,<em>type</em>[,<em>filter</em>]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Create a table that lists all conversations that could be seen in the
capture.  <em>type</em> specifies the conversation endpoint types for which we
want to generate the statistics; currently the supported ones are:</p>
</div>
<div class="literalblock">
<div class="content">
<pre>"eth"   Ethernet addresses
"fc"    Fibre Channel addresses
"fddi"  FDDI addresses
"ip"    IPv4 addresses
"ipv6"  IPv6 addresses
"ipx"   IPX addresses
"tcp"   TCP/IP socket pairs   Both IPv4 and IPv6 are supported
"tr"    Token Ring addresses
"udp"   UDP/IP socket pairs   Both IPv4 and IPv6 are supported</pre>
</div>
</div>
<div class="paragraph">
<p>If the optional <em>filter</em> is specified, only those packets that match the
filter will be used in the calculations.</p>
</div>
<div class="paragraph">
<p>The table is presented with one line for each conversation and displays
the number of packets/bytes in each direction as well as the total
number of packets/bytes.  By default, the table is sorted according to
the total number of packets.</p>
</div>
<div class="paragraph">
<p>These tables can also be generated at runtime by selecting the appropriate
conversation type from the menu "Tools/Statistics/Conversation List/".</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> dcerpc,srt,<em>name-or-uuid</em>,<em>major</em>.<em>minor</em>[,<em>filter</em>]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Collect call/reply SRT (Service Response Time) data for DCERPC interface
<em>name</em> or <em>uuid</em>, version <em>major</em>.<em>minor</em>.
Data collected is the number of calls for each procedure, MinSRT, MaxSRT
and AvgSRT.
Interface <em>name</em> and <em>uuid</em> are case-insensitive.</p>
</div>
<div class="paragraph">
<p>Example: <span class="nowrap"><strong>-z dcerpc,srt,12345778-1234-abcd-ef00-0123456789ac,1.0</strong></span> will collect data for the CIFS SAMR Interface.</p>
</div>
<div class="paragraph">
<p>This option can be used multiple times on the command line.</p>
</div>
<div class="paragraph">
<p>If the optional <em>filter</em>  is provided, the stats will only be calculated
on those calls that match that filter.</p>
</div>
<div class="paragraph">
<p>Example: <span class="nowrap"><strong>-z dcerpc,srt,12345778-1234-abcd-ef00-0123456789ac,1.0,ip.addr==1.2.3.4</strong></span> will collect SAMR
SRT statistics for a specific host.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> dhcp,stat[,<em>filter</em>]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Show DHCP (BOOTP) statistics.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> expert</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Show expert information.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> fc,srt[,<em>filter</em>]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Collect call/reply SRT (Service Response Time) data for FC.  Data collected
is the number of calls for each Fibre Channel command, MinSRT, MaxSRT and AvgSRT.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z fc,srt</strong>
will calculate the Service Response Time as the time delta between the
First packet of the exchange and the Last packet of the exchange.</p>
</div>
<div class="paragraph">
<p>The data will be presented as separate tables for all normal FC commands,
Only those commands that are seen in the capture will have its stats
displayed.</p>
</div>
<div class="paragraph">
<p>This option can be used multiple times on the command line.</p>
</div>
<div class="paragraph">
<p>If the optional <em>filter</em> is provided, the stats will only be calculated
on those calls that match that filter.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z "fc,srt,fc.id==01.02.03"</strong> will collect stats only for
FC packets exchanged by the host at FC address 01.02.03 .</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> h225,counter[<em>,filter</em>]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Count ITU-T H.225 messages and their reasons.  In the first column you get a
list of H.225 messages and H.225 message reasons which occur in the current
capture file.  The number of occurrences of each message or reason is displayed
in the second column.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z h225,counter</strong></p>
</div>
<div class="paragraph">
<p>This option can be used multiple times on the command line.</p>
</div>
<div class="paragraph">
<p>If the optional <em>filter</em> is provided, the stats will only be calculated
on those calls that match that filter.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z "h225,counter,ip.addr==1.2.3.4"</strong> will collect stats only for
H.225 packets exchanged by the host at IP address 1.2.3.4 .</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> h225,srt[<em>,filter</em>]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Collect request/response SRT (Service Response Time) data for ITU-T H.225 RAS.
Data collected is the number of calls of each ITU-T H.225 RAS Message Type,
Minimum SRT, Maximum SRT, Average SRT, Minimum in Packet, and Maximum in Packet.
You will also get the number of Open Requests (Unresponded Requests),
Discarded Responses (Responses without matching request) and Duplicate Messages.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z h225,srt</strong></p>
</div>
<div class="paragraph">
<p>This option can be used multiple times on the command line.</p>
</div>
<div class="paragraph">
<p>If the optional <em>filter</em> is provided, the stats will only be calculated
on those calls that match that filter.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z "h225,srt,ip.addr==1.2.3.4"</strong> will collect stats only for
ITU-T H.225 RAS packets exchanged by the host at IP address 1.2.3.4 .</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> io,stat</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Collect packet/bytes statistics for the capture in intervals of 1 second.
This option will open a window with up to 5 color-coded graphs where
number-of-packets-per-second or number-of-bytes-per-second statistics
can be calculated and displayed.</p>
</div>
<div class="paragraph">
<p>This option can be used multiple times on the command line.</p>
</div>
<div class="paragraph">
<p>This graph window can also be opened from the Analyze:Statistics:Traffic:IO-Stat
menu item.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> ldap,srt[,<em>filter</em>]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Collect call/reply SRT (Service Response Time) data for LDAP.  Data collected
is the number of calls for each implemented LDAP command, MinSRT, MaxSRT and AvgSRT.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z ldap,srt</strong>
will calculate the Service Response Time as the time delta between the
Request and the Response.</p>
</div>
<div class="paragraph">
<p>The data will be presented as separate tables for all implemented LDAP commands,
Only those commands that are seen in the capture will have its stats
displayed.</p>
</div>
<div class="paragraph">
<p>This option can be used multiple times on the command line.</p>
</div>
<div class="paragraph">
<p>If the optional <em>filter</em> is provided, the stats will only be calculated
on those calls that match that filter.</p>
</div>
<div class="paragraph">
<p>Example: use <strong>-z "ldap,srt,ip.addr==10.1.1.1"</strong> will collect stats only for
LDAP packets exchanged by the host at IP address 10.1.1.1 .</p>
</div>
<div class="paragraph">
<p>The only LDAP commands that are currently implemented and for which the stats will be available are:
BIND
SEARCH
MODIFY
ADD
DELETE
MODRDN
COMPARE
EXTENDED</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> megaco,srt[<em>,filter</em>]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Collect request/response SRT (Service Response Time) data for MEGACO.
(This is similar to <strong>-z smb,srt</strong>).  Data collected is the number of calls
for each known MEGACO Command, Minimum SRT, Maximum SRT and Average SRT.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z megaco,srt</strong></p>
</div>
<div class="paragraph">
<p>This option can be used multiple times on the command line.</p>
</div>
<div class="paragraph">
<p>If the optional <em>filter</em> is provided, the stats will only be calculated
on those calls that match that filter.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z "megaco,srt,ip.addr==1.2.3.4"</strong> will collect stats only for
MEGACO packets exchanged by the host at IP address 1.2.3.4 .</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> mgcp,srt[<em>,filter</em>]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Collect request/response SRT (Service Response Time) data for MGCP.
(This is similar to <strong>-z smb,srt</strong>).  Data collected is the number of calls
for each known MGCP Type, Minimum SRT, Maximum SRT and Average SRT.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z mgcp,srt</strong></p>
</div>
<div class="paragraph">
<p>This option can be used multiple times on the command line.</p>
</div>
<div class="paragraph">
<p>If the optional <em>filter</em> is provided, the stats will only be calculated
on those calls that match that filter.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z "mgcp,srt,ip.addr==1.2.3.4"</strong> will collect stats only for
MGCP packets exchanged by the host at IP address 1.2.3.4 .</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> mtp3,msus[,&lt;filter&gt;]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Show MTP3 MSU statistics.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> multicast,stat[,&lt;filter&gt;]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Show UDP multicast stream statistics.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> rpc,programs</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Collect call/reply SRT data for all known ONC-RPC programs/versions.
Data collected is the number of calls for each protocol/version, MinSRT,
MaxSRT and AvgSRT.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> rpc,srt,<em>name-or-number</em>,<em>version</em>[,&lt;filter&gt;]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Collect call/reply SRT (Service Response Time) data for program
<em>name</em>/<em>version</em> or <em>number</em>/<em>version</em>.
Data collected is the number of calls for each procedure, MinSRT, MaxSRT and
AvgSRT.
Program <em>name</em> is case-insensitive.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z rpc,srt,100003,3</strong> will collect data for NFS v3.</p>
</div>
<div class="paragraph">
<p>This option can be used multiple times on the command line.</p>
</div>
<div class="paragraph">
<p>If the optional <em>filter</em> is provided, the stats will only be calculated
on those calls that match that filter.</p>
</div>
<div class="paragraph">
<p>Example: <span class="nowrap"><strong>-z rpc,srt,nfs,3,nfs.fh.hash==0x12345678</strong></span> will collect NFS v3
SRT statistics for a specific file.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> scsi,srt,<em>cmdset</em>[,&lt;filter&gt;]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Collect call/reply SRT (Service Response Time) data for SCSI commandset &lt;cmdset&gt;.</p>
</div>
<div class="paragraph">
<p>Commandsets are 0:SBC   1:SSC  5:MMC</p>
</div>
<div class="paragraph">
<p>Data collected
is the number of calls for each procedure, MinSRT, MaxSRT and AvgSRT.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z scsi,srt,0</strong> will collect data for SCSI BLOCK COMMANDS (SBC).</p>
</div>
<div class="paragraph">
<p>This option can be used multiple times on the command line.</p>
</div>
<div class="paragraph">
<p>If the optional <em>filter</em> is provided, the stats will only be calculated
on those calls that match that filter.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z scsi,srt,0,ip.addr==1.2.3.4</strong> will collect SCSI SBC
SRT statistics for a specific iscsi/ifcp/fcip host.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> sip,stat[<em>,filter</em>]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This option will activate a counter for SIP messages.  You will get the number
of occurrences of each SIP Method and of each SIP Status-Code.  Additionally you
also get the number of resent SIP Messages (only for SIP over UDP).</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z sip,stat</strong></p>
</div>
<div class="paragraph">
<p>This option can be used multiple times on the command line.</p>
</div>
<div class="paragraph">
<p>If the optional <em>filter</em> is provided, the stats will only be calculated
on those calls that match that filter.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z "sip,stat,ip.addr==1.2.3.4"</strong> will collect stats only for
SIP packets exchanged by the host at IP address 1.2.3.4 .</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> smb,srt[,<em>filter</em>]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Collect call/reply SRT (Service Response Time) data for SMB.  Data collected
is the number of calls for each SMB command, MinSRT, MaxSRT and AvgSRT.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z smb,srt</strong></p>
</div>
<div class="paragraph">
<p>The data will be presented as separate tables for all normal SMB commands,
all Transaction2 commands and all NT Transaction commands.
Only those commands that are seen in the capture will have their stats
displayed.
Only the first command in a xAndX command chain will be used in the
calculation.  So for common SessionSetupAndX + TreeConnectAndX chains,
only the SessionSetupAndX call will be used in the statistics.
This is a flaw that might be fixed in the future.</p>
</div>
<div class="paragraph">
<p>This option can be used multiple times on the command line.</p>
</div>
<div class="paragraph">
<p>If the optional <em>filter</em> is provided, the stats will only be calculated
on those calls that match that filter.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z "smb,srt,ip.addr==1.2.3.4"</strong> will collect stats only for
SMB packets exchanged by the host at IP address 1.2.3.4 .</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> voip,calls</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This option will show a window that shows VoIP calls found in the capture file.
This is the same window shown as when you go to the Statistics Menu and choose
VoIP Calls.</p>
</div>
<div class="paragraph">
<p>Example: <strong>-z voip,calls</strong></p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> wlan,stat[,&lt;filter&gt;]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Show IEEE 802.11 network and station statistics.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><strong>-z</strong> wsp,stat[,&lt;filter&gt;]</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Show WSP packet counters.</p>
</div>
</div>
</div>
</dd>
</dl>
</div>
</div>
</div>
<div class="sect1">
<h2 id="_interface">INTERFACE</h2>
<div class="sectionbody">
<div class="sect2">
<h3 id="_menu_items">MENU ITEMS</h3>
<div class="dlist">
<dl>
<dt class="hdlist1"><span class="menuseq"><b class="menu">File</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Open</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">File</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Open Recent</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">File</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Merge</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Merge another capture file to the currently loaded one.  The <em>File:Merge</em>
dialog box allows the merge "Prepended", "Chronologically" or "Appended",
relative to the already loaded one.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">File</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Close</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Open or close a capture file.  The <em>File:Open</em> dialog box
allows a filter to be specified; when the capture file is read, the
filter is applied to all packets read from the file, and packets not
matching the filter are discarded.  The <em>File:Open Recent</em> is a submenu
and will show a list of previously opened files.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">File</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Save</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">File</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Save As</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Save the current capture, or the packets currently displayed from that
capture, to a file.  Check boxes let you select whether to save all
packets, or just those that have passed the current display filter and/or
those that are currently marked, and an option menu lets you select (from
a list of file formats in which at particular capture, or the packets
currently displayed from that capture, can be saved), a file format in
which to save it.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">File</b>&nbsp;<b class="caret">›</b> <b class="submenu">File Set</b>&nbsp;<b class="caret">›</b> <b class="menuitem">List Files</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Show a dialog box that lists all files of the file set matching the currently
loaded file.  A file set is a compound of files resulting from a capture using
the "multiple files" / "ringbuffer" mode, recognizable by the filename pattern,
e.g.: Filename_00001_20220714101530.pcap.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">File</b>&nbsp;<b class="caret">›</b> <b class="submenu">File Set</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Next File</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">File</b>&nbsp;<b class="caret">›</b> <b class="submenu">File Set</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Previous File</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>If the currently loaded file is part of a file set (see above), open the
next / previous file in that set.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">File</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Export</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Export captured data into an external format.  Note: the data cannot be
imported back into Wireshark, so be sure to keep the capture file.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">File</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Print</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Print packet data from the current capture.  You can select the range of
packets to be printed (which packets are printed), and the output format of
each packet (how each packet is printed).  The output format will be similar
to the displayed values, so a summary line, the packet details view, and/or
the hex dump of the packet can be printed.</p>
</div>
<div class="paragraph">
<p>Printing options can be set with the <em>Edit:Preferences</em> menu item, or in the
dialog box popped up by this menu item.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">File</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Quit</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Exit the application.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="submenu">Copy</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Description</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Copies the description of the selected field in the protocol tree to
the clipboard.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="submenu">Copy</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Fieldname</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Copies the fieldname of the selected field in the protocol tree to
the clipboard.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="submenu">Copy</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Value</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Copies the value of the selected field in the protocol tree to
the clipboard.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="submenu">Copy</b>&nbsp;<b class="caret">›</b> <b class="menuitem">As Filter</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Create a display filter based on the data currently highlighted in the
packet details and copy that filter to the clipboard.</p>
</div>
<div class="paragraph">
<p>If that data is a field that can be tested in a display filter
expression, the display filter will test that field; otherwise, the
display filter will be based on the absolute offset within the packet.
Therefore it could be unreliable if the packet contains protocols with
variable-length headers, such as a source-routed token-ring packet.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Find Packet</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Search forward or backward, starting with the currently selected packet
(or the most recently selected packet, if no packet is selected).  Search
criteria can be a display filter expression, a string of hexadecimal
digits, or a text string.</p>
</div>
<div class="paragraph">
<p>When searching for a text string, you can search the packet data, or you
can search the text in the Info column in the packet list pane or in the
packet details pane.</p>
</div>
<div class="paragraph">
<p>Hexadecimal digits can be separated by colons, periods, or dashes.
Text string searches can be ASCII or Unicode (or both), and may be
case insensitive.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Find Next</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Find Previous</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Search forward / backward for a packet matching the filter from the previous
search, starting with the currently selected packet (or the most recently
selected packet, if no packet is selected).</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Mark Packet (toggle)</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Mark (or unmark if currently marked) the selected packet.  The field
"frame.marked" is set for packets that are marked, so that, for example,
a display filters can be used to display only marked packets, and so that
the /"Edit:Find Packet" dialog can be used to find the next or previous
marked packet.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Find Next Mark</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Find Previous Mark</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Find next/previous marked packet.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Mark All Packets</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Unmark All Packets</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Mark / Unmark all packets that are currently displayed.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="submenu">Time Reference</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Set Time Reference (toggle)</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Set (or unset if currently set) the selected packet as a Time Reference packet.
When a packet is set as a Time Reference packet, the timestamps in the packet
list pane will be replaced with the string "<strong>REF</strong>".
The relative time timestamp in later packets will then be calculated relative
to the timestamp of this Time Reference packet and not the first packet in
the capture.</p>
</div>
<div class="paragraph">
<p>Packets that have been selected as Time Reference packets will always be
displayed in the packet list pane.  Display filters will not affect or
hide these packets.</p>
</div>
<div class="paragraph">
<p>If there is a column displayed for "Cumulative Bytes" this counter will
be reset at every Time Reference packet.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="submenu">Time Reference</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Find Next</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="submenu">Time Reference</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Find Previous</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Search forward / backward for a time referenced packet.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Configuration Profiles</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Manage configuration profiles to be able to use more than one set of
preferences and configurations.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Edit</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Preferences</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Set the GUI, capture, printing and protocol options
(see /Preferences dialog below).</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Main Toolbar</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Filter Toolbar</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Statusbar</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Show or hide the main window controls.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Packet List</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Packet Details</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Packet Bytes</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Show or hide the main window panes.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Time Display Format</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Set the format of the packet timestamp displayed in the packet list window.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="submenu">Name Resolution</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Resolve Name</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Try to resolve a name for the currently selected item.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="submenu">Name Resolution</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Enable for …​ Layer</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Enable or disable translation of addresses to names in the display.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Colorize Packet List</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Enable or disable the coloring rules.  Disabling will improve performance.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Auto Scroll in Live Capture</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Enable or disable the automatic scrolling of the
packet list while a live capture is in progress.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Zoom In</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Zoom Out</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Zoom into / out of the main window data (by changing the font size).</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Normal Size</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Reset the zoom factor of zoom in / zoom out back to normal font size.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Resize All Columns</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Resize all columns to best fit the current packet display.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Expand / Collapse Subtrees</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Expands / Collapses the currently selected item and it’s subtrees in the packet details.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Expand All</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Collapse All</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Expand / Collapse all branches of the packet details.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Colorize Conversation</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Select color for a conversation.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Reset Coloring 1-10</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Reset Color for a conversation.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Coloring Rules</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Change the foreground and background colors of the packet information in
the list of packets, based upon display filters.  The list of display
filters is applied to each packet sequentially.  After the first display
filter matches a packet, any additional display filters in the list are
ignored.  Therefore, if you are filtering on the existence of protocols,
you should list the higher-level protocols first, and the lower-level
protocols last.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">How Colorization Works</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Packets are colored according to a list of color filters.  Each filter
consists of a name, a filter expression and a coloration.  A packet is
colored according to the first filter that it matches.  Color filter
expressions use exactly the same syntax as display filter expressions.</p>
</div>
<div class="paragraph">
<p>When Wireshark starts, the color filters are loaded from:</p>
</div>
<div class="olist arabic">
<ol class="arabic">
<li>
<p>The user’s personal color filters file or, if that does not exist,</p>
</li>
<li>
<p>The global color filters file.</p>
</li>
</ol>
</div>
<div class="paragraph">
<p>If neither of these exist then the packets will not be colored.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Show Packet In New Window</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Create a new window containing a packet details view and a hex dump
window of the currently selected packet; this window will continue to
display that packet’s details and data even if another packet is
selected.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">View</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Reload</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Reload a capture file.  Same as <em>File:Close</em> and <em>File:Open</em> the same
file again.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Go</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Back</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Go back in previously visited packets history.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Go</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Forward</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Go forward in previously visited packets history.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Go</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Go To Packet</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Go to a particular numbered packet.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Go</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Go To Corresponding Packet</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>If a field in the packet details pane containing a packet number is
selected, go to the packet number specified by that field.  (This works
only if the dissector that put that entry into the packet details put it
into the details as a filterable field rather than just as text.) This
can be used, for example, to go to the packet for the request
corresponding to a reply, or the reply corresponding to a request, if
that packet number has been put into the packet details.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Go</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Previous Packet</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Go</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Next Packet</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Go</b>&nbsp;<b class="caret">›</b> <b class="menuitem">First Packet</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Go</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Last Packet</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Go to the previous / next / first / last packet in the capture.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Go</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Previous Packet In Conversation</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Go</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Next Packet In Conversation</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Go to the previous / next packet of the conversation (TCP, UDP or IP)</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Capture</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Interfaces</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Shows a dialog box with all currently known interfaces and displaying the
current network traffic amount.  Capture sessions can be started from here.
Beware: keeping this box open results in high system load!</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Capture</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Options</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Initiate a live packet capture (see /"Capture Options Dialog"
below).  If no filename is specified, a temporary file will be created
to hold the capture.  The location of the file can be chosen by setting your
TMPDIR environment variable before starting <strong>Wireshark</strong>.  Otherwise, the
default TMPDIR location is system-dependent, but is likely either <em>/var/tmp</em>
or <em>/tmp</em>.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Capture</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Start</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Start a live packet capture with the previously selected options.  This won’t
open the options dialog box, and can be convenient for repeatedly capturing
with the same options.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Capture</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Stop</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Stop a running live capture.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Capture</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Restart</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>While a live capture is running, stop it and restart with the same options
again.  This can be convenient to remove irrelevant packets, if no valuable
packets were captured so far.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Capture</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Capture Filters</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Edit the saved list of capture filters, allowing filters to be added,
changed, or deleted.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Analyze</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Display Filters</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Edit the saved list of display filters, allowing filters to be added,
changed, or deleted.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Analyze</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Display Filter Macros</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Create shortcuts for complex macros</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Analyze</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Apply as Filter</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Create a display filter based on the data currently highlighted in the
packet details and apply the filter.</p>
</div>
<div class="paragraph">
<p>If that data is a field that can be tested in a display filter
expression, the display filter will test that field; otherwise, the
display filter will be based on the absolute offset within the packet.
Therefore it could be unreliable if the packet contains protocols with
variable-length headers, such as a source-routed token-ring packet.</p>
</div>
<div class="paragraph">
<p>The <strong>Selected</strong> option creates a display filter that tests for a match
of the data; the <strong>Not Selected</strong> option creates a display filter that
tests for a non-match of the data.  The <strong>And Selected</strong>, <strong>Or Selected</strong>,
<strong>And Not Selected</strong>, and <strong>Or Not Selected</strong> options add to the end of
the display filter in the strip at the top (or bottom) an AND or OR
operator followed by the new display filter expression.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Analyze</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Prepare as Filter</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Create a display filter based on the data currently highlighted in the
packet details.  The filter strip at the top (or bottom) is updated but
it is not yet applied.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Analyze</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Enabled Protocols</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Allow protocol dissection to be enabled or disabled for a specific
protocol.  Individual protocols can be enabled or disabled by clicking
on them in the list or by highlighting them and pressing the space bar.
The entire list can be enabled, disabled, or inverted using the buttons
below the list.</p>
</div>
<div class="paragraph">
<p>When a protocol is disabled, dissection in a particular packet stops
when that protocol is reached, and Wireshark moves on to the next packet.
Any higher-layer protocols that would otherwise have been processed will
not be displayed.  For example, disabling TCP will prevent the dissection
and display of TCP, HTTP, SMTP, Telnet, and any other protocol exclusively
dependent on TCP.</p>
</div>
<div class="paragraph">
<p>The list of protocols can be saved, so that Wireshark will start up with
the protocols in that list disabled.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Analyze</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Decode As</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>If you have a packet selected, present a dialog allowing you to change
which dissectors are used to decode this packet.  The dialog has one
panel each for the link layer, network layer and transport layer
protocol/port numbers, and will allow each of these to be changed
independently.  For example, if the selected packet is a TCP packet to
port 12345, using this dialog you can instruct Wireshark to decode all
packets to or from that TCP port as HTTP packets.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Analyze</b>&nbsp;<b class="caret">›</b> <b class="menuitem">User Specified Decodes</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Create a new window showing whether any protocol ID to dissector
mappings have been changed by the user.  This window also allows the
user to reset all decodes to their default values.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Analyze</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Follow TCP Stream</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>If you have a TCP packet selected, display the contents of the data
stream for the TCP connection to which that packet belongs, as text, in
a separate window, and leave the list of packets in a filtered state,
with only those packets that are part of that TCP connection being
displayed.  You can revert to your old view by pressing ENTER in the
display filter text box, thereby invoking your old display filter (or
resetting it back to no display filter).</p>
</div>
<div class="paragraph">
<p>The window in which the data stream is displayed lets you select:</p>
</div>
<div class="ulist">
<ul>
<li>
<p>whether to display the entire conversation, or one or the other side of
it;</p>
</li>
<li>
<p>whether the data being displayed is to be treated as ASCII or EBCDIC
text or as raw hex data;</p>
</li>
</ul>
</div>
<div class="paragraph">
<p>and lets you print what’s currently being displayed, using the same
print options that are used for the <em>File:Print Packet</em> menu item, or
save it as text to a file.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Analyze</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Follow UDP Stream</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Analyze</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Follow TLS Stream</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>(Similar to Analyze:Follow TCP Stream)</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Analyze</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Expert Info</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Analyze</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Expert Info Composite</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>(Kind of) a log of anomalies found by Wireshark in a capture file.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Analyze</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Conversation Filter</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Summary</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Show summary information about the capture, including elapsed time,
packet counts, byte counts, and the like.  If a display filter is in
effect, summary information will be shown about the capture and about
the packets currently being displayed.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Protocol Hierarchy</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Show the number of packets, and the number of bytes in those packets,
for each protocol in the trace.  It organizes the protocols in the same
hierarchy in which they were found in the trace.  Besides counting the
packets in which the protocol exists, a count is also made for packets
in which the protocol is the last protocol in the stack.  These
last-protocol counts show you how many packets (and the byte count
associated with those packets) <strong>ended</strong> in a particular protocol.  In
the table, they are listed under "End Packets" and "End Bytes".</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Conversations</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Lists of conversations; selectable by protocol.  See Statistics:Conversation List below.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">End Points</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>List of End Point Addresses by protocol with packets/bytes/…​. counts.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Packet Lengths</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Grouped counts of packet lengths (0-19 bytes, 20-39 bytes, …​)</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">I/O Graphs</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Open a window where up to 5 graphs in different colors can be displayed
to indicate number of packets or number of bytes per second for all packets
matching the specified filter.
By default only one graph will be displayed showing number of packets per second.</p>
</div>
<div class="paragraph">
<p>The top part of the window contains the graphs and scales for the X and
Y axis.  If the graph is too long to fit inside the window there is a
horizontal scrollbar below the drawing area that can scroll the graphs
to the left or the right.  The horizontal axis displays the time into
the capture and the vertical axis will display the measured quantity at
that time.</p>
</div>
<div class="paragraph">
<p>Below the drawing area and the scrollbar are the controls.  On the
bottom left there will be five similar sets of controls to control each
individual graph such as "Display:&lt;button&gt;" which button will toggle
that individual graph on/off.  If &lt;button&gt; is ticked, the graph will be
displayed. "Color:&lt;color&gt;" which is just a button to show which color
will be used to draw that graph. Finally "Filter:&lt;filter-text&gt;" which
can be used to specify a display filter for that particular graph.</p>
</div>
<div class="paragraph">
<p>If filter-text is empty then all packets will be used to calculate the
quantity for that graph.  If filter-text is specified only those packets
that match that display filter will be considered in the calculation of
quantity.</p>
</div>
<div class="paragraph">
<p>To the right of the 5 graph controls there are four menus to control
global aspects of the draw area and graphs.  The "Unit:" menu is used to
control what to measure; "packets/tick", "bytes/tick" or "advanced…​"</p>
</div>
<div class="paragraph">
<p>packets/tick will measure the number of packets matching the (if
specified) display filter for the graph in each measurement interval.</p>
</div>
<div class="paragraph">
<p>bytes/tick will measure the total number of bytes in all packets matching
the (if specified) display filter for the graph in each measurement
interval.</p>
</div>
<div class="paragraph">
<p>advanced…​ see below</p>
</div>
<div class="paragraph">
<p>"Tick interval:" specifies what measurement intervals to use.  The
default is 1 second and means that the data will be counted over 1
second intervals.</p>
</div>
<div class="paragraph">
<p>"Pixels per tick:" specifies how many pixels wide each measurement
interval will be in the drawing area.  The default is 5 pixels per tick.</p>
</div>
<div class="paragraph">
<p>"Y-scale:" controls the max value for the y-axis.  Default value is
"auto" which means that <strong>Wireshark</strong> will try to adjust the maxvalue
automatically.</p>
</div>
<div class="paragraph">
<p>"advanced…​" If Unit:advanced…​  is selected the window will display
two more controls for each of the five graphs.  One control will be a
menu where the type of calculation can be selected from
SUM,COUNT,MAX,MIN,AVG and LOAD, and one control, textbox, where the name of a
single display filter field can be specified.</p>
</div>
<div class="paragraph">
<p>The following restrictions apply to type and field combinations:</p>
</div>
<div class="paragraph">
<p>SUM: available for all types of integers and will calculate the SUM of
all occurrences of this field in the measurement interval.  Note that
some field can occur multiple times in the same packet and then all
instances will be summed up.  Example: 'tcp.len' which will count the
amount of payload data transferred across TCP in each interval.</p>
</div>
<div class="paragraph">
<p>COUNT: available for all field types.  This will COUNT the number of times
certain field occurs in each interval.  Note that some fields
may occur multiple times in each packet and if that is the case
then each instance will be counted independently and COUNT
will be greater than the number of packets.</p>
</div>
<div class="paragraph">
<p>MAX: available for all integer and relative time fields.  This will calculate
the max seen integer/time value seen for the field during the interval.
Example: 'smb.time' which will plot the maximum SMB response time.</p>
</div>
<div class="paragraph">
<p>MIN: available for all integer and relative time fields.  This will calculate
the min seen integer/time value seen for the field during the interval.
Example: 'smb.time' which will plot the minimum SMB response time.</p>
</div>
<div class="paragraph">
<p>AVG: available for all integer and relative time fields.This will
calculate the average seen integer/time value seen for the field during
the interval.  Example: 'smb.time' which will plot the average SMB
response time.</p>
</div>
<div class="paragraph">
<p>LOAD: available only for relative time fields (response times).</p>
</div>
<div class="paragraph">
<p>Example of advanced:
Display how NFS response time MAX/MIN/AVG changes over time:</p>
</div>
<div class="paragraph">
<p>Set first graph to:</p>
</div>
<div class="literalblock">
<div class="content">
<pre>filter:nfs&amp;&amp;rpc.time
Calc:MAX rpc.time</pre>
</div>
</div>
<div class="paragraph">
<p>Set second graph to</p>
</div>
<div class="literalblock">
<div class="content">
<pre>filter:nfs&amp;&amp;rpc.time
Calc:AVG rpc.time</pre>
</div>
</div>
<div class="paragraph">
<p>Set third graph to</p>
</div>
<div class="literalblock">
<div class="content">
<pre>filter:nfs&amp;&amp;rpc.time
Calc:MIN rpc.time</pre>
</div>
</div>
<div class="paragraph">
<p>Example of advanced:
Display how the average packet size from host a.b.c.d changes over time.</p>
</div>
<div class="paragraph">
<p>Set first graph to</p>
</div>
<div class="literalblock">
<div class="content">
<pre>filter:ip.addr==a.b.c.d&amp;&amp;frame.pkt_len
Calc:AVG frame.pkt_len</pre>
</div>
</div>
<div class="paragraph">
<p>LOAD:
The LOAD io-stat type is very different from anything you have ever seen
before! While the response times themselves as plotted by MIN,MAX,AVG are
indications on the Server load (which affects the Server response time),
the LOAD measurement measures the Client LOAD.
What this measures is how much workload the client generates,
i.e. how fast will the client issue new commands when the previous ones
completed.
i.e. the level of concurrency the client can maintain.
The higher the number, the more and faster is the client issuing new
commands.  When the LOAD goes down, it may be due to client load making
the client slower in issuing new commands (there may be other reasons as
well, maybe the client just doesn’t have any commands it wants to issue
right then).</p>
</div>
<div class="paragraph">
<p>Load is measured in concurrency/number of overlapping i/o and the value
1000 means there is a constant load of one i/o.</p>
</div>
<div class="paragraph">
<p>In each tick interval the amount of overlap is measured.
See the graph below containing three commands:
Below the graph are the LOAD values for each interval that would be calculated.</p>
</div>
<div class="literalblock">
<div class="content">
<pre>|     |     |     |     |     |     |     |     |
|     |     |     |     |     |     |     |     |
|     |  o=====*  |     |     |     |     |     |
|     |     |     |     |     |     |     |     |
|  o========*     | o============*  |     |     |
|     |     |     |     |     |     |     |     |
--------------------------------------------------&gt; Time
 500   1500   500  750   1000   500    0     0</pre>
</div>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Conversation List</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This option will open a new window that displays a list of all
conversations between two endpoints.  The list has one row for each
unique conversation and displays total number of packets/bytes seen as
well as number of packets/bytes in each direction.</p>
</div>
<div class="paragraph">
<p>By default the list is sorted according to the number of packets but by
clicking on the column header; it is possible to re-sort the list in
ascending or descending order by any column.</p>
</div>
<div class="paragraph">
<p>By first selecting a conversation by clicking on it and then using the
right mouse button (on those platforms that have a right
mouse button) Wireshark will display a popup menu offering several different
filter operations to apply to the capture.</p>
</div>
<div class="paragraph">
<p>These statistics windows can also be invoked from the Wireshark command
line using the <strong>-z conv</strong> argument.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Service Response Time</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="ulist">
<ul>
<li>
<p>AFP</p>
</li>
<li>
<p>CAMEL</p>
</li>
<li>
<p>DCE-RPC</p>
</li>
</ul>
</div>
<div class="paragraph">
<p>Open a window to display Service Response Time statistics for an
arbitrary DCE-RPC program
interface and display <strong>Procedure</strong>, <strong>Number of Calls</strong>, <strong>Minimum SRT</strong>,
<strong>Maximum SRT</strong> and <strong>Average SRT</strong> for all procedures for that
program/version.  These windows opened will update in semi-real time to
reflect changes when doing live captures or when reading new capture
files into <strong>Wireshark</strong>.</p>
</div>
<div class="paragraph">
<p>This dialog will also allow an optional filter string to be used.
If an optional filter string is used only such DCE-RPC request/response pairs
that match that filter will be used to calculate the statistics.  If no filter
string is specified all request/response pairs will be used.</p>
</div>
<div class="ulist">
<ul>
<li>
<p>Diameter</p>
</li>
<li>
<p>Fibre Channel</p>
</li>
</ul>
</div>
<div class="paragraph">
<p>Open a window to display Service Response Time statistics for Fibre Channel
and display <strong>FC Type</strong>, <strong>Number of Calls</strong>, <strong>Minimum SRT</strong>,
<strong>Maximum SRT</strong> and <strong>Average SRT</strong> for all FC types.
These windows opened will update in semi-real time to
reflect changes when doing live captures or when reading new capture
files into <strong>Wireshark</strong>.
The Service Response Time is calculated as the time delta between the
First packet of the exchange and the Last packet of the exchange.</p>
</div>
<div class="paragraph">
<p>This dialog will also allow an optional filter string to be used.
If an optional filter string is used only such FC first/last exchange pairs
that match that filter will be used to calculate the statistics.  If no filter
string is specified all request/response pairs will be used.</p>
</div>
<div class="ulist">
<ul>
<li>
<p>GTP</p>
</li>
<li>
<p>H.225 RAS</p>
</li>
</ul>
</div>
<div class="paragraph">
<p>Collect requests/response SRT (Service Response Time) data for ITU-T H.225 RAS.
Data collected is <strong>number of calls</strong> for each known ITU-T H.225 RAS Message Type,
<strong>Minimum SRT</strong>, <strong>Maximum SRT</strong>, <strong>Average SRT</strong>, <strong>Minimum in Packet</strong>, and <strong>Maximum in Packet</strong>.
You will also get the number of <strong>Open Requests</strong> (Unresponded Requests),
<strong>Discarded Responses</strong> (Responses without matching request) and Duplicate Messages.
These windows opened will update in semi-real time to reflect changes when
doing live captures or when reading new capture files into <strong>Wireshark</strong>.</p>
</div>
<div class="paragraph">
<p>You can apply an optional filter string in a dialog box, before starting
the calculation.  The statistics will only be calculated
on those calls matching that filter.</p>
</div>
<div class="ulist">
<ul>
<li>
<p>LDAP</p>
</li>
<li>
<p>MEGACO</p>
</li>
<li>
<p>MGCP</p>
</li>
</ul>
</div>
<div class="paragraph">
<p>Collect requests/response SRT (Service Response Time) data for MGCP.
Data collected is <strong>number of calls</strong> for each known MGCP Type,
<strong>Minimum SRT</strong>, <strong>Maximum SRT</strong>, <strong>Average SRT</strong>, <strong>Minimum in Packet</strong>, and <strong>Maximum in Packet</strong>.
These windows opened will update in semi-real time to reflect changes when
doing live captures or when reading new capture files into <strong>Wireshark</strong>.</p>
</div>
<div class="paragraph">
<p>You can apply an optional filter string in a dialog box, before starting
the calculation.  The statistics will only be calculated
on those calls matching that filter.</p>
</div>
<div class="ulist">
<ul>
<li>
<p>NCP</p>
</li>
<li>
<p>ONC-RPC</p>
</li>
</ul>
</div>
<div class="paragraph">
<p>Open a window to display statistics for an arbitrary ONC-RPC program interface
and display <strong>Procedure</strong>, <strong>Number of Calls</strong>, <strong>Minimum SRT</strong>, <strong>Maximum SRT</strong> and <strong>Average SRT</strong> for all procedures for that program/version.
These windows opened will update in semi-real time to reflect changes when
doing live captures or when reading new capture files into <strong>Wireshark</strong>.</p>
</div>
<div class="paragraph">
<p>This dialog will also allow an optional filter string to be used.
If an optional filter string is used only such ONC-RPC request/response pairs
that match that filter will be used to calculate the statistics.  If no filter
string is specified all request/response pairs will be used.</p>
</div>
<div class="paragraph">
<p>By first selecting a conversation by clicking on it and then using the
right mouse button (on those platforms that have a right
mouse button) Wireshark will display a popup menu offering several different
filter operations to apply to the capture.</p>
</div>
<div class="ulist">
<ul>
<li>
<p>RADIUS</p>
</li>
<li>
<p>SCSI</p>
</li>
<li>
<p>SMB</p>
</li>
</ul>
</div>
<div class="paragraph">
<p>Collect call/reply SRT (Service Response Time) data for SMB.  Data collected
is the number of calls for each SMB command, MinSRT, MaxSRT and AvgSRT.</p>
</div>
<div class="paragraph">
<p>The data will be presented as separate tables for all normal SMB commands,
all Transaction2 commands and all NT Transaction commands.
Only those commands that are seen in the capture will have its stats
displayed.
Only the first command in a xAndX command chain will be used in the
calculation.  So for common SessionSetupAndX + TreeConnectAndX chains,
only the SessionSetupAndX call will be used in the statistics.
This is a flaw that might be fixed in the future.</p>
</div>
<div class="paragraph">
<p>You can apply an optional filter string in a dialog box, before starting
the calculation.  The stats will only be calculated
on those calls matching that filter.</p>
</div>
<div class="paragraph">
<p>By first selecting a conversation by clicking on it and then using the
right mouse button (on those platforms that have a right
mouse button) Wireshark will display a popup menu offering several different
filter operations to apply to the capture.</p>
</div>
<div class="ulist">
<ul>
<li>
<p>SMB2</p>
</li>
</ul>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">BOOTP-DHCP</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Compare</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Compare two Capture Files</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Flow Graph</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Flow Graph: General/TCP</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">HTTP</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>HTTP Load Distribution, Packet Counter &amp; Requests</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">IP Addresses</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Count/Rate/Percent by IP Address</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">IP Destinations</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Count/Rate/Percent by IP Address/protocol/port</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">IP Protocol Types</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Count/Rate/Percent by IP Protocol Types</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">ONC-RPC Programs</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This dialog will open a window showing aggregated SRT statistics for all
ONC-RPC Programs/versions that exist in the capture file.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">TCP Stream Graph</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Graphs: Round Trip; Throughput; Time-Sequence (Stevens); Time-Sequence (tcptrace)</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">UDP Multicast streams</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Multicast Streams Counts/Rates/…​ by Source/Destination Address/Port pairs</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Statistics</b>&nbsp;<b class="caret">›</b> <b class="menuitem">WLAN Traffic</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>WLAN Traffic Statistics</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Telephony</b>&nbsp;<b class="caret">›</b> <b class="menuitem">ITU-T H.225</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Count ITU-T H.225 messages and their reasons.  In the first column you get a
list of H.225 messages and H.225 message reasons, which occur in the current
capture file.  The number of occurrences of each message or reason will be displayed
in the second column.
This window opened will update in semi-real time to reflect changes when
doing live captures or when reading new capture files into <strong>Wireshark</strong>.</p>
</div>
<div class="paragraph">
<p>You can apply an optional filter string in a dialog box, before starting
the counter.  The statistics will only be calculated
on those calls matching that filter.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Telephony</b>&nbsp;<b class="caret">›</b> <b class="menuitem">SIP</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Activate a counter for SIP messages.  You will get the number of occurrences of each
SIP Method and of each SIP Status-Code.  Additionally you also get the number of
resent SIP Messages (only for SIP over UDP).</p>
</div>
<div class="paragraph">
<p>This window opened will update in semi-real time to reflect changes when
doing live captures or when reading new capture files into <strong>Wireshark</strong>.</p>
</div>
<div class="paragraph">
<p>You can apply an optional filter string in a dialog box, before starting
the counter.  The statistics will only be calculated
on those calls matching that filter.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Tools</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Firewall ACL Rules</b></span></dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Help</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Contents</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Some help texts.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Help</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Supported Protocols</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>List of supported protocols and display filter protocol fields.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Help</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Manual Pages</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Display locally installed HTML versions of these manual pages in a web browser.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Help</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Wireshark Online</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Various links to online resources to be open in a web browser, like
<a href="https://www.wireshark.org/" class="bare">https://www.wireshark.org</a>.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">Help</b>&nbsp;<b class="caret">›</b> <b class="menuitem">About Wireshark</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>See various information about Wireshark (see /About dialog below), like the
version, the folders used, the available plugins, …​</p>
</div>
</div>
</div>
</dd>
</dl>
</div>
</div>
<div class="sect2">
<h3 id="_windows">WINDOWS</h3>
<div class="dlist">
<dl>
<dt class="hdlist1">Main Window</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The main window contains the usual things like the menu, some toolbars, the
main area and a statusbar.  The main area is split into three panes, you can
resize each pane using a "thumb" at the right end of each divider line.</p>
</div>
<div class="paragraph">
<p>The main window is much more flexible than before.  The layout of the main
window can be customized by the <em>Layout</em> page in the dialog box popped
up by <em>Edit:Preferences</em>, the following will describe the layout with the
default settings.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Main Toolbar</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Some menu items are available for quick access here.  There is no way to
customize the items in the toolbar, however the toolbar can be hidden by
<em>View:Main Toolbar</em>.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Filter Toolbar</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>A display filter can be entered into the filter toolbar.
A filter for HTTP, HTTPS, and DNS traffic might look like this:</p>
</div>
<div class="literalblock">
<div class="content">
<pre>tcp.port in {80 443 53}</pre>
</div>
</div>
<div class="paragraph">
<p>Selecting the <em>Filter:</em> button lets you choose from a list of named
filters that you can optionally save.  Pressing the Return or Enter
keys, or selecting the <em>Apply</em> button, will cause the filter to be
applied to the current list of packets.  Selecting the <em>Reset</em> button
clears the display filter so that all packets are displayed (again).</p>
</div>
<div class="paragraph">
<p>There is no way to customize the items in the toolbar, however the toolbar
can be hidden by <em>View:Filter Toolbar</em>.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Packet List Pane</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The top pane contains the list of network packets that you can scroll
through and select.  By default, the packet number, packet timestamp,
source and destination addresses, protocol, and description are
displayed for each packet; the <em>Columns</em> page in the dialog box popped
up by <em>Edit:Preferences</em> lets you change this (although, unfortunately,
you currently have to save the preferences, and exit and restart
Wireshark, for those changes to take effect).</p>
</div>
<div class="paragraph">
<p>If you click on the heading for a column, the display will be sorted by
that column; clicking on the heading again will reverse the sort order
for that column.</p>
</div>
<div class="paragraph">
<p>An effort is made to display information as high up the protocol stack
as possible, e.g. IP addresses are displayed for IP packets, but the
MAC layer address is displayed for unknown packet types.</p>
</div>
<div class="paragraph">
<p>The right mouse button can be used to pop up a menu of operations.</p>
</div>
<div class="paragraph">
<p>The middle mouse button can be used to mark a packet.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Packet Details Pane</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The middle pane contains a display of the details of the
currently-selected packet.  The display shows each field and its value
in each protocol header in the stack.  The right mouse button can be
used to pop up a menu of operations.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Packet Bytes Pane</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The lowest pane contains a hex and ASCII dump of the actual packet data.
Selecting a field in the packet details highlights the corresponding
bytes in this section.</p>
</div>
<div class="paragraph">
<p>The right mouse button can be used to pop up a menu of operations.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Statusbar</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The statusbar is divided into three parts, on the left some context dependent
things are shown, like information about the loaded file, in the center the
number of packets are displayed, and on the right the current configuration
profile.</p>
</div>
<div class="paragraph">
<p>The statusbar can be hidden by <em>View:Statusbar</em>.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Preferences</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>Preferences</em> dialog lets you control various personal preferences
for the behavior of <strong>Wireshark</strong>.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">User Interface Preferences</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>User Interface</em> page is used to modify small aspects of the GUI to
your own personal taste:</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Selection Bars</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The selection bar in the packet list and packet details can have either
a "browse" or "select" behavior.  If the selection bar has a "browse"
behavior, the arrow keys will move an outline of the selection bar,
allowing you to browse the rest of the list or details without changing
the selection until you press the space bar.  If the selection bar has a
"select" behavior, the arrow keys will move the selection bar and change
the selection to the new item in the packet list or packet details.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Save Window Position</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>If this item is selected, the position of the main Wireshark window will
be saved when Wireshark exits, and used when Wireshark is started again.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Save Window Size</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>If this item is selected, the size of the main Wireshark window will
be saved when Wireshark exits, and used when Wireshark is started again.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Save Window Maximized state</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>If this item is selected the maximize state of the main Wireshark window
will be saved when Wireshark exists, and used when Wireshark is started again.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">File Open Dialog Behavior</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This item allows the user to select how Wireshark handles the listing
of the "File Open" Dialog when opening trace files.  "Remember Last
Directory" causes Wireshark to automatically position the dialog in the
directory of the most recently opened file, even between launches of Wireshark.
"Always Open in Directory" allows the user to define a persistent directory
that the dialog will always default to.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Directory</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Allows the user to specify a persistent File Open directory.  Trailing
slashes or backslashes will automatically be added.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">File Open Preview timeout</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This items allows the user to define how much time is spend reading the
capture file to present preview data in the File Open dialog.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Open Recent maximum list entries</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The File menu supports a recent file list.  This items allows the user to
specify how many files are kept track of in this list.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Ask for unsaved capture files</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>When closing a capture file or Wireshark itself if the file isn’t saved yet
the user is presented the option to save the file when this item is set.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Wrap during find</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This items determines the behavior when reaching the beginning or the end
of a capture file.  When set the search wraps around and continues, otherwise
it stops.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Settings dialogs show a save button</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This item determines if the various dialogs sport an explicit Save button
or that save is implicit in OK / Apply.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Web browser command</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This entry specifies the command line to launch a web browser.  It is used
to access online content, like the Wiki and user guide.  Use '%s' to place
the request URL in the command line.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Layout Preferences</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>Layout</em> page lets you specify the general layout of the main window.
You can choose from six different layouts and fill the three panes with the
contents you like.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Scrollbars</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The vertical scrollbars in the three panes can be set to be either on
the left or the right.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Alternating row colors</dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1">Hex Display</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The highlight method in the hex dump display for the selected protocol
item can be set to use either inverse video, or bold characters.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Toolbar style</dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1">Filter toolbar placement</dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1">Custom window title</dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1">Column Preferences</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>Columns</em> page lets you specify the number, title, and format
of each column in the packet list.</p>
</div>
<div class="paragraph">
<p>The <em>Column title</em> entry is used to specify the title of the column
displayed at the top of the packet list.  The type of data that the column
displays can be specified using the <em>Column format</em> option menu.
The row of buttons on the left perform the following actions:</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">New</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Adds a new column to the list.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Delete</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Deletes the currently selected list item.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Up / Down</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Moves the selected list item up or down one position.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Font Preferences</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>Font</em> page lets you select the font to be used for most text.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Color Preferences</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>Colors</em> page can be used to change the color of the text
displayed in the TCP stream window and for marked packets.  To change a color,
simply select an attribute from the "Set:" menu and use the color selector to
get the desired color.  The new text colors are displayed as a sample text.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Capture Preferences</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>Capture</em> page lets you specify various parameters for capturing
live packet data; these are used the first time a capture is started.</p>
</div>
<div class="paragraph">
<p>The <em>Interface:</em> combo box lets you specify the interface from which to
capture packet data, or the name of a FIFO from which to get the packet
data.</p>
</div>
<div class="paragraph">
<p>The <em>Data link type:</em> option menu lets you, for some interfaces, select
the data link header you want to see on the packets you capture.  For
example, in some OSes and with some versions of libpcap, you can choose,
on an 802.11 interface, whether the packets should appear as Ethernet
packets (with a fake Ethernet header) or as 802.11 packets.</p>
</div>
<div class="paragraph">
<p>The <em>Limit each packet to …​ bytes</em> check box lets you set the
snapshot length to use when capturing live data; turn on the check box,
and then set the number of bytes to use as the snapshot length.</p>
</div>
<div class="paragraph">
<p>The <em>Filter:</em> text entry lets you set a capture filter expression to be
used when capturing.</p>
</div>
<div class="paragraph">
<p>If any of the environment variables SSH_CONNECTION, SSH_CLIENT,
REMOTEHOST, DISPLAY, or SESSIONNAME are set, Wireshark will create a
default capture filter that excludes traffic from the hosts and ports
defined in those variables.</p>
</div>
<div class="paragraph">
<p>The <em>Capture packets in promiscuous mode</em> check box lets you specify
whether to put the interface in promiscuous mode when capturing.</p>
</div>
<div class="paragraph">
<p>The <em>Update list of packets in real time</em> check box lets you specify
that the display should be updated as packets are seen.</p>
</div>
<div class="paragraph">
<p>The <em>Automatic scrolling in live capture</em> check box lets you specify
whether, in an "Update list of packets in real time" capture, the packet
list pane should automatically scroll to show the most recently captured
packets.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Printing Preferences</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The radio buttons at the top of the <em>Printing</em> page allow you choose
between printing packets with the <em>File:Print Packet</em> menu item as text
or PostScript, and sending the output directly to a command or saving it
to a file.  The <em>Command:</em> text entry box, on UNIX-compatible systems,
is the command to send files to (usually <strong>lpr</strong>), and the <em>File:</em> entry
box lets you enter the name of the file you wish to save to.
Additionally, you can select the <em>File:</em> button to browse the file
system for a particular save file.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Name Resolution Preferences</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>Enable MAC name resolution</em>, <em>Enable network name resolution</em> and
<em>Enable transport name resolution</em> check boxes let you specify whether
MAC addresses, network addresses, and transport-layer port numbers
should be translated to names.</p>
</div>
<div class="paragraph">
<p>The <em>Enable concurrent DNS name resolution</em> allows Wireshark to send out
multiple name resolution requests and not wait for the result before
continuing dissection.  This speeds up dissection with network name
resolution but initially may miss resolutions.  The number of concurrent
requests can be set here as well.</p>
</div>
<div class="paragraph">
<p><em>SMI paths</em></p>
</div>
<div class="paragraph">
<p><em>SMI modules</em></p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">RTP Player Preferences</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This page allows you to select the number of channels visible in the
RTP player window.  It determines the height of the window, more channels
are possible and visible by means of a scroll bar.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Protocol Preferences</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>There are also pages for various protocols that Wireshark dissects,
controlling the way Wireshark handles those protocols.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Edit Capture Filter List</dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1">Edit Display Filter List</dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1">Capture Filter</dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1">Display Filter</dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1">Read Filter</dt>
<dd>
<div class="openblock">
<div class="content">

</div>
</div>
</dd>
<dt class="hdlist1">Search Filter</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>Edit Capture Filter List</em> dialog lets you create, modify, and
delete capture filters, and the <em>Edit Display Filter List</em> dialog lets
you create, modify, and delete display filters.</p>
</div>
<div class="paragraph">
<p>The <em>Capture Filter</em> dialog lets you do all of the editing operations
listed, and also lets you choose or construct a filter to be used when
capturing packets.</p>
</div>
<div class="paragraph">
<p>The <em>Display Filter</em> dialog lets you do all of the editing operations
listed, and also lets you choose or construct a filter to be used to
filter the current capture being viewed.</p>
</div>
<div class="paragraph">
<p>The <em>Read Filter</em> dialog lets you do all of the editing operations
listed, and also lets you choose or construct a filter to be used to
as a read filter for a capture file you open.</p>
</div>
<div class="paragraph">
<p>The <em>Search Filter</em> dialog lets you do all of the editing operations
listed, and also lets you choose or construct a filter expression to be
used in a find operation.</p>
</div>
<div class="paragraph">
<p>In all of those dialogs, the <em>Filter name</em> entry specifies a
descriptive name for a filter, e.g.  <strong>Web and DNS traffic</strong>.  The
<em>Filter string</em> entry is the text that actually describes the filtering
action to take, as described above.The dialog buttons perform the
following actions:</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">New</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>If there is text in the two entry boxes, creates a new associated list
item.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Edit</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Modifies the currently selected list item to match what’s in the entry
boxes.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Delete</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Deletes the currently selected list item.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Add Expression…​</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>For display filter expressions, pops up a dialog box to allow you to
construct a filter expression to test a particular field; it offers
lists of field names, and, when appropriate, lists from which to select
tests to perform on the field and values with which to compare it.  In
that dialog box, the OK button will cause the filter expression you
constructed to be entered into the <em>Filter string</em> entry at the current
cursor position.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">OK</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>In the <em>Capture Filter</em> dialog, closes the dialog box and makes the
filter in the <em>Filter string</em> entry the filter in the <em>Capture
 Preferences</em> dialog.  In the <em>Display Filter</em> dialog, closes the dialog
box and makes the filter in the <em>Filter string</em> entry the current
display filter, and applies it to the current capture.  In the <em>Read
 Filter</em> dialog, closes the dialog box and makes the filter in the
<em>Filter string</em> entry the filter in the <em>Open Capture File</em> dialog.
In the <em>Search Filter</em> dialog, closes the dialog box and makes the
filter in the <em>Filter string</em> entry the filter in the <em>Find Packet</em>
dialog.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Apply</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Makes the filter in the <em>Filter string</em> entry the current display
filter, and applies it to the current capture.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Save</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>If the list of filters being edited is the list of
capture filters, saves the current filter list to the personal capture
filters file, and if the list of filters being edited is the list of
display filters, saves the current filter list to the personal display
filters file.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Close</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Closes the dialog without doing anything with the filter in the <em>Filter
 string</em> entry.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">The Color Filters Dialog</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This dialog displays a list of color filters and allows it to be
modified.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">THE FILTER LIST</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Single rows may be selected by clicking.  Multiple rows may be selected
by using the ctrl and shift keys in combination with the mouse button.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">NEW</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Adds a new filter at the bottom of the list and opens the Edit Color
Filter dialog box.  You will have to alter the filter expression at
least before the filter will be accepted.  The format of color filter
expressions is identical to that of display filters.  The new filter is
selected, so it may immediately be moved up and down, deleted or edited.
To avoid confusion all filters are unselected before the new filter is
created.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">EDIT</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Opens the Edit Color Filter dialog box for the selected filter. (If this
button is disabled you may have more than one filter selected, making it
ambiguous which is to be edited.)</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">ENABLE</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Enables the selected color filter(s).</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">DISABLE</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Disables the selected color filter(s).</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">DELETE</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Deletes the selected color filter(s).</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">EXPORT</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Allows you to choose a file in which to save the current list of color
filters.  You may also choose to save only the selected filters.  A
button is provided to save the filters in the global color filters file
(you must have sufficient permissions to write this file, of course).</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">IMPORT</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Allows you to choose a file containing color filters which are then
added to the bottom of the current list.  All the added filters are
selected, so they may be moved to the correct position in the list as a
group.  To avoid confusion, all filters are unselected before the new
filters are imported.  A button is provided to load the filters from the
global color filters file.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">CLEAR</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Deletes your personal color filters file, reloads the global
color filters file, if any, and closes the dialog.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">UP</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Moves the selected filter(s) up the list, making it more likely that
they will be used to color packets.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">DOWN</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Moves the selected filter(s) down the list, making it less likely that
they will be used to color packets.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">OK</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Closes the dialog and uses the color filters as they stand.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">APPLY</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Colors the packets according to the current list of color filters, but
does not close the dialog.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">SAVE</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Saves the current list of color filters in your personal color filters
file.  Unless you do this they will not be used the next time you start
Wireshark.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">CLOSE</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Closes the dialog without changing the coloration of the packets.  Note
that changes you have made to the current list of color filters are not
undone.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Capture Options Dialog</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>Capture Options Dialog</em> lets you specify various parameters for
capturing live packet data.</p>
</div>
<div class="paragraph">
<p>The <em>Interface:</em> field lets you specify the interface from which to
capture packet data or a command from which to get the packet data via a
pipe.</p>
</div>
<div class="paragraph">
<p>The <em>Link layer header type:</em> field lets you specify the interfaces link
layer header type.  This field is usually disabled, as most interface have
only one header type.</p>
</div>
<div class="paragraph">
<p>The <em>Capture packets in promiscuous mode</em> check box lets you specify
whether the interface should be put into promiscuous mode when
capturing.</p>
</div>
<div class="paragraph">
<p>The <em>Limit each packet to …​ bytes</em> check box and field lets you
specify a maximum number of bytes per packet to capture and save; if the
check box is not checked, the limit will be 262144 bytes.</p>
</div>
<div class="paragraph">
<p>The <em>Capture Filter:</em> entry lets you specify the capture filter using a
tcpdump-style filter string as described above.</p>
</div>
<div class="paragraph">
<p>The <em>File:</em> entry lets you specify the file into which captured packets
should be saved, as in the <em>Printer Options</em> dialog above.  If not
specified, the captured packets will be saved in a temporary file; you
can save those packets to a file with the <em>File:Save As</em> menu item.</p>
</div>
<div class="paragraph">
<p>The <em>Use multiple files</em> check box lets you specify that the capture
should be done in "multiple files" mode.  This option is disabled, if the
<em>Update list of packets in real time</em> option is checked.</p>
</div>
<div class="paragraph">
<p>The <em>Next file every …​  megabyte(s)</em> check box and fields lets
you specify that a switch to a next file should be done
if the specified filesize is reached.  You can also select the appropriate
unit, but beware that the filesize has a maximum of 2 GiB.
The check box is forced to be checked, as "multiple files" mode requires a
file size to be specified.</p>
</div>
<div class="paragraph">
<p>The <em>Next file every …​ minute(s)</em> check box and fields lets
you specify that the switch to a next file should be done after the specified
time has elapsed, even if the specified capture size is not reached.</p>
</div>
<div class="paragraph">
<p>The <em>Ring buffer with …​ files</em> field lets you specify the number
of files of a ring buffer.  This feature will capture into the first file
again, after the specified number of files have been used.</p>
</div>
<div class="paragraph">
<p>The <em>Stop capture after …​ files</em> field lets you specify the number
of capture files used, until the capture is stopped.</p>
</div>
<div class="paragraph">
<p>The <em>Stop capture after …​ packet(s)</em> check box and field let
you specify that Wireshark should stop capturing after having captured
some number of packets; if the check box is not checked, Wireshark will
not stop capturing at some fixed number of captured packets.</p>
</div>
<div class="paragraph">
<p>The <em>Stop capture after …​ megabyte(s)</em> check box and field lets
you specify that Wireshark should stop capturing after the file to which
captured packets are being saved grows as large as or larger than some
specified number of megabytes.  If the check box is not checked, Wireshark
will not stop capturing at some capture file size (although the operating
system on which Wireshark is running, or the available disk space, may still
limit the maximum size of a capture file).  This option is disabled, if
"multiple files" mode is used,</p>
</div>
<div class="paragraph">
<p>The <em>Stop capture after …​  second(s)</em> check box and field let you
specify that Wireshark should stop capturing after it has been capturing
for some number of seconds; if the check box is not checked, Wireshark
will not stop capturing after some fixed time has elapsed.</p>
</div>
<div class="paragraph">
<p>The <em>Update list of packets in real time</em> check box lets you specify
whether the display should be updated as packets are captured and, if
you specify that, the <em>Automatic scrolling in live capture</em> check box
lets you specify the packet list pane should automatically scroll to
show the most recently captured packets as new packets arrive.</p>
</div>
<div class="paragraph">
<p>The <em>Enable MAC name resolution</em>, <em>Enable network name resolution</em> and
<em>Enable transport name resolution</em> check boxes let you specify whether
MAC addresses, network addresses, and transport-layer port numbers
should be translated to names.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">About</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>About</em> dialog lets you view various information about Wireshark.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">About</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Wireshark</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>Wireshark</em> page lets you view general information about Wireshark,
like the installed version, licensing information and such.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">About</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Authors</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>Authors</em> page shows the author and all contributors.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">About</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Folders</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>Folders</em> page lets you view the directory names where Wireshark is
searching it’s various configuration and other files.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1"><span class="menuseq"><b class="menu">About</b>&nbsp;<b class="caret">›</b> <b class="menuitem">Plugins</b></span></dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>Plugins</em> page lets you view the dissector plugin modules
available on your system.</p>
</div>
<div class="paragraph">
<p>The <em>Plugins List</em> shows the name and version of each dissector plugin
module found on your system.</p>
</div>
<div class="paragraph">
<p>On Unix-compatible systems, the plugins are looked for in the following
directories: the <em>lib/wireshark/plugins/$VERSION</em> directory under the
main installation directory (for example,
<em>/usr/local/lib/wireshark/plugins/$VERSION</em>), and then
<em>$HOME/.wireshark/plugins</em>.</p>
</div>
<div class="paragraph">
<p>On Windows systems, the plugins are looked for in the following
directories: <em>plugins\$VERSION</em> directory under the main installation
directory (for example, <em>C:\Program Files\Wireshark\plugins\$VERSION</em>),
and then <em>%APPDATA%\Wireshark\plugins\$VERSION</em> (or, if %APPDATA% isn’t
defined, <em>%USERPROFILE%\Application Data\Wireshark\plugins\$VERSION</em>).</p>
</div>
<div class="paragraph">
<p>$VERSION is the version number of the plugin interface, which
is typically the version number of Wireshark.  Note that a dissector
plugin module may support more than one protocol; there is not
necessarily a one-to-one correspondence between dissector plugin modules
and protocols.  Protocols supported by a dissector plugin module are
enabled and disabled using the <em>Edit:Protocols</em> dialog box, just as
protocols built into Wireshark are.</p>
</div>
</div>
</div>
</dd>
</dl>
</div>
</div>
</div>
</div>
<div class="sect1">
<h2 id="_capture_filter_syntax">CAPTURE FILTER SYNTAX</h2>
<div class="sectionbody">
<div class="paragraph">
<p>See the manual page of <a href="https://www.tcpdump.org/manpages/pcap-filter.7.html">pcap-filter</a>(7) or, if that doesn’t exist, <a href="https://www.tcpdump.org/manpages/tcpdump.1.html">tcpdump</a>(8),
or, if that doesn’t exist, <a href="https://gitlab.com/wireshark/wireshark/-/wikis/CaptureFilters" class="bare">https://gitlab.com/wireshark/wireshark/-/wikis/CaptureFilters</a>.</p>
</div>
</div>
</div>
<div class="sect1">
<h2 id="_display_filter_syntax">DISPLAY FILTER SYNTAX</h2>
<div class="sectionbody">
<div class="paragraph">
<p>For a complete table of protocol and protocol fields that are filterable
in <strong>Wireshark</strong> see the <a href="file:///usr/share/wireshark/wireshark-filter.html">wireshark-filter</a>(4) manual page.</p>
</div>
</div>
</div>
<div class="sect1">
<h2 id="_files">FILES</h2>
<div class="sectionbody">
<div class="paragraph">
<p>These files contains various <strong>Wireshark</strong> configuration settings.</p>
</div>
<div class="dlist">
<dl>
<dt class="hdlist1">Preferences</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>preferences</em> files contain global (system-wide) and personal
preference settings.  If the system-wide preference file exists, it is
read first, overriding the default settings.  If the personal preferences
file exists, it is read next, overriding any previous values.  Note: If
the command line flag <strong>-o</strong> is used (possibly more than once), it will
in turn override values from the preferences files.</p>
</div>
<div class="paragraph">
<p>The preferences settings are in the form <em>prefname:value</em>,
one per line,
where <em>prefname</em> is the name of the preference
and <em>value</em> is the value to
which it should be set; white space is allowed between <strong>:</strong> and
<em>value</em>.  A preference setting can be continued on subsequent lines by
indenting the continuation lines with white space.  A <strong>#</strong> character
starts a comment that runs to the end of the line:</p>
</div>
<div class="literalblock">
<div class="content">
<pre># Vertical scrollbars should be on right side?
# TRUE or FALSE (case-insensitive).
gui.scrollbar_on_right: TRUE</pre>
</div>
</div>
<div class="paragraph">
<p>The global preferences file is looked for in the <em>wireshark</em> directory
under the <em>share</em> subdirectory of the main installation directory (for
example, <em>/usr/local/share/wireshark/preferences</em>) on UNIX-compatible
systems, and in the main installation directory (for example,
<em>C:\Program Files\Wireshark\preferences</em>) on Windows systems.</p>
</div>
<div class="paragraph">
<p>The personal preferences file is looked for in
<em>$XDG_CONFIG_HOME/wireshark/preferences</em>
(or, if <em>$XDG_CONFIG_HOME/wireshark</em> does not exist while <em>$HOME/.wireshark</em>
is present, <em>$HOME/.wireshark/preferences</em>) on
UNIX-compatible systems and <em>%APPDATA%\Wireshark\preferences</em> (or, if
%APPDATA% isn’t defined, <em>%USERPROFILE%\Application
 Data\Wireshark\preferences</em>) on Windows systems.</p>
</div>
<div class="paragraph">
<p>Note: Whenever the preferences are saved by using the <em>Save</em> button
in the <em>Edit:Preferences</em> dialog box, your personal preferences file
will be overwritten with the new settings, destroying any comments and
unknown/obsolete settings that were in the file.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Recent</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>recent</em> file contains personal settings (mostly GUI related) such
as the current <strong>Wireshark</strong> window size.  The file is saved at program exit and
read in at program start automatically.  Note: The command line flag <strong>-o</strong>
may be used to override settings from this file.</p>
</div>
<div class="paragraph">
<p>The settings in this file have the same format as in the <em>preferences</em>
files, and the same directory as for the personal preferences file is
used.</p>
</div>
<div class="paragraph">
<p>Note: Whenever Wireshark is closed, your recent file
will be overwritten with the new settings, destroying any comments and
unknown/obsolete settings that were in the file.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Disabled (Enabled) Protocols</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>disabled_protos</em> files contain system-wide and personal lists of
protocols that have been disabled, so that their dissectors are never
called.  The files contain protocol names, one per line, where the
protocol name is the same name that would be used in a display filter
for the protocol:</p>
</div>
<div class="literalblock">
<div class="content">
<pre>http
tcp     # a comment</pre>
</div>
</div>
<div class="paragraph">
<p>If a protocol is listed in the global <em>disabled_protos</em> file, it is not
displayed in the <em>Analyze:Enabled Protocols</em> dialog box, and so cannot
be enabled by the user.</p>
</div>
<div class="paragraph">
<p>The global <em>disabled_protos</em> file uses the same directory as the global
preferences file.</p>
</div>
<div class="paragraph">
<p>The personal <em>disabled_protos</em> file uses the same directory as the
personal preferences file.</p>
</div>
<div class="paragraph">
<p>Note: Whenever the disabled protocols list is saved by using the <em>Save</em>
button in the <em>Analyze:Enabled Protocols</em> dialog box, your personal
disabled protocols file will be overwritten with the new settings,
destroying any comments that were in the file.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Name Resolution (hosts)</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>If the personal <em>hosts</em> file exists, it is
used to resolve IPv4 and IPv6 addresses before any other
attempts are made to resolve them.  The file has the standard <em>hosts</em>
file syntax; each line contains one IP address and name, separated by
whitespace.  The same directory as for the personal preferences file is used.</p>
</div>
<div class="paragraph">
<p>Capture filter name resolution is handled by libpcap on UNIX-compatible
systems and WinPcap on Windows.  As such the Wireshark personal <em>hosts</em> file
will not be consulted for capture filter name resolution.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Name Resolution (subnets)</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>If an IPv4 address cannot be translated via name resolution (no exact
match is found) then a partial match is attempted via the <em>subnets</em> file.
Both the global <em>subnets</em> file and personal <em>subnets</em> files are used
if they exist.</p>
</div>
<div class="paragraph">
<p>Each line of this file consists of an IPv4 address, a subnet mask length
separated only by a / and a name separated by whitespace. While the address
must be a full IPv4 address, any values beyond the mask length are subsequently
ignored.</p>
</div>
<div class="paragraph">
<p>An example is:</p>
</div>
<div class="paragraph">
<p># Comments must be prepended by the # sign!
192.168.0.0/24 ws_test_network</p>
</div>
<div class="paragraph">
<p>A partially matched name will be printed as "subnet-name.remaining-address".
For example, "192.168.0.1" under the subnet above would be printed as
"ws_test_network.1"; if the mask length above had been 16 rather than 24, the
printed address would be "ws_test_network.0.1".</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Name Resolution (ethers)</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>ethers</em> files are consulted to correlate 6-byte hardware addresses to
names.  First the personal <em>ethers</em> file is tried and if an address is not
found there the global <em>ethers</em> file is tried next.</p>
</div>
<div class="paragraph">
<p>Each line contains one hardware address and name, separated by
whitespace.  The digits of the hardware address are separated by colons
(:), dashes (-) or periods (.).  The same separator character must be
used consistently in an address.  The following three lines are valid
lines of an <em>ethers</em> file:</p>
</div>
<div class="literalblock">
<div class="content">
<pre>ff:ff:ff:ff:ff:ff          Broadcast
c0-00-ff-ff-ff-ff          TR_broadcast
00.00.00.00.00.00          Zero_broadcast</pre>
</div>
</div>
<div class="paragraph">
<p>The global <em>ethers</em> file is looked for in the <em>/etc</em> directory on
UNIX-compatible systems, and in the main installation directory (for
example, <em>C:\Program Files\Wireshark</em>) on Windows systems.</p>
</div>
<div class="paragraph">
<p>The personal <em>ethers</em> file is looked for in the same directory as the personal
preferences file.</p>
</div>
<div class="paragraph">
<p>Capture filter name resolution is handled by libpcap on UNIX-compatible
systems and WinPcap on Windows.  As such the Wireshark personal <em>ethers</em> file
will not be consulted for capture filter name resolution.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Name Resolution (manuf)</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>manuf</em> file is used to match the 3-byte vendor portion of a 6-byte
hardware address with the manufacturer’s name; it can also contain well-known
MAC addresses and address ranges specified with a netmask.  The format of the
file is the same as the <em>ethers</em> files, except that entries such as:</p>
</div>
<div class="literalblock">
<div class="content">
<pre>00:00:0C      Cisco</pre>
</div>
</div>
<div class="paragraph">
<p>can be provided, with the 3-byte OUI and the name for a vendor, and
entries such as:</p>
</div>
<div class="literalblock">
<div class="content">
<pre>00-00-0C-07-AC/40     All-HSRP-routers</pre>
</div>
</div>
<div class="paragraph">
<p>can be specified, with a MAC address and a mask indicating how many bits
of the address must match.  The above entry, for example, has 40
significant bits, or 5 bytes, and would match addresses from
00-00-0C-07-AC-00 through 00-00-0C-07-AC-FF.  The mask need not be a
multiple of 8.</p>
</div>
<div class="paragraph">
<p>The <em>manuf</em> file is looked for in the same directory as the global
preferences file.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Name Resolution (services)</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>services</em> file is used to translate port numbers into names.
Both the global <em>services</em> file and personal <em>services</em> files are used
if they exist.</p>
</div>
<div class="paragraph">
<p>The file has the standard <em>services</em> file syntax; each line contains one
(service) name and one transport identifier separated by white space.  The
transport identifier includes one port number and one transport protocol name
(typically tcp, udp, or sctp) separated by a /.</p>
</div>
<div class="paragraph">
<p>An example is:</p>
</div>
<div class="paragraph">
<p>mydns       5045/udp     # My own Domain Name Server
mydns       5045/tcp     # My own Domain Name Server</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Name Resolution (ipxnets)</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>ipxnets</em> files are used to correlate 4-byte IPX network numbers to
names.  First the global <em>ipxnets</em> file is tried and if that address is not
found there the personal one is tried next.</p>
</div>
<div class="paragraph">
<p>The format is the same as the <em>ethers</em>
file, except that each address is four bytes instead of six.
Additionally, the address can be represented as a single hexadecimal
number, as is more common in the IPX world, rather than four hex octets.
For example, these four lines are valid lines of an <em>ipxnets</em> file:</p>
</div>
<div class="literalblock">
<div class="content">
<pre>C0.A8.2C.00              HR
c0-a8-1c-00              CEO
00:00:BE:EF              IT_Server1
110f                     FileServer3</pre>
</div>
</div>
<div class="paragraph">
<p>The global <em>ipxnets</em> file is looked for in the <em>/etc</em> directory on
UNIX-compatible systems, and in the main installation directory (for
example, <em>C:\Program Files\Wireshark</em>) on Windows systems.</p>
</div>
<div class="paragraph">
<p>The personal <em>ipxnets</em> file is looked for in the same directory as the
personal preferences file.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Capture Filters</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>cfilters</em> files contain system-wide and personal capture filters.
Each line contains one filter, starting with the string displayed in the
dialog box in quotation marks, followed by the filter string itself:</p>
</div>
<div class="literalblock">
<div class="content">
<pre>"HTTP" port 80
"DCERPC" port 135</pre>
</div>
</div>
<div class="paragraph">
<p>The global <em>cfilters</em> file uses the same directory as the
global preferences file.</p>
</div>
<div class="paragraph">
<p>The personal <em>cfilters</em> file uses the same directory as the personal
preferences file.  It is written through the Capture:Capture Filters
dialog.</p>
</div>
<div class="paragraph">
<p>If the global <em>cfilters</em> file exists, it is used only if the personal
<em>cfilters</em> file does not exist; global and personal capture filters are
not merged.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Display Filters</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>dfilters</em> files contain system-wide and personal display filters.
Each line contains one filter, starting with the string displayed in the
dialog box in quotation marks, followed by the filter string itself:</p>
</div>
<div class="literalblock">
<div class="content">
<pre>"HTTP" http
"DCERPC" dcerpc</pre>
</div>
</div>
<div class="paragraph">
<p>The global <em>dfilters</em> file uses the same directory as the
global preferences file.</p>
</div>
<div class="paragraph">
<p>The personal <em>dfilters</em> file uses the same directory as the
personal preferences file.  It is written through the Analyze:Display
Filters dialog.</p>
</div>
<div class="paragraph">
<p>If the global <em>dfilters</em> file exists, it is used only if the personal
<em>dfilters</em> file does not exist; global and personal display filters are
not merged.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Color Filters (Coloring Rules)</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>The <em>colorfilters</em> files contain system-wide and personal color filters.
Each line contains one filter, starting with the string displayed in the
dialog box, followed by the corresponding display filter.  Then the
background and foreground colors are appended:</p>
</div>
<div class="literalblock">
<div class="content">
<pre># a comment
@tcp@tcp@[59345,58980,65534][0,0,0]
@udp@udp@[28834,57427,65533][0,0,0]</pre>
</div>
</div>
<div class="paragraph">
<p>The global <em>colorfilters</em> file uses the same directory as the
global preferences file.</p>
</div>
<div class="paragraph">
<p>The personal <em>colorfilters</em> file uses the same directory as the
personal preferences file.  It is written through the View:Coloring Rules
dialog.</p>
</div>
<div class="paragraph">
<p>If the global <em>colorfilters</em> file exists, it is used only if the personal
<em>colorfilters</em> file does not exist; global and personal color filters are
not merged.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">Plugins</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>See above in the description of the About:Plugins page.</p>
</div>
</div>
</div>
</dd>
</dl>
</div>
</div>
</div>
<div class="sect1">
<h2 id="_environment_variables">ENVIRONMENT VARIABLES</h2>
<div class="sectionbody">
<div class="dlist">
<dl>
<dt class="hdlist1">WIRESHARK_CONFIG_DIR</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This environment variable overrides the location of personal configuration
files. It defaults to <em>$XDG_CONFIG_HOME/wireshark</em> (or <em>$HOME/.wireshark</em> if
the former is missing while the latter exists). On Windows,
<em>%APPDATA%\Wireshark</em> is used instead. Available since Wireshark 3.0.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">WIRESHARK_DEBUG_WMEM_OVERRIDE</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Setting this environment variable forces the wmem framework to use the
specified allocator backend for <strong>all</strong> allocations, regardless of which
backend is normally specified by the code. This is mainly useful to developers
when testing or debugging. See <em>README.wmem</em> in the source distribution for
details.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">WIRESHARK_RUN_FROM_BUILD_DIRECTORY</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This environment variable causes the plugins and other data files to be loaded
from the build directory (where the program was compiled) rather than from the
standard locations.  It has no effect when the program in question is running
with root (or setuid) permissions on *NIX.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">WIRESHARK_DATA_DIR</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This environment variable causes the various data files to be loaded from
a directory other than the standard locations.  It has no effect when the
program in question is running with root (or setuid) permissions on *NIX.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">ERF_RECORDS_TO_CHECK</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This environment variable controls the number of ERF records checked when
deciding if a file really is in the ERF format.  Setting this environment
variable a number higher than the default (20) would make false positives
less likely.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">IPFIX_RECORDS_TO_CHECK</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This environment variable controls the number of IPFIX records checked when
deciding if a file really is in the IPFIX format.  Setting this environment
variable a number higher than the default (20) would make false positives
less likely.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">WIRESHARK_ABORT_ON_DISSECTOR_BUG</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>If this environment variable is set, <strong>Wireshark</strong> will call abort(3)
when a dissector bug is encountered.  abort(3) will cause the program to
exit abnormally; if you are running <strong>Wireshark</strong> in a debugger, it
should halt in the debugger and allow inspection of the process, and, if
you are not running it in a debugger, it will, on some OSes, assuming
your environment is configured correctly, generate a core dump file.
This can be useful to developers attempting to troubleshoot a problem
with a protocol dissector.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">WIRESHARK_ABORT_ON_TOO_MANY_ITEMS</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>If this environment variable is set, <strong>Wireshark</strong> will call abort(3)
if a dissector tries to add too many items to a tree (generally this
is an indication of the dissector not breaking out of a loop soon enough).
abort(3) will cause the program to exit abnormally; if you are running
<strong>Wireshark</strong> in a debugger, it should halt in the debugger and allow
inspection of the process, and, if you are not running it in a debugger,
it will, on some OSes, assuming your environment is configured correctly,
generate a core dump file.  This can be useful to developers attempting to
troubleshoot a problem with a protocol dissector.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">WIRESHARK_QUIT_AFTER_CAPTURE</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Cause <strong>Wireshark</strong> to exit after the end of the capture session.  This
doesn’t automatically start a capture; you must still use <strong>-k</strong> to do
that.  You must also specify an autostop condition, e.g.  <strong>-c</strong> or <strong>-a
 duration:…​</strong>.  This means that you will not be able to see the results
of the capture after it stops; it’s primarily useful for testing.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">WIRESHARK_LOG_LEVEL</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This environment variable controls the verbosity of diagnostic messages to
the console. From less verbose to most verbose levels can be <code>critical</code>,
<code>warning</code>, <code>message</code>, <code>info</code>, <code>debug</code> or <code>noisy</code>. Levels above the
current level are also active. Levels <code>critical</code> and <code>error</code> are always
active.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">WIRESHARK_LOG_FATAL</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Sets the fatal log level. Fatal log levels cause the program to abort.
This level can be set to <code>Error</code>, <code>critical</code> or <code>warning</code>. <code>Error</code> is
always fatal and is the default.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">WIRESHARK_LOG_DOMAINS</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>This environment variable selects which log domains are active. The filter is
given as a case-insensitive comma separated list. If set only the included
domains will be enabled. The default domain is always considered to be enabled.
Domain filter lists can be preceded by '!' to invert the sense of the match.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">WIRESHARK_LOG_DEBUG</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>List of domains with <code>debug</code> log level. This sets the level of the provided
log domains and takes precedence over the active domains filter. If preceded
by '!' this disables the <code>debug</code> level instead.</p>
</div>
</div>
</div>
</dd>
<dt class="hdlist1">WIRESHARK_LOG_NOISY</dt>
<dd>
<div class="openblock">
<div class="content">
<div class="paragraph">
<p>Same as above but for <code>noisy</code> log level instead.</p>
</div>
</div>
</div>
</dd>
</dl>
</div>
</div>
</div>
<div class="sect1">
<h2 id="_authors">AUTHORS</h2>
<div class="sectionbody">
<div class="paragraph">
<p>Wireshark would not be the powerful, featureful application it is without the generous contributions of hundreds of developers.</p>
</div>
<div class="paragraph">
<p>A complete list of authors can be found in the AUTHORS file in Wireshark’s source code repository and at <a href="https://www.wireshark.org/about.html#authors" class="bare">https://www.wireshark.org/about.html#authors</a>.</p>
</div>
</div>
</div>
<div class="sect1">
<h2 id="_see_also">SEE ALSO</h2>
<div class="sectionbody">
<div class="paragraph">
<p><a href="file:///usr/share/wireshark/wireshark-filter.html">wireshark-filter</a>(4), <a href="file:///usr/share/wireshark/tshark.html">tshark</a>(1), <a href="file:///usr/share/wireshark/editcap.html">editcap</a>(1), <a href="https://www.tcpdump.org/manpages/pcap.3pcap.html">pcap</a>(3), <a href="file:///usr/share/wireshark/dumpcap.html">dumpcap</a>(1), <a href="file:///usr/share/wireshark/mergecap.html">mergecap</a>(1),
<a href="file:///usr/share/wireshark/text2pcap.html">text2pcap</a>(1), <a href="https://www.tcpdump.org/manpages/pcap-filter.7.html">pcap-filter</a>(7) or <a href="https://www.tcpdump.org/manpages/tcpdump.1.html">tcpdump</a>(8)</p>
</div>
</div>
</div>
<div class="sect1">
<h2 id="_notes">NOTES</h2>
<div class="sectionbody">
<div class="paragraph">
<p>This is the manual page for <strong>Wireshark</strong> 3.6.2.
The latest version of <strong>Wireshark</strong> can be found at
<a href="https://www.wireshark.org/" class="bare">https://www.wireshark.org</a>.</p>
</div>
<div class="paragraph">
<p>HTML versions of the Wireshark project man pages are available at
<a href="https://www.wireshark.org/docs/man-pages" class="bare">https://www.wireshark.org/docs/man-pages</a>.</p>
</div>
</div>
</div>
</div>
<div id="footer">
<div id="footer-text">
Last updated 2022-03-04 16:13:20 UTC
</div>
</div>

</body></html>