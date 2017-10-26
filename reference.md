<!DOCTYPE html><html lang="en"><head><meta charset="utf-8"><title>GN Reference</title><link rel="stylesheet" type="text/css" href="/+static/base.HLL9TqKl0YYybSzmT_wTdw.cache.css"/><link rel="stylesheet" type="text/css" href="/+static/doc.fY_dVMHIoRstreKV1Va--g.cache.css"/><link rel="stylesheet" type="text/css" href="/+static/prettify/prettify.pZ5FqzM6cPxAflH0va2Ucw.cache.css"/><!-- default customHeadTagPart --></head><body class="Site"><header class="Site-header "><div class="Header"><div class="Header-title"></div></div></header><div class="Site-content Site-Content--markdown"><div class="Container"><div class="doc"><h1><a class="h" name="GN-Reference" href="#GN-Reference"><span></span></a><a class="h" name="gn-reference" href="#gn-reference"><span></span></a>GN Reference</h1><p><em>This page is automatically generated from</em> <code class="code">gn help --markdown all</code>.</p><h2><a class="h" name="Contents" href="#Contents"><span></span></a><a class="h" name="contents" href="#contents"><span></span></a>Contents</h2><ul><li><a href="#commands">Commands</a><ul><li><a href="#analyze">analyze: Analyze which targets are affected by a list of files.</a></li><li><a href="#args">args: Display or configure arguments declared by the build.</a></li><li><a href="#check">check: Check header dependencies.</a></li><li><a href="#clean">clean: Cleans the output directory.</a></li><li><a href="#desc">desc: Show lots of insightful information about a target or config.</a></li><li><a href="#format">format: Format .gn file.</a></li><li><a href="#gen">gen: Generate ninja files.</a></li><li><a href="#help">help: Does what you think.</a></li><li><a href="#ls">ls: List matching targets.</a></li><li><a href="#path">path: Find paths between two targets.</a></li><li><a href="#refs">refs: Find stuff referencing a target or file.</a></li></ul></li><li><a href="#targets">Target declarations</a><ul><li><a href="#action">action: Declare a target that runs a script a single time.</a></li><li><a href="#action_foreach">action_foreach: Declare a target that runs a script over a set of files.</a></li><li><a href="#bundle_data">bundle_data: [iOS/macOS] Declare a target without output.</a></li><li><a href="#copy">copy: Declare a target that copies files.</a></li><li><a href="#create_bundle">create_bundle: [iOS/macOS] Build an iOS or macOS bundle.</a></li><li><a href="#executable">executable: Declare an executable target.</a></li><li><a href="#group">group: Declare a named group of targets.</a></li><li><a href="#loadable_module">loadable_module: Declare a loadable module target.</a></li><li><a href="#shared_library">shared_library: Declare a shared library target.</a></li><li><a href="#source_set">source_set: Declare a source set target.</a></li><li><a href="#static_library">static_library: Declare a static library target.</a></li><li><a href="#target">target: Declare an target with the given programmatic type.</a></li></ul></li><li><a href="#functions">Buildfile functions</a><ul><li><a href="#assert">assert: Assert an expression is true at generation time.</a></li><li><a href="#config">config: Defines a configuration object.</a></li><li><a href="#declare_args">declare_args: Declare build arguments.</a></li><li><a href="#defined">defined: Returns whether an identifier is defined.</a></li><li><a href="#exec_script">exec_script: Synchronously run a script and return the output.</a></li><li><a href="#foreach">foreach: Iterate over a list.</a></li><li><a href="#forward_variables_from">forward_variables_from: Copies variables from a different scope.</a></li><li><a href="#get_label_info">get_label_info: Get an attribute from a target&#39;s label.</a></li><li><a href="#get_path_info">get_path_info: Extract parts of a file or directory name.</a></li><li><a href="#get_target_outputs">get_target_outputs: [file list] Get the list of outputs from a target.</a></li><li><a href="#getenv">getenv: Get an environment variable.</a></li><li><a href="#import">import: Import a file into the current scope.</a></li><li><a href="#not_needed">not_needed: Mark variables from scope as not needed.</a></li><li><a href="#pool">pool: Defines a pool object.</a></li><li><a href="#print">print: Prints to the console.</a></li><li><a href="#process_file_template">process_file_template: Do template expansion over a list of files.</a></li><li><a href="#read_file">read_file: Read a file into a variable.</a></li><li><a href="#rebase_path">rebase_path: Rebase a file or directory to another location.</a></li><li><a href="#set_default_toolchain">set_default_toolchain: Sets the default toolchain name.</a></li><li><a href="#set_defaults">set_defaults: Set default values for a target type.</a></li><li><a href="#set_sources_assignment_filter">set_sources_assignment_filter: Set a pattern to filter source files.</a></li><li><a href="#split_list">split_list: Splits a list into N different sub-lists.</a></li><li><a href="#template">template: Define a template rule.</a></li><li><a href="#tool">tool: Specify arguments to a toolchain tool.</a></li><li><a href="#toolchain">toolchain: Defines a toolchain.</a></li><li><a href="#write_file">write_file: Write a file to disk.</a></li></ul></li><li><a href="#predefined_variables">Built-in predefined variables</a><ul><li><a href="#current_cpu">current_cpu: [string] The processor architecture of the current toolchain.</a></li><li><a href="#current_os">current_os: [string] The operating system of the current toolchain.</a></li><li><a href="#current_toolchain">current_toolchain: [string] Label of the current toolchain.</a></li><li><a href="#default_toolchain">default_toolchain: [string] Label of the default toolchain.</a></li><li><a href="#host_cpu">host_cpu: [string] The processor architecture that GN is running on.</a></li><li><a href="#host_os">host_os: [string] The operating system that GN is running on.</a></li><li><a href="#invoker">invoker: [string] The invoking scope inside a template.</a></li><li><a href="#python_path">python_path: [string] Absolute path of Python.</a></li><li><a href="#root_build_dir">root_build_dir: [string] Directory where build commands are run.</a></li><li><a href="#root_gen_dir">root_gen_dir: [string] Directory for the toolchain&#39;s generated files.</a></li><li><a href="#root_out_dir">root_out_dir: [string] Root directory for toolchain output files.</a></li><li><a href="#target_cpu">target_cpu: [string] The desired cpu architecture for the build.</a></li><li><a href="#target_gen_dir">target_gen_dir: [string] Directory for a target&#39;s generated files.</a></li><li><a href="#target_name">target_name: [string] The name of the current target.</a></li><li><a href="#target_os">target_os: [string] The desired operating system for the build.</a></li><li><a href="#target_out_dir">target_out_dir: [string] Directory for target output files.</a></li></ul></li><li><a href="#target_variables">Variables you set in targets</a><ul><li><a href="#all_dependent_configs">all_dependent_configs: [label list] Configs to be forced on dependents.</a></li><li><a href="#allow_circular_includes_from">allow_circular_includes_from: [label list] Permit includes from deps.</a></li><li><a href="#arflags">arflags: [string list] Arguments passed to static_library archiver.</a></li><li><a href="#args">args: [string list] Arguments passed to an action.</a></li><li><a href="#asmflags">asmflags: [string list] Flags passed to the assembler.</a></li><li><a href="#assert_no_deps">assert_no_deps: [label pattern list] Ensure no deps on these targets.</a></li><li><a href="#bundle_contents_dir">bundle_contents_dir: Expansion of {{bundle_contents_dir}} in create_bundle.</a></li><li><a href="#bundle_deps_filter">bundle_deps_filter: [label list] A list of labels that are filtered out.</a></li><li><a href="#bundle_executable_dir">bundle_executable_dir: Expansion of {{bundle_executable_dir}} in create_bundle</a></li><li><a href="#bundle_plugins_dir">bundle_plugins_dir: Expansion of {{bundle_plugins_dir}} in create_bundle.</a></li><li><a href="#bundle_resources_dir">bundle_resources_dir: Expansion of {{bundle_resources_dir}} in create_bundle.</a></li><li><a href="#bundle_root_dir">bundle_root_dir: Expansion of {{bundle_root_dir}} in create_bundle.</a></li><li><a href="#cflags">cflags: [string list] Flags passed to all C compiler variants.</a></li><li><a href="#cflags_c">cflags_c: [string list] Flags passed to the C compiler.</a></li><li><a href="#cflags_cc">cflags_cc: [string list] Flags passed to the C++ compiler.</a></li><li><a href="#cflags_objc">cflags_objc: [string list] Flags passed to the Objective C compiler.</a></li><li><a href="#cflags_objcc">cflags_objcc: [string list] Flags passed to the Objective C++ compiler.</a></li><li><a href="#check_includes">check_includes: [boolean] Controls whether a target&#39;s files are checked.</a></li><li><a href="#code_signing_args">code_signing_args: [string list] Arguments passed to code signing script.</a></li><li><a href="#code_signing_outputs">code_signing_outputs: [file list] Output files for code signing step.</a></li><li><a href="#code_signing_script">code_signing_script: [file name] Script for code signing.</a></li><li><a href="#code_signing_sources">code_signing_sources: [file list] Sources for code signing step.</a></li><li><a href="#complete_static_lib">complete_static_lib: [boolean] Links all deps into a static library.</a></li><li><a href="#configs">configs: [label list] Configs applying to this target or config.</a></li><li><a href="#data">data: [file list] Runtime data file dependencies.</a></li><li><a href="#data_deps">data_deps: [label list] Non-linked dependencies.</a></li><li><a href="#defines">defines: [string list] C preprocessor defines.</a></li><li><a href="#depfile">depfile: [string] File name for input dependencies for actions.</a></li><li><a href="#deps">deps: [label list] Private linked dependencies.</a></li><li><a href="#include_dirs">include_dirs: [directory list] Additional include directories.</a></li><li><a href="#inputs">inputs: [file list] Additional compile-time dependencies.</a></li><li><a href="#ldflags">ldflags: [string list] Flags passed to the linker.</a></li><li><a href="#lib_dirs">lib_dirs: [directory list] Additional library directories.</a></li><li><a href="#libs">libs: [string list] Additional libraries to link.</a></li><li><a href="#output_dir">output_dir: [directory] Directory to put output file in.</a></li><li><a href="#output_extension">output_extension: [string] Value to use for the output&#39;s file extension.</a></li><li><a href="#output_name">output_name: [string] Name for the output file other than the default.</a></li><li><a href="#output_prefix_override">output_prefix_override: [boolean] Don&#39;t use prefix for output name.</a></li><li><a href="#outputs">outputs: [file list] Output files for actions and copy targets.</a></li><li><a href="#partial_info_plist">partial_info_plist: [filename] Path plist from asset catalog compiler.</a></li><li><a href="#pool">pool: [string] Label of the pool used by the action.</a></li><li><a href="#precompiled_header">precompiled_header: [string] Header file to precompile.</a></li><li><a href="#precompiled_header_type">precompiled_header_type: [string] &ldquo;gcc&rdquo; or &ldquo;msvc&rdquo;.</a></li><li><a href="#precompiled_source">precompiled_source: [file name] Source file to precompile.</a></li><li><a href="#product_type">product_type: [string] Product type for Xcode projects.</a></li><li><a href="#public">public: [file list] Declare public header files for a target.</a></li><li><a href="#public_configs">public_configs: [label list] Configs applied to dependents.</a></li><li><a href="#public_deps">public_deps: [label list] Declare public dependencies.</a></li><li><a href="#response_file_contents">response_file_contents: [string list] Contents of .rsp file for actions.</a></li><li><a href="#script">script: [file name] Script file for actions.</a></li><li><a href="#sources">sources: [file list] Source files for a target.</a></li><li><a href="#testonly">testonly: [boolean] Declares a target must only be used for testing.</a></li><li><a href="#visibility">visibility: [label list] A list of labels that can depend on a target.</a></li><li><a href="#write_runtime_deps">write_runtime_deps: Writes the target&#39;s runtime_deps to the given path.</a></li><li><a href="#xcode_extra_attributes">xcode_extra_attributes: [scope] Extra attributes for Xcode projects.</a></li><li><a href="#test_application_name">test_application_name: [string] Test application name for unit or ui test target.</a></li></ul></li><li><a href="#other">Other help topics</a><ul><li><a href="#all">all: Print all the help at once</a></li><li><a href="#buildargs">buildargs: How build arguments work.</a></li><li><a href="#dotfile">dotfile: Info about the toplevel .gn file.</a></li><li><a href="#execution">execution: Build graph and execution overview.</a></li><li><a href="#grammar">grammar: Language and grammar for GN build files.</a></li><li><a href="#input_conversion">input_conversion: Processing input from exec_script and read_file.</a></li><li><a href="#label_pattern">label_pattern: Matching more than one label.</a></li><li><a href="#labels">labels: About labels.</a></li><li><a href="#ninja_rules">ninja_rules: How Ninja build rules are named.</a></li><li><a href="#nogncheck">nogncheck: Annotating includes for checking.</a></li><li><a href="#runtime_deps">runtime_deps: How runtime dependency computation works.</a></li><li><a href="#source_expansion">source_expansion: Map sources to outputs for scripts.</a></li><li><a href="#switches">switches: Show available command-line switches.</a></li></ul></li></ul><h2><a class="h" name="commands" href="#commands"><span></span></a>Commands</h2><h3><a class="h" name="analyze" href="#analyze"><span></span></a><strong>gn analyze &lt;out_dir&gt; &lt;input_path&gt; &lt;output_path&gt;</strong></h3><pre class="code">  Analyze which targets are affected by a list of files.

  This command takes three arguments:

  out_dir is the path to the build directory.

  input_path is a path to a file containing a JSON object with three fields:

   - &quot;files&quot;: A list of the filenames to check.

   - &quot;test_targets&quot;: A list of the labels for targets that are needed to run
     the tests we wish to run.

   - &quot;additional_compile_targets&quot;: A list of the labels for targets that we
     wish to rebuild, but aren&#39;t necessarily needed for testing. The important
     difference between this field and &quot;test_targets&quot; is that if an item in
     the additional_compile_targets list refers to a group, then any
     dependencies of that group will be returned if they are out of date, but
     the group itself does not need to be. If the dependencies themselves are
     groups, the same filtering is repeated. This filtering can be used to
     avoid rebuilding dependencies of a group that are unaffected by the input
     files. The list may also contain the string &quot;all&quot; to refer to a
     pseudo-group that contains every root target in the build graph.

     This filtering behavior is also known as &quot;pruning&quot; the list of compile
     targets.

  output_path is a path indicating where the results of the command are to be
  written. The results will be a file containing a JSON object with one or more
  of following fields:

   - &quot;compile_targets&quot;: A list of the labels derived from the input
     compile_targets list that are affected by the input files. Due to the way
     the filtering works for compile targets as described above, this list may
     contain targets that do not appear in the input list.

   - &quot;test_targets&quot;: A list of the labels from the input test_targets list that
     are affected by the input files. This list will be a proper subset of the
     input list.

   - &quot;invalid_targets&quot;: A list of any names from the input that do not exist in
     the build graph. If this list is non-empty, the &quot;error&quot; field will also be
     set to &quot;Invalid targets&quot;.

   - &quot;status&quot;: A string containing one of three values:

       - &quot;Found dependency&quot;
       - &quot;No dependency&quot;
       - &quot;Found dependency (all) &quot;

     In the first case, the lists returned in compile_targets and test_targets
     should be passed to ninja to build. In the second case, nothing was
     affected and no build is necessary. In the third case, GN could not
     determine the correct answer and returned the input as the output in order
     to be safe.

   - &quot;error&quot;: This will only be present if an error occurred, and will contain
     a string describing the error. This includes cases where the input file is
     not in the right format, or contains invalid targets.

  The command returns 1 if it is unable to read the input file or write the
  output file, or if there is something wrong with the build such that gen
  would also fail, and 0 otherwise. In particular, it returns 0 even if the
  &quot;error&quot; key is non-empty and a non-fatal error occurred. In other words, it
  tries really hard to always write something to the output JSON and convey
  errors that way rather than via return codes.
</pre><h3><a class="h" name="args-1" href="#args-1"><span></span></a><strong>gn args &lt;out_dir&gt; [--list] [--short] [--args] [--overrides-only]</strong></h3><pre class="code">  See also &quot;gn help buildargs&quot; for a more high-level overview of how
  build arguments work.
</pre><h4><a class="h" name="Commands-gn-args-out_dir_list_short_args_overrides_only-Usage" href="#Commands-gn-args-out_dir_list_short_args_overrides_only-Usage"><span></span></a><a class="h" name="commands-gn-args-out_dir_list_short_args_overrides_only-usage" href="#commands-gn-args-out_dir_list_short_args_overrides_only-usage"><span></span></a><strong>Usage</strong></h4><pre class="code">  gn args &lt;out_dir&gt;
      Open the arguments for the given build directory in an editor. If the
      given build directory doesn&#39;t exist, it will be created and an empty args
      file will be opened in the editor. You would type something like this
      into that file:
          enable_doom_melon=false
          os=&quot;android&quot;

      To find your editor on Posix, GN will search the environment variables in
      order: GN_EDITOR, VISUAL, and EDITOR. On Windows GN will open the command
      associated with .txt files.

      Note: you can edit the build args manually by editing the file &quot;args.gn&quot;
      in the build directory and then running &quot;gn gen &lt;out_dir&gt;&quot;.

  gn args &lt;out_dir&gt; --list[=&lt;exact_arg&gt;] [--short] [--overrides-only]
      Lists all build arguments available in the current configuration, or, if
      an exact_arg is specified for the list flag, just that one build
      argument.

      The output will list the declaration location, current value for the
      build, default value (if different than the current value), and comment
      preceeding the declaration.

      If --short is specified, only the names and current values will be
      printed.

      If --overrides-only is specified, only the names and current values of
      arguments that have been overridden (i.e. non-default arguments) will
      be printed. Overrides come from the &lt;out_dir&gt;/args.gn file and //.gn
</pre><h4><a class="h" name="Commands-gn-args-out_dir_list_short_args_overrides_only-Examples" href="#Commands-gn-args-out_dir_list_short_args_overrides_only-Examples"><span></span></a><a class="h" name="commands-gn-args-out_dir_list_short_args_overrides_only-examples" href="#commands-gn-args-out_dir_list_short_args_overrides_only-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  gn args out/Debug
    Opens an editor with the args for out/Debug.

  gn args out/Debug --list --short
    Prints all arguments with their default values for the out/Debug
    build.

  gn args out/Debug --list --short --overrides-only
    Prints overridden arguments for the out/Debug build.

  gn args out/Debug --list=target_cpu
    Prints information about the &quot;target_cpu&quot; argument for the &quot;
   &quot;out/Debug
    build.

  gn args --list --args=&quot;os=\&quot;android\&quot; enable_doom_melon=true&quot;
    Prints all arguments with the default values for a build with the
    given arguments set (which may affect the values of other
    arguments).
</pre><h3><a class="h" name="check" href="#check"><span></span></a><strong>gn check &lt;out_dir&gt; [&lt;label_pattern&gt;] [--force]</strong></h3><pre class="code">  GN&#39;s include header checker validates that the includes for C-like source
  files match the build dependency graph.

  &quot;gn check&quot; is the same thing as &quot;gn gen&quot; with the &quot;--check&quot; flag except that
  this command does not write out any build files. It&#39;s intended to be an easy
  way to manually trigger include file checking.

  The &lt;label_pattern&gt; can take exact labels or patterns that match more than
  one (although not general regular expressions). If specified, only those
  matching targets will be checked. See &quot;gn help label_pattern&quot; for details.
</pre><h4><a class="h" name="Command_specific-switches" href="#Command_specific-switches"><span></span></a><a class="h" name="command_specific-switches" href="#command_specific-switches"><span></span></a><strong>Command-specific switches</strong></h4><pre class="code">  --force
      Ignores specifications of &quot;check_includes = false&quot; and checks all
      target&#39;s files that match the target label.
</pre><h4><a class="h" name="What-gets-checked" href="#What-gets-checked"><span></span></a><a class="h" name="what-gets-checked" href="#what-gets-checked"><span></span></a><strong>What gets checked</strong></h4><pre class="code">  The .gn file may specify a list of targets to be checked. Only these targets
  will be checked if no label_pattern is specified on the command line.
  Otherwise, the command-line list is used instead. See &quot;gn help dotfile&quot;.

  Targets can opt-out from checking with &quot;check_includes = false&quot; (see
  &quot;gn help check_includes&quot;).

  For targets being checked:

    - GN opens all C-like source files in the targets to be checked and scans
      the top for includes.

    - Includes with a &quot;nogncheck&quot; annotation are skipped (see
      &quot;gn help nogncheck&quot;).

    - Only includes using &quot;quotes&quot; are checked. &lt;brackets&gt; are assumed to be
      system includes.

    - Include paths are assumed to be relative to either the source root or the
      &quot;root_gen_dir&quot; and must include all the path components. (It might be
      nice in the future to incorporate GN&#39;s knowledge of the include path to
      handle other include styles.)

    - GN does not run the preprocessor so will not understand conditional
      includes.

    - Only includes matching known files in the build are checked: includes
      matching unknown paths are ignored.

  For an include to be valid:

    - The included file must be in the current target, or there must be a path
      following only public dependencies to a target with the file in it
      (&quot;gn path&quot; is a good way to diagnose problems).

    - There can be multiple targets with an included file: only one needs to be
      valid for the include to be allowed.

    - If there are only &quot;sources&quot; in a target, all are considered to be public
      and can be included by other targets with a valid public dependency path.

    - If a target lists files as &quot;public&quot;, only those files are able to be
      included by other targets. Anything in the sources will be considered
      private and will not be includable regardless of dependency paths.

    - Ouptuts from actions are treated like public sources on that target.

    - A target can include headers from a target that depends on it if the
      other target is annotated accordingly. See &quot;gn help
      allow_circular_includes_from&quot;.
</pre><h4><a class="h" name="Advice-on-fixing-problems" href="#Advice-on-fixing-problems"><span></span></a><a class="h" name="advice-on-fixing-problems" href="#advice-on-fixing-problems"><span></span></a><strong>Advice on fixing problems</strong></h4><pre class="code">  If you have a third party project that uses relative includes, it&#39;s generally
  best to exclude that target from checking altogether via
  &quot;check_includes = false&quot;.

  If you have conditional includes, make sure the build conditions and the
  preprocessor conditions match, and annotate the line with &quot;nogncheck&quot; (see
  &quot;gn help nogncheck&quot; for an example).

  If two targets are hopelessly intertwined, use the
  &quot;allow_circular_includes_from&quot; annotation. Ideally each should have identical
  dependencies so configs inherited from those dependencies are consistent (see
  &quot;gn help allow_circular_includes_from&quot;).

  If you have a standalone header file or files that need to be shared between
  a few targets, you can consider making a source_set listing only those
  headers as public sources. With only header files, the source set will be a
  no-op from a build perspective, but will give a central place to refer to
  those headers. That source set&#39;s files will still need to pass &quot;gn check&quot; in
  isolation.

  In rare cases it makes sense to list a header in more than one target if it
  could be considered conceptually a member of both.
</pre><h4><a class="h" name="Commands-gn-check-out_dir_label_pattern_force-Examples" href="#Commands-gn-check-out_dir_label_pattern_force-Examples"><span></span></a><a class="h" name="commands-gn-check-out_dir_label_pattern_force-examples" href="#commands-gn-check-out_dir_label_pattern_force-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  gn check out/Debug
      Check everything.

  gn check out/Default //foo:bar
      Check only the files in the //foo:bar target.

  gn check out/Default &quot;//foo/*
      Check only the files in targets in the //foo directory tree.
</pre><h3><a class="h" name="clean" href="#clean"><span></span></a><strong>gn clean &lt;out_dir&gt;</strong></h3><pre class="code">  Deletes the contents of the output directory except for args.gn and
  creates a Ninja build environment sufficient to regenerate the build.
</pre><h3><a class="h" name="desc" href="#desc"><span></span></a><strong>gn desc &lt;out_dir&gt;  [] [--blame] &quot;</strong></h3><h4><a class="h" name="format_json" href="#format_json"><span></span></a><strong>[--format=json]</strong></h4><pre class="code">  Displays information about a given target or config. The build build
  parameters will be taken for the build in the given &lt;out_dir&gt;.

  The &lt;label or pattern&gt; can be a target label, a config label, or a label
  pattern (see &quot;gn help label_pattern&quot;). A label pattern will only match
  targets.
</pre><h4><a class="h" name="Possibilities-for" href="#Possibilities-for"><span></span></a><a class="h" name="possibilities-for" href="#possibilities-for"><span></span></a><strong>Possibilities for </strong></h4><pre class="code">  (If unspecified an overall summary will be displayed.)

  all_dependent_configs
  allow_circular_includes_from
  arflags [--blame]
  args
  cflags [--blame]
  cflags_cc [--blame]
  cflags_cxx [--blame]
  check_includes
  configs [--tree] (see below)
  defines [--blame]
  depfile
  deps [--all] [--tree] (see below)
  include_dirs [--blame]
  inputs
  ldflags [--blame]
  lib_dirs
  libs
  outputs
  public_configs
  public
  script
  sources
  testonly
  visibility

  runtime_deps
      Compute all runtime deps for the given target. This is a computed list
      and does not correspond to any GN variable, unlike most other values
      here.

      The output is a list of file names relative to the build directory. See
      &quot;gn help runtime_deps&quot; for how this is computed. This also works with
      &quot;--blame&quot; to see the source of the dependency.
</pre><h4><a class="h" name="Shared-flags" href="#Shared-flags"><span></span></a><a class="h" name="shared-flags" href="#shared-flags"><span></span></a><strong>Shared flags</strong></h4><pre class="code">  --all-toolchains
      Normally only inputs in the default toolchain will be included.
      This switch will turn on matching all toolchains.

      For example, a file is in a target might be compiled twice:
      once in the default toolchain and once in a secondary one. Without
      this flag, only the default toolchain one will be matched by
      wildcards. With this flag, both will be matched.

  --format=json
      Format the output as JSON instead of text.
</pre><h4><a class="h" name="Target-flags" href="#Target-flags"><span></span></a><a class="h" name="target-flags" href="#target-flags"><span></span></a><strong>Target flags</strong></h4><pre class="code">  --blame
      Used with any value specified on a config, this will name the config that
      cause that target to get the flag. This doesn&#39;t currently work for libs
      and lib_dirs because those are inherited and are more complicated to
      figure out the blame (patches welcome).
</pre><h4><a class="h" name="Configs" href="#Configs"><span></span></a><a class="h" name="configs" href="#configs"><span></span></a><strong>Configs</strong></h4><pre class="code">  The &quot;configs&quot; section will list all configs that apply. For targets this will
  include configs specified in the &quot;configs&quot; variable of the target, and also
  configs pushed onto this target via public or &quot;all dependent&quot; configs.

  Configs can have child configs. Specifying --tree will show the hierarchy.
</pre><h4><a class="h" name="Printing-outputs" href="#Printing-outputs"><span></span></a><a class="h" name="printing-outputs" href="#printing-outputs"><span></span></a><strong>Printing outputs</strong></h4><pre class="code">  The &quot;outputs&quot; section will list all outputs that apply, including the outputs
  computed from the tool definition (eg for &quot;executable&quot;, &quot;static_library&quot;, ...
  targets).
</pre><h4><a class="h" name="Printing-deps" href="#Printing-deps"><span></span></a><a class="h" name="printing-deps" href="#printing-deps"><span></span></a><strong>Printing deps</strong></h4><pre class="code">  Deps will include all public, private, and data deps (TODO this could be
  clarified and enhanced) sorted in order applying. The following may be used:

  --all
      Collects all recursive dependencies and prints a sorted flat list. Also
      usable with --tree (see below).
  --as=(buildfile|label|output)
      How to print targets.

      buildfile
          Prints the build files where the given target was declared as
          file names.
      label  (default)
          Prints the label of the target.
      output
          Prints the first output file for the target relative to the
          root build directory.

  --testonly=(true|false)
      Restrict outputs to targets with the testonly flag set
      accordingly. When unspecified, the target&#39;s testonly flags are
      ignored.

  --tree
      Print a dependency tree. By default, duplicates will be elided with &quot;...&quot;
      but when --all and -tree are used together, no eliding will be performed.

      The &quot;deps&quot;, &quot;public_deps&quot;, and &quot;data_deps&quot; will all be included in the
      tree.

      Tree output can not be used with the filtering or output flags: --as,
      --type, --testonly.
  --type=(action|copy|executable|group|loadable_module|shared_library|
          source_set|static_library)
      Restrict outputs to targets matching the given type. If
      unspecified, no filtering will be performed.
</pre><h4><a class="h" name="Note" href="#Note"><span></span></a><a class="h" name="note" href="#note"><span></span></a><strong>Note</strong></h4><pre class="code">  This command will show the full name of directories and source files, but
  when directories and source paths are written to the build file, they will be
  adjusted to be relative to the build directory. So the values for paths
  displayed by this command won&#39;t match (but should mean the same thing).
</pre><h4><a class="h" name="Commands-gn-desc-out_dir_blame-Examples" href="#Commands-gn-desc-out_dir_blame-Examples"><span></span></a><a class="h" name="commands-gn-desc-out_dir_blame-examples" href="#commands-gn-desc-out_dir_blame-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  gn desc out/Debug //base:base
      Summarizes the given target.

  gn desc out/Foo :base_unittests deps --tree
      Shows a dependency tree of the &quot;base_unittests&quot; project in
      the current directory.

  gn desc out/Debug //base defines --blame
      Shows defines set for the //base:base target, annotated by where
      each one was set from.
</pre><h3><a class="h" name="format" href="#format"><span></span></a><strong>gn format [--dump-tree] (--stdin | &lt;build_file&gt;)</strong></h3><pre class="code">  Formats .gn file to a standard format.

  The contents of some lists (&#39;sources&#39;, &#39;deps&#39;, etc.) will be sorted to a
  canonical order. To suppress this, you can add a comment of the form &quot;#
  NOSORT&quot; immediately preceeding the assignment. e.g.

  # NOSORT
  sources = [
    &quot;z.cc&quot;,
    &quot;a.cc&quot;,
  ]
</pre><h4><a class="h" name="Commands-gn-format-dump_tree_stdin-build_file-Arguments" href="#Commands-gn-format-dump_tree_stdin-build_file-Arguments"><span></span></a><a class="h" name="commands-gn-format-dump_tree_stdin-build_file-arguments" href="#commands-gn-format-dump_tree_stdin-build_file-arguments"><span></span></a><strong>Arguments</strong></h4><pre class="code">  --dry-run
      Does not change or output anything, but sets the process exit code based
      on whether output would be different than what&#39;s on disk. This is useful
      for presubmit/lint-type checks.
      - Exit code 0: successful format, matches on disk.
      - Exit code 1: general failure (parse error, etc.)
      - Exit code 2: successful format, but differs from on disk.

  --dump-tree
      For debugging, dumps the parse tree to stdout and does not update the
      file or print formatted output.

  --stdin
      Read input from stdin and write to stdout rather than update a file
      in-place.
</pre><h4><a class="h" name="Commands-gn-format-dump_tree_stdin-build_file-Examples" href="#Commands-gn-format-dump_tree_stdin-build_file-Examples"><span></span></a><a class="h" name="commands-gn-format-dump_tree_stdin-build_file-examples" href="#commands-gn-format-dump_tree_stdin-build_file-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  gn format //some/BUILD.gn
  gn format some\\BUILD.gn
  gn format /abspath/some/BUILD.gn
  gn format --stdin
</pre><h3><a class="h" name="gen" href="#gen"><span></span></a><strong>gn gen [--check] [] &lt;out_dir&gt;</strong></h3><pre class="code">  Generates ninja files from the current tree and puts them in the given output
  directory.

  The output directory can be a source-repo-absolute path name such as:
      //out/foo
  Or it can be a directory relative to the current directory such as:
      out/foo

  &quot;gn gen --check&quot; is the same as running &quot;gn check&quot;. See &quot;gn help check&quot;
  for documentation on that mode.

  See &quot;gn help switches&quot; for the common command-line switches.
</pre><h4><a class="h" name="IDE-options" href="#IDE-options"><span></span></a><a class="h" name="ide-options" href="#ide-options"><span></span></a><strong>IDE options</strong></h4><pre class="code">  GN optionally generates files for IDE. Possibilities for &lt;ide options&gt;

  --ide=&lt;ide_name&gt;
      Generate files for an IDE. Currently supported values:
      &quot;eclipse&quot; - Eclipse CDT settings file.
      &quot;vs&quot; - Visual Studio project/solution files.
             (default Visual Studio version: 2015)
      &quot;vs2013&quot; - Visual Studio 2013 project/solution files.
      &quot;vs2015&quot; - Visual Studio 2015 project/solution files.
      &quot;vs2017&quot; - Visual Studio 2017 project/solution files.
      &quot;xcode&quot; - Xcode workspace/solution files.
      &quot;qtcreator&quot; - QtCreator project files.
      &quot;json&quot; - JSON file containing target information

  --filters=&lt;path_prefixes&gt;
      Semicolon-separated list of label patterns used to limit the set of
      generated projects (see &quot;gn help label_pattern&quot;). Only matching targets
      and their dependencies will be included in the solution. Only used for
      Visual Studio, Xcode and JSON.
</pre><h4><a class="h" name="Visual-Studio-Flags" href="#Visual-Studio-Flags"><span></span></a><a class="h" name="visual-studio-flags" href="#visual-studio-flags"><span></span></a><strong>Visual Studio Flags</strong></h4><pre class="code">  --sln=&lt;file_name&gt;
      Override default sln file name (&quot;all&quot;). Solution file is written to the
      root build directory.

  --no-deps
      Don&#39;t include targets dependencies to the solution. Changes the way how
      --filters option works. Only directly matching targets are included.

  --winsdk=&lt;sdk_version&gt;
      Use the specified Windows 10 SDK version to generate project files.
      As an example, &quot;10.0.15063.0&quot; can be specified to use Creators Update SDK
      instead of the default one.
</pre><h4><a class="h" name="Xcode-Flags" href="#Xcode-Flags"><span></span></a><a class="h" name="xcode-flags" href="#xcode-flags"><span></span></a><strong>Xcode Flags</strong></h4><pre class="code">  --workspace=&lt;file_name&gt;
      Override defaut workspace file name (&quot;all&quot;). The workspace file is
      written to the root build directory.

  --ninja-extra-args=&lt;string&gt;
      This string is passed without any quoting to the ninja invocation
      command-line. Can be used to configure ninja flags, like &quot;-j&quot; if using
      goma for example.

  --root-target=&lt;target_name&gt;
      Name of the target corresponding to &quot;All&quot; target in Xcode. If unset,
      &quot;All&quot; invokes ninja without any target and builds everything.
</pre><h4><a class="h" name="QtCreator-Flags" href="#QtCreator-Flags"><span></span></a><a class="h" name="qtcreator-flags" href="#qtcreator-flags"><span></span></a><strong>QtCreator Flags</strong></h4><pre class="code">  --root-target=&lt;target_name&gt;
      Name of the root target for which the QtCreator project will be generated
      to contain files of it and its dependencies. If unset, the whole build
      graph will be emitted.
</pre><h4><a class="h" name="Eclipse-IDE-Support" href="#Eclipse-IDE-Support"><span></span></a><a class="h" name="eclipse-ide-support" href="#eclipse-ide-support"><span></span></a><strong>Eclipse IDE Support</strong></h4><pre class="code">  GN DOES NOT generate Eclipse CDT projects. Instead, it generates a settings
  file which can be imported into an Eclipse CDT project. The XML file contains
  a list of include paths and defines. Because GN does not generate a full
  .cproject definition, it is not possible to properly define includes/defines
  for each file individually. Instead, one set of includes/defines is generated
  for the entire project. This works fairly well but may still result in a few
  indexer issues here and there.
</pre><h4><a class="h" name="Generic-JSON-Output" href="#Generic-JSON-Output"><span></span></a><a class="h" name="generic-json-output" href="#generic-json-output"><span></span></a><strong>Generic JSON Output</strong></h4><pre class="code">  Dumps target information to a JSON file and optionally invokes a
  python script on the generated file. See the comments at the beginning
  of json_project_writer.cc and desc_builder.cc for an overview of the JSON
  file format.

  --json-file-name=&lt;json_file_name&gt;
      Overrides default file name (project.json) of generated JSON file.

  --json-ide-script=&lt;path_to_python_script&gt;
      Executes python script after the JSON file is generated. Path can be
      project absolute (//), system absolute (/) or relative, in which case the
      output directory will be base. Path to generated JSON file will be first
      argument when invoking script.

  --json-ide-script-args=&lt;argument&gt;
      Optional second argument that will passed to executed script.
</pre><h3><a class="h" name="help" href="#help"><span></span></a><strong>gn help </strong></h3><pre class="code">  Yo dawg, I heard you like help on your help so I put help on the help in the
  help.

  You can also use &quot;all&quot; as the parameter to get all help at once.
</pre><h4><a class="h" name="Switches" href="#Switches"><span></span></a><a class="h" name="switches" href="#switches"><span></span></a><strong>Switches</strong></h4><pre class="code">  --markdown
      Format output in markdown syntax.
</pre><h4><a class="h" name="Commands-gn-help-Example" href="#Commands-gn-help-Example"><span></span></a><a class="h" name="commands-gn-help-example" href="#commands-gn-help-example"><span></span></a><strong>Example</strong></h4><pre class="code">  gn help --markdown all
      Dump all help to stdout in markdown format.
</pre><h3><a class="h" name="ls" href="#ls"><span></span></a><strong>gn ls &lt;out_dir&gt; [&lt;label_pattern&gt;] [--all-toolchains] [--as=...]</strong></h3><pre class="code">      [--type=...] [--testonly=...]

  Lists all targets matching the given pattern for the given build directory.
  By default, only targets in the default toolchain will be matched unless a
  toolchain is explicitly supplied.

  If the label pattern is unspecified, list all targets. The label pattern is
  not a general regular expression (see &quot;gn help label_pattern&quot;). If you need
  more complex expressions, pipe the result through grep.
</pre><h4><a class="h" name="Commands-gn-ls-out_dir_label_pattern_all_toolchains_as-Options" href="#Commands-gn-ls-out_dir_label_pattern_all_toolchains_as-Options"><span></span></a><a class="h" name="commands-gn-ls-out_dir_label_pattern_all_toolchains_as-options" href="#commands-gn-ls-out_dir_label_pattern_all_toolchains_as-options"><span></span></a><strong>Options</strong></h4><pre class="code">  --as=(buildfile|label|output)
      How to print targets.

      buildfile
          Prints the build files where the given target was declared as
          file names.
      label  (default)
          Prints the label of the target.
      output
          Prints the first output file for the target relative to the
          root build directory.

  --all-toolchains
      Normally only inputs in the default toolchain will be included.
      This switch will turn on matching all toolchains.

      For example, a file is in a target might be compiled twice:
      once in the default toolchain and once in a secondary one. Without
      this flag, only the default toolchain one will be matched by
      wildcards. With this flag, both will be matched.

  --testonly=(true|false)
      Restrict outputs to targets with the testonly flag set
      accordingly. When unspecified, the target&#39;s testonly flags are
      ignored.

  --type=(action|copy|executable|group|loadable_module|shared_library|
          source_set|static_library)
      Restrict outputs to targets matching the given type. If
      unspecified, no filtering will be performed.
</pre><h4><a class="h" name="Commands-gn-ls-out_dir_label_pattern_all_toolchains_as-Examples" href="#Commands-gn-ls-out_dir_label_pattern_all_toolchains_as-Examples"><span></span></a><a class="h" name="commands-gn-ls-out_dir_label_pattern_all_toolchains_as-examples" href="#commands-gn-ls-out_dir_label_pattern_all_toolchains_as-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  gn ls out/Debug
      Lists all targets in the default toolchain.

  gn ls out/Debug &quot;//base/*&quot;
      Lists all targets in the directory base and all subdirectories.

  gn ls out/Debug &quot;//base:*&quot;
      Lists all targets defined in //base/BUILD.gn.

  gn ls out/Debug //base --as=output
      Lists the build output file for //base:base

  gn ls out/Debug --type=executable
      Lists all executables produced by the build.

  gn ls out/Debug &quot;//base/*&quot; --as=output | xargs ninja -C out/Debug
      Builds all targets in //base and all subdirectories.

  gn ls out/Debug //base --all-toolchains
      Lists all variants of the target //base:base (it may be referenced
      in multiple toolchains).
</pre><h3><a class="h" name="path" href="#path"><span></span></a><strong>gn path &lt;out_dir&gt; &lt;target_one&gt; &lt;target_two&gt;</strong></h3><pre class="code">  Finds paths of dependencies between two targets. Each unique path will be
  printed in one group, and groups will be separate by newlines. The two
  targets can appear in either order (paths will be found going in either
  direction).

  By default, a single path will be printed. If there is a path with only
  public dependencies, the shortest public path will be printed. Otherwise, the
  shortest path using either public or private dependencies will be printed. If
  --with-data is specified, data deps will also be considered. If there are
  multiple shortest paths, an arbitrary one will be selected.
</pre><h4><a class="h" name="Interesting-paths" href="#Interesting-paths"><span></span></a><a class="h" name="interesting-paths" href="#interesting-paths"><span></span></a><strong>Interesting paths</strong></h4><pre class="code">  In a large project, there can be 100&#39;s of millions of unique paths between a
  very high level and a common low-level target. To make the output more useful
  (and terminate in a reasonable time), GN will not revisit sub-paths
  previously known to lead to the target.
</pre><h4><a class="h" name="Commands-gn-path-out_dir_target_one_target_two-Options" href="#Commands-gn-path-out_dir_target_one_target_two-Options"><span></span></a><a class="h" name="commands-gn-path-out_dir_target_one_target_two-options" href="#commands-gn-path-out_dir_target_one_target_two-options"><span></span></a><strong>Options</strong></h4><pre class="code">  --all
     Prints all &quot;interesting&quot; paths found rather than just the first one.
     Public paths will be printed first in order of increasing length, followed
     by non-public paths in order of increasing length.

  --public
     Considers only public paths. Can&#39;t be used with --with-data.

  --with-data
     Additionally follows data deps. Without this flag, only public and private
     linked deps will be followed. Can&#39;t be used with --public.
</pre><h4><a class="h" name="Commands-gn-path-out_dir_target_one_target_two-Example" href="#Commands-gn-path-out_dir_target_one_target_two-Example"><span></span></a><a class="h" name="commands-gn-path-out_dir_target_one_target_two-example" href="#commands-gn-path-out_dir_target_one_target_two-example"><span></span></a><strong>Example</strong></h4><pre class="code">  gn path out/Default //base //tools/gn
</pre><h3><a class="h" name="refs" href="#refs"><span></span></a><strong>gn refs &lt;out_dir&gt; (&lt;label_pattern&gt;|||@&lt;response_file&gt;)</strong>*</h3><pre class="code">        [--all] [--all-toolchains] [--as=...] [--testonly=...] [--type=...]

  Finds reverse dependencies (which targets reference something). The input is
  a list containing:

   - Target label: The result will be which targets depend on it.

   - Config label: The result will be which targets list the given config in
     its &quot;configs&quot; or &quot;public_configs&quot; list.

   - Label pattern: The result will be which targets depend on any target
     matching the given pattern. Patterns will not match configs. These are not
     general regular expressions, see &quot;gn help label_pattern&quot; for details.

   - File name: The result will be which targets list the given file in its
     &quot;inputs&quot;, &quot;sources&quot;, &quot;public&quot;, &quot;data&quot;, or &quot;outputs&quot;. Any input that does
     not contain wildcards and does not match a target or a config will be
     treated as a file.

   - Response file: If the input starts with an &quot;@&quot;, it will be interpreted as
     a path to a file containing a list of labels or file names, one per line.
     This allows us to handle long lists of inputs without worrying about
     command line limits.
</pre><h4><a class="h" name="Commands-gn-refs-out_dir_label_pattern_response_file-Options" href="#Commands-gn-refs-out_dir_label_pattern_response_file-Options"><span></span></a><a class="h" name="commands-gn-refs-out_dir_label_pattern_response_file-options" href="#commands-gn-refs-out_dir_label_pattern_response_file-options"><span></span></a><strong>Options</strong></h4><pre class="code">  --all
      When used without --tree, will recurse and display all unique
      dependencies of the given targets. For example, if the input is a target,
      this will output all targets that depend directly or indirectly on the
      input. If the input is a file, this will output all targets that depend
      directly or indirectly on that file.

      When used with --tree, turns off eliding to show a complete tree.
  --all-toolchains
      Normally only inputs in the default toolchain will be included.
      This switch will turn on matching all toolchains.

      For example, a file is in a target might be compiled twice:
      once in the default toolchain and once in a secondary one. Without
      this flag, only the default toolchain one will be matched by
      wildcards. With this flag, both will be matched.

  --as=(buildfile|label|output)
      How to print targets.

      buildfile
          Prints the build files where the given target was declared as
          file names.
      label  (default)
          Prints the label of the target.
      output
          Prints the first output file for the target relative to the
          root build directory.

  -q
     Quiet. If nothing matches, don&#39;t print any output. Without this option, if
     there are no matches there will be an informational message printed which
     might interfere with scripts processing the output.
  --testonly=(true|false)
      Restrict outputs to targets with the testonly flag set
      accordingly. When unspecified, the target&#39;s testonly flags are
      ignored.

  --tree
      Outputs a reverse dependency tree from the given target. Duplicates will
      be elided. Combine with --all to see a full dependency tree.

      Tree output can not be used with the filtering or output flags: --as,
      --type, --testonly.
  --type=(action|copy|executable|group|loadable_module|shared_library|
          source_set|static_library)
      Restrict outputs to targets matching the given type. If
      unspecified, no filtering will be performed.
</pre><h4><a class="h" name="Examples-target-input" href="#Examples-target-input"><span></span></a><a class="h" name="examples-target-input" href="#examples-target-input"><span></span></a><strong>Examples (target input)</strong></h4><pre class="code">  gn refs out/Debug //tools/gn:gn
      Find all targets depending on the given exact target name.

  gn refs out/Debug //base:i18n --as=buildfiles | xargs gvim
      Edit all .gn files containing references to //base:i18n

  gn refs out/Debug //base --all
      List all targets depending directly or indirectly on //base:base.

  gn refs out/Debug &quot;//base/*&quot;
      List all targets depending directly on any target in //base or
      its subdirectories.

  gn refs out/Debug &quot;//base:*&quot;
      List all targets depending directly on any target in
      //base/BUILD.gn.

  gn refs out/Debug //base --tree
      Print a reverse dependency tree of //base:base
</pre><h4><a class="h" name="Examples-file-input" href="#Examples-file-input"><span></span></a><a class="h" name="examples-file-input" href="#examples-file-input"><span></span></a><strong>Examples (file input)</strong></h4><pre class="code">  gn refs out/Debug //base/macros.h
      Print target(s) listing //base/macros.h as a source.

  gn refs out/Debug //base/macros.h --tree
      Display a reverse dependency tree to get to the given file. This
      will show how dependencies will reference that file.

  gn refs out/Debug //base/macros.h //base/at_exit.h --all
      Display all unique targets with some dependency path to a target
      containing either of the given files as a source.

  gn refs out/Debug //base/macros.h --testonly=true --type=executable
          --all --as=output
      Display the executable file names of all test executables
      potentially affected by a change to the given file.
</pre><h2><a class="h" name="targets" href="#targets"><span></span></a>Target declarations</h2><h3><a class="h" name="action" href="#action"><span></span></a><strong>action</strong>: Declare a target that runs a script a single time.</h3><pre class="code">  This target type allows you to run a script a single time to produce one or
  more output files. If you want to run a script once for each of a set of
  input files, see &quot;gn help action_foreach&quot;.
</pre><h4><a class="h" name="Target-declarations-action_Declare-a-target-that-runs-a-script-a-single-time-Inputs" href="#Target-declarations-action_Declare-a-target-that-runs-a-script-a-single-time-Inputs"><span></span></a><a class="h" name="target-declarations-action_declare-a-target-that-runs-a-script-a-single-time-inputs" href="#target-declarations-action_declare-a-target-that-runs-a-script-a-single-time-inputs"><span></span></a><strong>Inputs</strong></h4><pre class="code">  In an action the &quot;sources&quot; and &quot;inputs&quot; are treated the same: they&#39;re both
  input dependencies on script execution with no special handling. If you want
  to pass the sources to your script, you must do so explicitly by including
  them in the &quot;args&quot;. Note also that this means there is no special handling of
  paths since GN doesn&#39;t know which of the args are paths and not. You will
  want to use rebase_path() to convert paths to be relative to the
  root_build_dir.

  You can dynamically write input dependencies (for incremental rebuilds if an
  input file changes) by writing a depfile when the script is run (see &quot;gn help
  depfile&quot;). This is more flexible than &quot;inputs&quot;.

  If the command line length is very long, you can use response files to pass
  args to your script. See &quot;gn help response_file_contents&quot;.

  It is recommended you put inputs to your script in the &quot;sources&quot; variable,
  and stuff like other Python files required to run your script in the &quot;inputs&quot;
  variable.
  The &quot;deps&quot; and &quot;public_deps&quot; for an action will always be
  completed before any part of the action is run so it can depend on
  the output of previous steps. The &quot;data_deps&quot; will be built if the
  action is built, but may not have completed before all steps of the
  action are started. This can give additional parallelism in the build
  for runtime-only dependencies.
</pre><h4><a class="h" name="Target-declarations-action_Declare-a-target-that-runs-a-script-a-single-time-Outputs" href="#Target-declarations-action_Declare-a-target-that-runs-a-script-a-single-time-Outputs"><span></span></a><a class="h" name="target-declarations-action_declare-a-target-that-runs-a-script-a-single-time-outputs" href="#target-declarations-action_declare-a-target-that-runs-a-script-a-single-time-outputs"><span></span></a><strong>Outputs</strong></h4><pre class="code">  You should specify files created by your script by specifying them in the
  &quot;outputs&quot;.
  The script will be executed with the given arguments with the current
  directory being that of the root build directory. If you pass files
  to your script, see &quot;gn help rebase_path&quot; for how to convert
  file names to be relative to the build directory (file names in the
  sources, outputs, and inputs will be all treated as relative to the
  current build file and converted as needed automatically).
</pre><h4><a class="h" name="Target-declarations-action_Declare-a-target-that-runs-a-script-a-single-time-File-name-handling" href="#Target-declarations-action_Declare-a-target-that-runs-a-script-a-single-time-File-name-handling"><span></span></a><a class="h" name="target-declarations-action_declare-a-target-that-runs-a-script-a-single-time-file-name-handling" href="#target-declarations-action_declare-a-target-that-runs-a-script-a-single-time-file-name-handling"><span></span></a><strong>File name handling</strong></h4><pre class="code">  All output files must be inside the output directory of the build.
  You would generally use |$target_out_dir| or |$target_gen_dir| to
  reference the output or generated intermediate file directories,
  respectively.
</pre><h4><a class="h" name="Target-declarations-action_Declare-a-target-that-runs-a-script-a-single-time-Variables" href="#Target-declarations-action_Declare-a-target-that-runs-a-script-a-single-time-Variables"><span></span></a><a class="h" name="target-declarations-action_declare-a-target-that-runs-a-script-a-single-time-variables" href="#target-declarations-action_declare-a-target-that-runs-a-script-a-single-time-variables"><span></span></a><strong>Variables</strong></h4><pre class="code">  args, data, data_deps, depfile, deps, inputs, outputs*, pool,
  response_file_contents, script*, sources
  * = required
</pre><h4><a class="h" name="Target-declarations-action_Declare-a-target-that-runs-a-script-a-single-time-Example" href="#Target-declarations-action_Declare-a-target-that-runs-a-script-a-single-time-Example"><span></span></a><a class="h" name="target-declarations-action_declare-a-target-that-runs-a-script-a-single-time-example" href="#target-declarations-action_declare-a-target-that-runs-a-script-a-single-time-example"><span></span></a><strong>Example</strong></h4><pre class="code">  action(&quot;run_this_guy_once&quot;) {
    script = &quot;doprocessing.py&quot;
    sources = [ &quot;my_configuration.txt&quot; ]
    outputs = [ &quot;$target_gen_dir/insightful_output.txt&quot; ]

    # Our script imports this Python file so we want to rebuild if it changes.
    inputs = [ &quot;helper_library.py&quot; ]

    # Note that we have to manually pass the sources to our script if the
    # script needs them as inputs.
    args = [ &quot;--out&quot;, rebase_path(target_gen_dir, root_build_dir) ] +
           rebase_path(sources, root_build_dir)
  }
</pre><h3><a class="h" name="action_foreach" href="#action_foreach"><span></span></a><strong>action_foreach</strong>: Declare a target that runs a script over a set of files.</h3><pre class="code">  This target type allows you to run a script once-per-file over a set of
  sources. If you want to run a script once that takes many files as input, see
  &quot;gn help action&quot;.
</pre><h4><a class="h" name="Target-declarations-action_foreach_Declare-a-target-that-runs-a-script-over-a-set-of-files-Inputs" href="#Target-declarations-action_foreach_Declare-a-target-that-runs-a-script-over-a-set-of-files-Inputs"><span></span></a><a class="h" name="target-declarations-action_foreach_declare-a-target-that-runs-a-script-over-a-set-of-files-inputs" href="#target-declarations-action_foreach_declare-a-target-that-runs-a-script-over-a-set-of-files-inputs"><span></span></a><strong>Inputs</strong></h4><pre class="code">  The script will be run once per file in the &quot;sources&quot; variable. The &quot;outputs&quot;
  variable should specify one or more files with a source expansion pattern in
  it (see &quot;gn help source_expansion&quot;). The output file(s) for each script
  invocation should be unique. Normally you use &quot;{{source_name_part}}&quot; in each
  output file.

  If your script takes additional data as input, such as a shared configuration
  file or a Python module it uses, those files should be listed in the &quot;inputs&quot;
  variable. These files are treated as dependencies of each script invocation.

  If the command line length is very long, you can use response files to pass
  args to your script. See &quot;gn help response_file_contents&quot;.

  You can dynamically write input dependencies (for incremental rebuilds if an
  input file changes) by writing a depfile when the script is run (see &quot;gn help
  depfile&quot;). This is more flexible than &quot;inputs&quot;.
  The &quot;deps&quot; and &quot;public_deps&quot; for an action will always be
  completed before any part of the action is run so it can depend on
  the output of previous steps. The &quot;data_deps&quot; will be built if the
  action is built, but may not have completed before all steps of the
  action are started. This can give additional parallelism in the build
  for runtime-only dependencies.
</pre><h4><a class="h" name="Target-declarations-action_foreach_Declare-a-target-that-runs-a-script-over-a-set-of-files-Outputs" href="#Target-declarations-action_foreach_Declare-a-target-that-runs-a-script-over-a-set-of-files-Outputs"><span></span></a><a class="h" name="target-declarations-action_foreach_declare-a-target-that-runs-a-script-over-a-set-of-files-outputs" href="#target-declarations-action_foreach_declare-a-target-that-runs-a-script-over-a-set-of-files-outputs"><span></span></a><strong>Outputs</strong></h4><pre class="code">  The script will be executed with the given arguments with the current
  directory being that of the root build directory. If you pass files
  to your script, see &quot;gn help rebase_path&quot; for how to convert
  file names to be relative to the build directory (file names in the
  sources, outputs, and inputs will be all treated as relative to the
  current build file and converted as needed automatically).
</pre><h4><a class="h" name="Target-declarations-action_foreach_Declare-a-target-that-runs-a-script-over-a-set-of-files-File-name-handling" href="#Target-declarations-action_foreach_Declare-a-target-that-runs-a-script-over-a-set-of-files-File-name-handling"><span></span></a><a class="h" name="target-declarations-action_foreach_declare-a-target-that-runs-a-script-over-a-set-of-files-file-name-handling" href="#target-declarations-action_foreach_declare-a-target-that-runs-a-script-over-a-set-of-files-file-name-handling"><span></span></a><strong>File name handling</strong></h4><pre class="code">  All output files must be inside the output directory of the build.
  You would generally use |$target_out_dir| or |$target_gen_dir| to
  reference the output or generated intermediate file directories,
  respectively.
</pre><h4><a class="h" name="Target-declarations-action_foreach_Declare-a-target-that-runs-a-script-over-a-set-of-files-Variables" href="#Target-declarations-action_foreach_Declare-a-target-that-runs-a-script-over-a-set-of-files-Variables"><span></span></a><a class="h" name="target-declarations-action_foreach_declare-a-target-that-runs-a-script-over-a-set-of-files-variables" href="#target-declarations-action_foreach_declare-a-target-that-runs-a-script-over-a-set-of-files-variables"><span></span></a><strong>Variables</strong></h4><pre class="code">  args, data, data_deps, depfile, deps, inputs, outputs*, pool,
  response_file_contents, script*, sources*
  * = required
</pre><h4><a class="h" name="Target-declarations-action_foreach_Declare-a-target-that-runs-a-script-over-a-set-of-files-Example" href="#Target-declarations-action_foreach_Declare-a-target-that-runs-a-script-over-a-set-of-files-Example"><span></span></a><a class="h" name="target-declarations-action_foreach_declare-a-target-that-runs-a-script-over-a-set-of-files-example" href="#target-declarations-action_foreach_declare-a-target-that-runs-a-script-over-a-set-of-files-example"><span></span></a><strong>Example</strong></h4><pre class="code">  # Runs the script over each IDL file. The IDL script will generate both a .cc
  # and a .h file for each input.
  action_foreach(&quot;my_idl&quot;) {
    script = &quot;idl_processor.py&quot;
    sources = [ &quot;foo.idl&quot;, &quot;bar.idl&quot; ]

    # Our script reads this file each time, so we need to list is as a
    # dependency so we can rebuild if it changes.
    inputs = [ &quot;my_configuration.txt&quot; ]

    # Transformation from source file name to output file names.
    outputs = [ &quot;$target_gen_dir/{{source_name_part}}.h&quot;,
                &quot;$target_gen_dir/{{source_name_part}}.cc&quot; ]

    # Note that since &quot;args&quot; is opaque to GN, if you specify paths here, you
    # will need to convert it to be relative to the build directory using
    # rebase_path().
    args = [
      &quot;{{source}}&quot;,
      &quot;-o&quot;,
      rebase_path(relative_target_gen_dir, root_build_dir) +
        &quot;/{{source_name_part}}.h&quot; ]
  }
</pre><h3><a class="h" name="bundle_data" href="#bundle_data"><span></span></a><strong>bundle_data</strong>: [iOS/macOS] Declare a target without output.</h3><pre class="code">  This target type allows to declare data that is required at runtime. It is
  used to inform &quot;create_bundle&quot; targets of the files to copy into generated
  bundle, see &quot;gn help create_bundle&quot; for help.

  The target must define a list of files as &quot;sources&quot; and a single &quot;outputs&quot;.
  If there are multiple files, source expansions must be used to express the
  output. The output must reference a file inside of {{bundle_root_dir}}.

  This target can be used on all platforms though it is designed only to
  generate iOS/macOS bundle. In cross-platform projects, it is advised to put it
  behind iOS/macOS conditionals.

  See &quot;gn help create_bundle&quot; for more information.
</pre><h4><a class="h" name="Target-declarations-bundle_data_iOS_macOS_Declare-a-target-without-output-Variables" href="#Target-declarations-bundle_data_iOS_macOS_Declare-a-target-without-output-Variables"><span></span></a><a class="h" name="target-declarations-bundle_data_ios_macos_declare-a-target-without-output-variables" href="#target-declarations-bundle_data_ios_macos_declare-a-target-without-output-variables"><span></span></a><strong>Variables</strong></h4><pre class="code">  sources*, outputs*, deps, data_deps, public_deps, visibility
  * = required
</pre><h4><a class="h" name="Target-declarations-bundle_data_iOS_macOS_Declare-a-target-without-output-Examples" href="#Target-declarations-bundle_data_iOS_macOS_Declare-a-target-without-output-Examples"><span></span></a><a class="h" name="target-declarations-bundle_data_ios_macos_declare-a-target-without-output-examples" href="#target-declarations-bundle_data_ios_macos_declare-a-target-without-output-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  bundle_data(&quot;icudata&quot;) {
    sources = [ &quot;sources/data/in/icudtl.dat&quot; ]
    outputs = [ &quot;{{bundle_resources_dir}}/{{source_file_part}}&quot; ]
  }

  bundle_data(&quot;base_unittests_bundle_data]&quot;) {
    sources = [ &quot;test/data&quot; ]
    outputs = [
      &quot;{{bundle_resources_dir}}/{{source_root_relative_dir}}/&quot; +
          &quot;{{source_file_part}}&quot;
    ]
  }

  bundle_data(&quot;material_typography_bundle_data&quot;) {
    sources = [
      &quot;src/MaterialTypography.bundle/Roboto-Bold.ttf&quot;,
      &quot;src/MaterialTypography.bundle/Roboto-Italic.ttf&quot;,
      &quot;src/MaterialTypography.bundle/Roboto-Regular.ttf&quot;,
      &quot;src/MaterialTypography.bundle/Roboto-Thin.ttf&quot;,
    ]
    outputs = [
      &quot;{{bundle_resources_dir}}/MaterialTypography.bundle/&quot;
          &quot;{{source_file_part}}&quot;
    ]
  }
</pre><h3><a class="h" name="copy" href="#copy"><span></span></a><strong>copy</strong>: Declare a target that copies files.</h3><h4><a class="h" name="Target-declarations-copy_Declare-a-target-that-copies-files-File-name-handling" href="#Target-declarations-copy_Declare-a-target-that-copies-files-File-name-handling"><span></span></a><a class="h" name="target-declarations-copy_declare-a-target-that-copies-files-file-name-handling" href="#target-declarations-copy_declare-a-target-that-copies-files-file-name-handling"><span></span></a><strong>File name handling</strong></h4><pre class="code">  All output files must be inside the output directory of the build. You would
  generally use |$target_out_dir| or |$target_gen_dir| to reference the output
  or generated intermediate file directories, respectively.

  Both &quot;sources&quot; and &quot;outputs&quot; must be specified. Sources can include as many
  files as you want, but there can only be one item in the outputs list (plural
  is used for the name for consistency with other target types).

  If there is more than one source file, your output name should specify a
  mapping from each source file to an output file name using source expansion
  (see &quot;gn help source_expansion&quot;). The placeholders will look like
  &quot;{{source_name_part}}&quot;, for example.
</pre><h4><a class="h" name="Target-declarations-copy_Declare-a-target-that-copies-files-Examples" href="#Target-declarations-copy_Declare-a-target-that-copies-files-Examples"><span></span></a><a class="h" name="target-declarations-copy_declare-a-target-that-copies-files-examples" href="#target-declarations-copy_declare-a-target-that-copies-files-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  # Write a rule that copies a checked-in DLL to the output directory.
  copy(&quot;mydll&quot;) {
    sources = [ &quot;mydll.dll&quot; ]
    outputs = [ &quot;$target_out_dir/mydll.dll&quot; ]
  }

  # Write a rule to copy several files to the target generated files directory.
  copy(&quot;myfiles&quot;) {
    sources = [ &quot;data1.dat&quot;, &quot;data2.dat&quot;, &quot;data3.dat&quot; ]

    # Use source expansion to generate output files with the corresponding file
    # names in the gen dir. This will just copy each file.
    outputs = [ &quot;$target_gen_dir/{{source_file_part}}&quot; ]
  }
</pre><h3><a class="h" name="create_bundle" href="#create_bundle"><span></span></a><strong>create_bundle</strong>: [ios/macOS] Build an iOS or macOS bundle.</h3><pre class="code">  This target generates an iOS or macOS bundle (which is a directory with a
  well-know structure). This target does not define any sources, instead they
  are computed from all &quot;bundle_data&quot; target this one depends on transitively
  (the recursion stops at &quot;create_bundle&quot; targets).

  The &quot;bundle_*_dir&quot; properties must be defined. They will be used for the
  expansion of {{bundle_*_dir}} rules in &quot;bundle_data&quot; outputs.

  This target can be used on all platforms though it is designed only to
  generate iOS or macOS bundle. In cross-platform projects, it is advised to put
  it behind iOS/macOS conditionals.

  If a create_bundle is specified as a data_deps for another target, the bundle
  is considered a leaf, and its public and private dependencies will not
  contribute to any data or data_deps. Required runtime dependencies should be
  placed in the bundle. A create_bundle can declare its own explicit data and
  data_deps, however.
</pre><h4><a class="h" name="Code-signing" href="#Code-signing"><span></span></a><a class="h" name="code-signing" href="#code-signing"><span></span></a><strong>Code signing</strong></h4><pre class="code">  Some bundle needs to be code signed as part of the build (on iOS all
  application needs to be code signed to run on a device). The code signature
  can be configured via the code_signing_script variable.

  If set, code_signing_script is the path of a script that invoked after all
  files have been moved into the bundle. The script must not change any file in
  the bundle, but may add new files.

  If code_signing_script is defined, then code_signing_outputs must also be
  defined and non-empty to inform when the script needs to be re-run. The
  code_signing_args will be passed as is to the script (so path have to be
  rebased) and additional inputs may be listed with the variable
  code_signing_sources.
</pre><h4><a class="h" name="Target-declarations-create_bundle_ios_macOS_Build-an-iOS-or-macOS-bundle-Variables" href="#Target-declarations-create_bundle_ios_macOS_Build-an-iOS-or-macOS-bundle-Variables"><span></span></a><a class="h" name="target-declarations-create_bundle_ios_macos_build-an-ios-or-macos-bundle-variables" href="#target-declarations-create_bundle_ios_macos_build-an-ios-or-macos-bundle-variables"><span></span></a><strong>Variables</strong></h4><pre class="code">  bundle_root_dir*, bundle_contents_dir*, bundle_resources_dir*,
  bundle_executable_dir*, bundle_plugins_dir*, bundle_deps_filter, deps,
  data_deps, public_deps, visibility, product_type, code_signing_args,
  code_signing_script, code_signing_sources, code_signing_outputs,
  xcode_extra_attributes, xcode_test_application_name, partial_info_plist
  * = required
</pre><h4><a class="h" name="Target-declarations-create_bundle_ios_macOS_Build-an-iOS-or-macOS-bundle-Example" href="#Target-declarations-create_bundle_ios_macOS_Build-an-iOS-or-macOS-bundle-Example"><span></span></a><a class="h" name="target-declarations-create_bundle_ios_macos_build-an-ios-or-macos-bundle-example" href="#target-declarations-create_bundle_ios_macos_build-an-ios-or-macos-bundle-example"><span></span></a><strong>Example</strong></h4><pre class="code">  # Defines a template to create an application. On most platform, this is just
  # an alias for an &quot;executable&quot; target, but on iOS/macOS, it builds an
  # application bundle.
  template(&quot;app&quot;) {
    if (!is_ios &amp;&amp; !is_mac) {
      executable(target_name) {
        forward_variables_from(invoker, &quot;*&quot;)
      }
    } else {
      app_name = target_name
      gen_path = target_gen_dir

      action(&quot;${app_name}_generate_info_plist&quot;) {
        script = [ &quot;//build/ios/ios_gen_plist.py&quot; ]
        sources = [ &quot;templates/Info.plist&quot; ]
        outputs = [ &quot;$gen_path/Info.plist&quot; ]
        args = rebase_path(sources, root_build_dir) +
               rebase_path(outputs, root_build_dir)
      }

      bundle_data(&quot;${app_name}_bundle_info_plist&quot;) {
        deps = [ &quot;:${app_name}_generate_info_plist&quot; ]
        sources = [ &quot;$gen_path/Info.plist&quot; ]
        outputs = [ &quot;{{bundle_contents_dir}}/Info.plist&quot; ]
      }

      executable(&quot;${app_name}_generate_executable&quot;) {
        forward_variables_from(invoker, &quot;*&quot;, [
                                               &quot;output_name&quot;,
                                               &quot;visibility&quot;,
                                             ])
        output_name =
            rebase_path(&quot;$gen_path/$app_name&quot;, root_build_dir)
      }

      code_signing =
          defined(invoker.code_signing) &amp;&amp; invoker.code_signing

      if (is_ios &amp;&amp; !code_signing) {
        bundle_data(&quot;${app_name}_bundle_executable&quot;) {
          deps = [ &quot;:${app_name}_generate_executable&quot; ]
          sources = [ &quot;$gen_path/$app_name&quot; ]
          outputs = [ &quot;{{bundle_executable_dir}}/$app_name&quot; ]
        }
      }

      create_bundle(&quot;${app_name}.app&quot;) {
        product_type = &quot;com.apple.product-type.application&quot;

        if (is_ios) {
          bundle_root_dir = &quot;${root_build_dir}/$target_name&quot;
          bundle_contents_dir = bundle_root_dir
          bundle_resources_dir = bundle_contents_dir
          bundle_executable_dir = bundle_contents_dir
          bundle_plugins_dir = &quot;${bundle_contents_dir}/Plugins&quot;

          extra_attributes = {
            ONLY_ACTIVE_ARCH = &quot;YES&quot;
            DEBUG_INFORMATION_FORMAT = &quot;dwarf&quot;
          }
        } else {
          bundle_root_dir = &quot;${root_build_dir}/target_name&quot;
          bundle_contents_dir  = &quot;${bundle_root_dir}/Contents&quot;
          bundle_resources_dir = &quot;${bundle_contents_dir}/Resources&quot;
          bundle_executable_dir = &quot;${bundle_contents_dir}/MacOS&quot;
          bundle_plugins_dir = &quot;${bundle_contents_dir}/Plugins&quot;
        }
        deps = [ &quot;:${app_name}_bundle_info_plist&quot; ]
        if (is_ios &amp;&amp; code_signing) {
          deps += [ &quot;:${app_name}_generate_executable&quot; ]
          code_signing_script = &quot;//build/config/ios/codesign.py&quot;
          code_signing_sources = [
            invoker.entitlements_path,
            &quot;$target_gen_dir/$app_name&quot;,
          ]
          code_signing_outputs = [
            &quot;$bundle_root_dir/$app_name&quot;,
            &quot;$bundle_root_dir/_CodeSignature/CodeResources&quot;,
            &quot;$bundle_root_dir/embedded.mobileprovision&quot;,
            &quot;$target_gen_dir/$app_name.xcent&quot;,
          ]
          code_signing_args = [
            &quot;-i=&quot; + ios_code_signing_identity,
            &quot;-b=&quot; + rebase_path(
                &quot;$target_gen_dir/$app_name&quot;, root_build_dir),
            &quot;-e=&quot; + rebase_path(
                invoker.entitlements_path, root_build_dir),
            &quot;-e=&quot; + rebase_path(
                &quot;$target_gen_dir/$app_name.xcent&quot;, root_build_dir),
            rebase_path(bundle_root_dir, root_build_dir),
          ]
        } else {
          deps += [ &quot;:${app_name}_bundle_executable&quot; ]
        }
      }
    }
  }
</pre><h3><a class="h" name="executable" href="#executable"><span></span></a><strong>executable</strong>: Declare an executable target.</h3><h4><a class="h" name="Target-declarations-executable_Declare-an-executable-target-Variables" href="#Target-declarations-executable_Declare-an-executable-target-Variables"><span></span></a><a class="h" name="target-declarations-executable_declare-an-executable-target-variables" href="#target-declarations-executable_declare-an-executable-target-variables"><span></span></a><strong>Variables</strong></h4><pre class="code">  Flags: cflags, cflags_c, cflags_cc, cflags_objc, cflags_objcc,
         asmflags, defines, include_dirs, ldflags, lib_dirs, libs,
         precompiled_header, precompiled_source
  Deps: data_deps, deps, public_deps
  Dependent configs: all_dependent_configs, public_configs
  General: check_includes, configs, data, inputs, output_name,
           output_extension, public, sources, testonly, visibility
</pre><h3><a class="h" name="group" href="#group"><span></span></a><strong>group</strong>: Declare a named group of targets.</h3><pre class="code">  This target type allows you to create meta-targets that just collect a set of
  dependencies into one named target. Groups can additionally specify configs
  that apply to their dependents.
</pre><h4><a class="h" name="Target-declarations-group_Declare-a-named-group-of-targets-Variables" href="#Target-declarations-group_Declare-a-named-group-of-targets-Variables"><span></span></a><a class="h" name="target-declarations-group_declare-a-named-group-of-targets-variables" href="#target-declarations-group_declare-a-named-group-of-targets-variables"><span></span></a><strong>Variables</strong></h4><pre class="code">  Deps: data_deps, deps, public_deps
  Dependent configs: all_dependent_configs, public_configs
</pre><h4><a class="h" name="Target-declarations-group_Declare-a-named-group-of-targets-Example" href="#Target-declarations-group_Declare-a-named-group-of-targets-Example"><span></span></a><a class="h" name="target-declarations-group_declare-a-named-group-of-targets-example" href="#target-declarations-group_declare-a-named-group-of-targets-example"><span></span></a><strong>Example</strong></h4><pre class="code">  group(&quot;all&quot;) {
    deps = [
      &quot;//project:runner&quot;,
      &quot;//project:unit_tests&quot;,
    ]
  }
</pre><h3><a class="h" name="loadable_module" href="#loadable_module"><span></span></a><strong>loadable_module</strong>: Declare a loadable module target.</h3><pre class="code">  This target type allows you to create an object file that is (and can only
  be) loaded and unloaded at runtime.

  A loadable module will be specified on the linker line for targets listing
  the loadable module in its &quot;deps&quot;. If you don&#39;t want this (if you don&#39;t need
  to dynamically load the library at runtime), then you should use a
  &quot;shared_library&quot; target type instead.
</pre><h4><a class="h" name="Target-declarations-loadable_module_Declare-a-loadable-module-target-Variables" href="#Target-declarations-loadable_module_Declare-a-loadable-module-target-Variables"><span></span></a><a class="h" name="target-declarations-loadable_module_declare-a-loadable-module-target-variables" href="#target-declarations-loadable_module_declare-a-loadable-module-target-variables"><span></span></a><strong>Variables</strong></h4><pre class="code">  Flags: cflags, cflags_c, cflags_cc, cflags_objc, cflags_objcc,
         asmflags, defines, include_dirs, ldflags, lib_dirs, libs,
         precompiled_header, precompiled_source
  Deps: data_deps, deps, public_deps
  Dependent configs: all_dependent_configs, public_configs
  General: check_includes, configs, data, inputs, output_name,
           output_extension, public, sources, testonly, visibility
</pre><h3><a class="h" name="shared_library" href="#shared_library"><span></span></a><strong>shared_library</strong>: Declare a shared library target.</h3><pre class="code">  A shared library will be specified on the linker line for targets listing the
  shared library in its &quot;deps&quot;. If you don&#39;t want this (say you dynamically
  load the library at runtime), then you should depend on the shared library
  via &quot;data_deps&quot; or, on Darwin platforms, use a &quot;loadable_module&quot; target type
  instead.
</pre><h4><a class="h" name="Target-declarations-shared_library_Declare-a-shared-library-target-Variables" href="#Target-declarations-shared_library_Declare-a-shared-library-target-Variables"><span></span></a><a class="h" name="target-declarations-shared_library_declare-a-shared-library-target-variables" href="#target-declarations-shared_library_declare-a-shared-library-target-variables"><span></span></a><strong>Variables</strong></h4><pre class="code">  Flags: cflags, cflags_c, cflags_cc, cflags_objc, cflags_objcc,
         asmflags, defines, include_dirs, ldflags, lib_dirs, libs,
         precompiled_header, precompiled_source
  Deps: data_deps, deps, public_deps
  Dependent configs: all_dependent_configs, public_configs
  General: check_includes, configs, data, inputs, output_name,
           output_extension, public, sources, testonly, visibility
</pre><h3><a class="h" name="source_set" href="#source_set"><span></span></a><strong>source_set</strong>: Declare a source set target.</h3><pre class="code">  A source set is a collection of sources that get compiled, but are not linked
  to produce any kind of library. Instead, the resulting object files are
  implicitly added to the linker line of all targets that depend on the source
  set.

  In most cases, a source set will behave like a static library, except no
  actual library file will be produced. This will make the build go a little
  faster by skipping creation of a large static library, while maintaining the
  organizational benefits of focused build targets.

  The main difference between a source set and a static library is around
  handling of exported symbols. Most linkers assume declaring a function
  exported means exported from the static library. The linker can then do dead
  code elimination to delete code not reachable from exported functions.

  A source set will not do this code elimination since there is no link step.
  This allows you to link many sources sets into a shared library and have the
  &quot;exported symbol&quot; notation indicate &quot;export from the final shared library and
  not from the intermediate targets.&quot; There is no way to express this concept
  when linking multiple static libraries into a shared library.
</pre><h4><a class="h" name="Target-declarations-source_set_Declare-a-source-set-target-Variables" href="#Target-declarations-source_set_Declare-a-source-set-target-Variables"><span></span></a><a class="h" name="target-declarations-source_set_declare-a-source-set-target-variables" href="#target-declarations-source_set_declare-a-source-set-target-variables"><span></span></a><strong>Variables</strong></h4><pre class="code">  Flags: cflags, cflags_c, cflags_cc, cflags_objc, cflags_objcc,
         asmflags, defines, include_dirs, ldflags, lib_dirs, libs,
         precompiled_header, precompiled_source
  Deps: data_deps, deps, public_deps
  Dependent configs: all_dependent_configs, public_configs
  General: check_includes, configs, data, inputs, output_name,
           output_extension, public, sources, testonly, visibility
</pre><h3><a class="h" name="static_library" href="#static_library"><span></span></a><strong>static_library</strong>: Declare a static library target.</h3><pre class="code">  Make a &quot;.a&quot; / &quot;.lib&quot; file.

  If you only need the static library for intermediate results in the build,
  you should consider a source_set instead since it will skip the (potentially
  slow) step of creating the intermediate library file.
</pre><h4><a class="h" name="Target-declarations-static_library_Declare-a-static-library-target-Variables" href="#Target-declarations-static_library_Declare-a-static-library-target-Variables"><span></span></a><a class="h" name="target-declarations-static_library_declare-a-static-library-target-variables" href="#target-declarations-static_library_declare-a-static-library-target-variables"><span></span></a><strong>Variables</strong></h4><pre class="code">  complete_static_lib
  Flags: cflags, cflags_c, cflags_cc, cflags_objc, cflags_objcc,
         asmflags, defines, include_dirs, ldflags, lib_dirs, libs,
         precompiled_header, precompiled_source
  Deps: data_deps, deps, public_deps
  Dependent configs: all_dependent_configs, public_configs
  General: check_includes, configs, data, inputs, output_name,
           output_extension, public, sources, testonly, visibility
</pre><h3><a class="h" name="target" href="#target"><span></span></a><strong>target</strong>: Declare an target with the given programmatic type.</h3><pre class="code">  target(target_type_string, target_name_string) { ... }

  The target() function is a way to invoke a built-in target or template with a
  type determined at runtime. This is useful for cases where the type of a
  target might not be known statically.

  Only templates and built-in target functions are supported for the
  target_type_string parameter. Arbitrary functions, configs, and toolchains
  are not supported.

  The call:
    target(&quot;source_set&quot;, &quot;doom_melon&quot;) {
  Is equivalent to:
    source_set(&quot;doom_melon&quot;) {
</pre><h4><a class="h" name="Target-declarations-target_Declare-an-target-with-the-given-programmatic-type-Example" href="#Target-declarations-target_Declare-an-target-with-the-given-programmatic-type-Example"><span></span></a><a class="h" name="target-declarations-target_declare-an-target-with-the-given-programmatic-type-example" href="#target-declarations-target_declare-an-target-with-the-given-programmatic-type-example"><span></span></a><strong>Example</strong></h4><pre class="code">  if (foo_build_as_shared) {
    my_type = &quot;shared_library&quot;
  } else {
    my_type = &quot;source_set&quot;
  }

  target(my_type, &quot;foo&quot;) {
    ...
  }
</pre><h2><a class="h" name="functions" href="#functions"><span></span></a>Buildfile functions</h2><h3><a class="h" name="assert" href="#assert"><span></span></a><strong>assert</strong>: Assert an expression is true at generation time.</h3><pre class="code">  assert(&lt;condition&gt; [, &lt;error string&gt;])

  If the condition is false, the build will fail with an error. If the
  optional second argument is provided, that string will be printed
  with the error message.
</pre><h4><a class="h" name="Buildfile-functions-assert_Assert-an-expression-is-true-at-generation-time-Examples" href="#Buildfile-functions-assert_Assert-an-expression-is-true-at-generation-time-Examples"><span></span></a><a class="h" name="buildfile-functions-assert_assert-an-expression-is-true-at-generation-time-examples" href="#buildfile-functions-assert_assert-an-expression-is-true-at-generation-time-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  assert(is_win)
  assert(defined(sources), &quot;Sources must be defined&quot;);
</pre><h3><a class="h" name="config" href="#config"><span></span></a><strong>config</strong>: Defines a configuration object.</h3><pre class="code">  Configuration objects can be applied to targets and specify sets of compiler
  flags, includes, defines, etc. They provide a way to conveniently group sets
  of this configuration information.

  A config is referenced by its label just like a target.

  The values in a config are additive only. If you want to remove a flag you
  need to remove the corresponding config that sets it. The final set of flags,
  defines, etc. for a target is generated in this order:

   1. The values specified directly on the target (rather than using a config.
   2. The configs specified in the target&#39;s &quot;configs&quot; list, in order.
   3. Public_configs from a breadth-first traversal of the dependency tree in
      the order that the targets appear in &quot;deps&quot;.
   4. All dependent configs from a breadth-first traversal of the dependency
      tree in the order that the targets appear in &quot;deps&quot;.
</pre><h4><a class="h" name="Variables-valid-in-a-config-definition" href="#Variables-valid-in-a-config-definition"><span></span></a><a class="h" name="variables-valid-in-a-config-definition" href="#variables-valid-in-a-config-definition"><span></span></a><strong>Variables valid in a config definition</strong></h4><pre class="code">  Flags: cflags, cflags_c, cflags_cc, cflags_objc, cflags_objcc,
         asmflags, defines, include_dirs, ldflags, lib_dirs, libs,
         precompiled_header, precompiled_source
  Nested configs: configs
</pre><h4><a class="h" name="Variables-on-a-target-used-to-apply-configs" href="#Variables-on-a-target-used-to-apply-configs"><span></span></a><a class="h" name="variables-on-a-target-used-to-apply-configs" href="#variables-on-a-target-used-to-apply-configs"><span></span></a><strong>Variables on a target used to apply configs</strong></h4><pre class="code">  all_dependent_configs, configs, public_configs
</pre><h4><a class="h" name="Buildfile-functions-config_Defines-a-configuration-object-Example" href="#Buildfile-functions-config_Defines-a-configuration-object-Example"><span></span></a><a class="h" name="buildfile-functions-config_defines-a-configuration-object-example" href="#buildfile-functions-config_defines-a-configuration-object-example"><span></span></a><strong>Example</strong></h4><pre class="code">  config(&quot;myconfig&quot;) {
    includes = [ &quot;include/common&quot; ]
    defines = [ &quot;ENABLE_DOOM_MELON&quot; ]
  }

  executable(&quot;mything&quot;) {
    configs = [ &quot;:myconfig&quot; ]
  }
</pre><h3><a class="h" name="declare_args" href="#declare_args"><span></span></a><strong>declare_args</strong>: Declare build arguments.</h3><pre class="code">  Introduces the given arguments into the current scope. If they are not
  specified on the command line or in a toolchain&#39;s arguments, the default
  values given in the declare_args block will be used. However, these defaults
  will not override command-line values.

  See also &quot;gn help buildargs&quot; for an overview.

  The precise behavior of declare args is:

   1. The declare_args() block executes. Any variable defined in the enclosing
      scope is available for reading, but any variable defined earlier in
      the current scope is not (since the overrides haven&#39;t been applied yet).

   2. At the end of executing the block, any variables set within that scope
      are saved globally as build arguments, with their current values being
      saved as the &quot;default value&quot; for that argument.

   3. User-defined overrides are applied. Anything set in &quot;gn args&quot; now
      overrides any default values. The resulting set of variables is promoted
      to be readable from the following code in the file.

  This has some ramifications that may not be obvious:

    - You should not perform difficult work inside a declare_args block since
      this only sets a default value that may be discarded. In particular,
      don&#39;t use the result of exec_script() to set the default value. If you
      want to have a script-defined default, set some default &quot;undefined&quot; value
      like [], &quot;&quot;, or -1, and after the declare_args block, call exec_script if
      the value is unset by the user.

    - Because you cannot read the value of a variable defined in the same
      block, if you need to make the default value of one arg depend
      on the possibly-overridden value of another, write two separate
      declare_args() blocks:

        declare_args() {
          enable_foo = true
        }
        declare_args() {
          # Bar defaults to same user-overridden state as foo.
          enable_bar = enable_foo
        }
</pre><h4><a class="h" name="Buildfile-functions-declare_args_Declare-build-arguments-Example" href="#Buildfile-functions-declare_args_Declare-build-arguments-Example"><span></span></a><a class="h" name="buildfile-functions-declare_args_declare-build-arguments-example" href="#buildfile-functions-declare_args_declare-build-arguments-example"><span></span></a><strong>Example</strong></h4><pre class="code">  declare_args() {
    enable_teleporter = true
    enable_doom_melon = false
  }

  If you want to override the (default disabled) Doom Melon:
    gn --args=&quot;enable_doom_melon=true enable_teleporter=true&quot;
  This also sets the teleporter, but it&#39;s already defaulted to on so it will
  have no effect.
</pre><h3><a class="h" name="defined" href="#defined"><span></span></a><strong>defined</strong>: Returns whether an identifier is defined.</h3><pre class="code">  Returns true if the given argument is defined. This is most useful in
  templates to assert that the caller set things up properly.

  You can pass an identifier:
    defined(foo)
  which will return true or false depending on whether foo is defined in the
  current scope.

  You can also check a named scope:
    defined(foo.bar)
  which will return true or false depending on whether bar is defined in the
  named scope foo. It will throw an error if foo is not defined or is not a
  scope.
</pre><h4><a class="h" name="Buildfile-functions-defined_Returns-whether-an-identifier-is-defined-Example" href="#Buildfile-functions-defined_Returns-whether-an-identifier-is-defined-Example"><span></span></a><a class="h" name="buildfile-functions-defined_returns-whether-an-identifier-is-defined-example" href="#buildfile-functions-defined_returns-whether-an-identifier-is-defined-example"><span></span></a><strong>Example</strong></h4><pre class="code">  template(&quot;mytemplate&quot;) {
    # To help users call this template properly...
    assert(defined(invoker.sources), &quot;Sources must be defined&quot;)

    # If we want to accept an optional &quot;values&quot; argument, we don&#39;t
    # want to dereference something that may not be defined.
    if (defined(invoker.values)) {
      values = invoker.values
    } else {
      values = &quot;some default value&quot;
    }
  }
</pre><h3><a class="h" name="exec_script" href="#exec_script"><span></span></a><strong>exec_script</strong>: Synchronously run a script and return the output.</h3><pre class="code">  exec_script(filename,
              arguments = [],
              input_conversion = &quot;&quot;,
              file_dependencies = [])

  Runs the given script, returning the stdout of the script. The build
  generation will fail if the script does not exist or returns a nonzero exit
  code.

  The current directory when executing the script will be the root build
  directory. If you are passing file names, you will want to use the
  rebase_path() function to make file names relative to this path (see &quot;gn help
  rebase_path&quot;).
</pre><h4><a class="h" name="Buildfile-functions-exec_script_Synchronously-run-a-script-and-return-the-output-Arguments" href="#Buildfile-functions-exec_script_Synchronously-run-a-script-and-return-the-output-Arguments"><span></span></a><a class="h" name="buildfile-functions-exec_script_synchronously-run-a-script-and-return-the-output-arguments" href="#buildfile-functions-exec_script_synchronously-run-a-script-and-return-the-output-arguments"><span></span></a><strong>Arguments</strong>:</h4><pre class="code">  filename:
      File name of python script to execute. Non-absolute names will be treated
      as relative to the current build file.

  arguments:
      A list of strings to be passed to the script as arguments. May be
      unspecified or the empty list which means no arguments.

  input_conversion:
      Controls how the file is read and parsed. See &quot;gn help input_conversion&quot;.

      If unspecified, defaults to the empty string which causes the script
      result to be discarded. exec script will return None.

  dependencies:
      (Optional) A list of files that this script reads or otherwise depends
      on. These dependencies will be added to the build result such that if any
      of them change, the build will be regenerated and the script will be
      re-run.

      The script itself will be an implicit dependency so you do not need to
      list it.
</pre><h4><a class="h" name="Buildfile-functions-exec_script_Synchronously-run-a-script-and-return-the-output-Example" href="#Buildfile-functions-exec_script_Synchronously-run-a-script-and-return-the-output-Example"><span></span></a><a class="h" name="buildfile-functions-exec_script_synchronously-run-a-script-and-return-the-output-example" href="#buildfile-functions-exec_script_synchronously-run-a-script-and-return-the-output-example"><span></span></a><strong>Example</strong></h4><pre class="code">  all_lines = exec_script(
      &quot;myscript.py&quot;, [some_input], &quot;list lines&quot;,
      [ rebase_path(&quot;data_file.txt&quot;, root_build_dir) ])

  # This example just calls the script with no arguments and discards the
  # result.
  exec_script(&quot;//foo/bar/myscript.py&quot;)
</pre><h3><a class="h" name="foreach" href="#foreach"><span></span></a><strong>foreach</strong>: Iterate over a list.</h3><pre class="code">    foreach(&lt;loop_var&gt;, &lt;list&gt;) {
      &lt;loop contents&gt;
    }

  Executes the loop contents block over each item in the list, assigning the
  loop_var to each item in sequence. The loop_var will be a copy so assigning
  to it will not mutate the list.

  The block does not introduce a new scope, so that variable assignments inside
  the loop will be visible once the loop terminates.

  The loop variable will temporarily shadow any existing variables with the
  same name for the duration of the loop. After the loop terminates the loop
  variable will no longer be in scope, and the previous value (if any) will be
  restored.
</pre><h4><a class="h" name="Buildfile-functions-foreach_Iterate-over-a-list-Example" href="#Buildfile-functions-foreach_Iterate-over-a-list-Example"><span></span></a><a class="h" name="buildfile-functions-foreach_iterate-over-a-list-example" href="#buildfile-functions-foreach_iterate-over-a-list-example"><span></span></a><strong>Example</strong></h4><pre class="code">  mylist = [ &quot;a&quot;, &quot;b&quot;, &quot;c&quot; ]
  foreach(i, mylist) {
    print(i)
  }

  Prints:
  a
  b
  c
</pre><h3><a class="h" name="forward_variables_from" href="#forward_variables_from"><span></span></a><strong>forward_variables_from</strong>: Copies variables from a different scope.</h3><pre class="code">  forward_variables_from(from_scope, variable_list_or_star,
                         variable_to_not_forward_list = [])

  Copies the given variables from the given scope to the local scope if they
  exist. This is normally used in the context of templates to use the values of
  variables defined in the template invocation to a template-defined target.

  The variables in the given variable_list will be copied if they exist in the
  given scope or any enclosing scope. If they do not exist, nothing will happen
  and they be left undefined in the current scope.

  As a special case, if the variable_list is a string with the value of &quot;*&quot;,
  all variables from the given scope will be copied. &quot;*&quot; only copies variables
  set directly on the from_scope, not enclosing ones. Otherwise it would
  duplicate all global variables.

  When an explicit list of variables is supplied, if the variable exists in the
  current (destination) scope already, an error will be thrown. If &quot;*&quot; is
  specified, variables in the current scope will be clobbered (the latter is
  important because most targets have an implicit configs list, which means it
  wouldn&#39;t work at all if it didn&#39;t clobber).

  The sources assignment filter (see &quot;gn help &quot;
     &quot;set_sources_assignment_filter&quot;)
  is never applied by this function. It&#39;s assumed than any desired filtering
  was already done when sources was set on the from_scope.

  If variables_to_not_forward_list is non-empty, then it must contains a list
  of variable names that will not be forwarded. This is mostly useful when
  variable_list_or_star has a value of &quot;*&quot;.
</pre><h4><a class="h" name="Buildfile-functions-forward_variables_from_Copies-variables-from-a-different-scope-Examples" href="#Buildfile-functions-forward_variables_from_Copies-variables-from-a-different-scope-Examples"><span></span></a><a class="h" name="buildfile-functions-forward_variables_from_copies-variables-from-a-different-scope-examples" href="#buildfile-functions-forward_variables_from_copies-variables-from-a-different-scope-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  # This is a common action template. It would invoke a script with some given
  # parameters, and wants to use the various types of deps and the visibility
  # from the invoker if it&#39;s defined. It also injects an additional dependency
  # to all targets.
  template(&quot;my_test&quot;) {
    action(target_name) {
      forward_variables_from(invoker, [ &quot;data_deps&quot;, &quot;deps&quot;,
                                        &quot;public_deps&quot;, &quot;visibility&quot; &quot;
                                                                    &quot;])
      # Add our test code to the dependencies.
      # &quot;deps&quot; may or may not be defined at this point.
      if (defined(deps)) {
        deps += [ &quot;//tools/doom_melon&quot; ]
      } else {
        deps = [ &quot;//tools/doom_melon&quot; ]
      }
    }
  }

  # This is a template around either a target whose type depends on a global
  # variable. It forwards all values from the invoker.
  template(&quot;my_wrapper&quot;) {
    target(my_wrapper_target_type, target_name) {
      forward_variables_from(invoker, &quot;*&quot;)
    }
  }

  # A template that wraps another. It adds behavior based on one
  # variable, and forwards all others to the nested target.
  template(&quot;my_ios_test_app&quot;) {
    ios_test_app(target_name) {
      forward_variables_from(invoker, &quot;*&quot;, [&quot;test_bundle_name&quot;])
      if (!defined(extra_substitutions)) {
        extra_substitutions = []
      }
      extra_substitutions += [ &quot;BUNDLE_ID_TEST_NAME=$test_bundle_name&quot; ]
    }
  }
</pre><h3><a class="h" name="get_label_info" href="#get_label_info"><span></span></a><strong>get_label_info</strong>: Get an attribute from a target&#39;s label.</h3><pre class="code">  get_label_info(target_label, what)

  Given the label of a target, returns some attribute of that target. The
  target need not have been previously defined in the same file, since none of
  the attributes depend on the actual target definition, only the label itself.

  See also &quot;gn help get_target_outputs&quot;.
</pre><h4><a class="h" name="Buildfile-functions-get_label_info_Get-an-attribute-from-a-target_s-label-Possible-values-for-the-what-parameter" href="#Buildfile-functions-get_label_info_Get-an-attribute-from-a-target_s-label-Possible-values-for-the-what-parameter"><span></span></a><a class="h" name="buildfile-functions-get_label_info_get-an-attribute-from-a-target_s-label-possible-values-for-the-what-parameter" href="#buildfile-functions-get_label_info_get-an-attribute-from-a-target_s-label-possible-values-for-the-what-parameter"><span></span></a><strong>Possible values for the &ldquo;what&rdquo; parameter</strong></h4><pre class="code">  &quot;name&quot;
      The short name of the target. This will match the value of the
      &quot;target_name&quot; variable inside that target&#39;s declaration. For the label
      &quot;//foo/bar:baz&quot; this will return &quot;baz&quot;.

  &quot;dir&quot;
      The directory containing the target&#39;s definition, with no slash at the
      end. For the label &quot;//foo/bar:baz&quot; this will return &quot;//foo/bar&quot;.

  &quot;target_gen_dir&quot;
      The generated file directory for the target. This will match the value of
      the &quot;target_gen_dir&quot; variable when inside that target&#39;s declaration.

  &quot;root_gen_dir&quot;
      The root of the generated file tree for the target. This will match the
      value of the &quot;root_gen_dir&quot; variable when inside that target&#39;s
      declaration.

  &quot;target_out_dir
      The output directory for the target. This will match the value of the
      &quot;target_out_dir&quot; variable when inside that target&#39;s declaration.

  &quot;root_out_dir&quot;
      The root of the output file tree for the target. This will match the
      value of the &quot;root_out_dir&quot; variable when inside that target&#39;s
      declaration.

  &quot;label_no_toolchain&quot;
      The fully qualified version of this label, not including the toolchain.
      For the input &quot;:bar&quot; it might return &quot;//foo:bar&quot;.

  &quot;label_with_toolchain&quot;
      The fully qualified version of this label, including the toolchain. For
      the input &quot;:bar&quot; it might return &quot;//foo:bar(//toolchain:x64)&quot;.

  &quot;toolchain&quot;
      The label of the toolchain. This will match the value of the
      &quot;current_toolchain&quot; variable when inside that target&#39;s declaration.
</pre><h4><a class="h" name="Buildfile-functions-get_label_info_Get-an-attribute-from-a-target_s-label-Examples" href="#Buildfile-functions-get_label_info_Get-an-attribute-from-a-target_s-label-Examples"><span></span></a><a class="h" name="buildfile-functions-get_label_info_get-an-attribute-from-a-target_s-label-examples" href="#buildfile-functions-get_label_info_get-an-attribute-from-a-target_s-label-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  get_label_info(&quot;:foo&quot;, &quot;name&quot;)
  # Returns string &quot;foo&quot;.

  get_label_info(&quot;//foo/bar:baz&quot;, &quot;target_gen_dir&quot;)
  # Returns string &quot;//out/Debug/gen/foo/bar&quot;.
</pre><h3><a class="h" name="get_path_info" href="#get_path_info"><span></span></a><strong>get_path_info</strong>: Extract parts of a file or directory name.</h3><pre class="code">  get_path_info(input, what)

  The first argument is either a string representing a file or directory name,
  or a list of such strings. If the input is a list the return value will be a
  list containing the result of applying the rule to each item in the input.
</pre><h4><a class="h" name="Buildfile-functions-get_path_info_Extract-parts-of-a-file-or-directory-name-Possible-values-for-the-what-parameter" href="#Buildfile-functions-get_path_info_Extract-parts-of-a-file-or-directory-name-Possible-values-for-the-what-parameter"><span></span></a><a class="h" name="buildfile-functions-get_path_info_extract-parts-of-a-file-or-directory-name-possible-values-for-the-what-parameter" href="#buildfile-functions-get_path_info_extract-parts-of-a-file-or-directory-name-possible-values-for-the-what-parameter"><span></span></a><strong>Possible values for the &ldquo;what&rdquo; parameter</strong></h4><pre class="code">  &quot;file&quot;
      The substring after the last slash in the path, including the name and
      extension. If the input ends in a slash, the empty string will be
      returned.
        &quot;foo/bar.txt&quot; =&gt; &quot;bar.txt&quot;
        &quot;bar.txt&quot; =&gt; &quot;bar.txt&quot;
        &quot;foo/&quot; =&gt; &quot;&quot;
        &quot;&quot; =&gt; &quot;&quot;

  &quot;name&quot;
     The substring of the file name not including the extension.
        &quot;foo/bar.txt&quot; =&gt; &quot;bar&quot;
        &quot;foo/bar&quot; =&gt; &quot;bar&quot;
        &quot;foo/&quot; =&gt; &quot;&quot;

  &quot;extension&quot;
      The substring following the last period following the last slash, or the
      empty string if not found. The period is not included.
        &quot;foo/bar.txt&quot; =&gt; &quot;txt&quot;
        &quot;foo/bar&quot; =&gt; &quot;&quot;

  &quot;dir&quot;
      The directory portion of the name, not including the slash.
        &quot;foo/bar.txt&quot; =&gt; &quot;foo&quot;
        &quot;//foo/bar&quot; =&gt; &quot;//foo&quot;
        &quot;foo&quot; =&gt; &quot;.&quot;

      The result will never end in a slash, so if the resulting is empty, the
      system (&quot;/&quot;) or source (&quot;//&quot;) roots, a &quot;.&quot; will be appended such that it
      is always legal to append a slash and a filename and get a valid path.

  &quot;out_dir&quot;
      The output file directory corresponding to the path of the given file,
      not including a trailing slash.
        &quot;//foo/bar/baz.txt&quot; =&gt; &quot;//out/Default/obj/foo/bar&quot;

  &quot;gen_dir&quot;
      The generated file directory corresponding to the path of the given file,
      not including a trailing slash.
        &quot;//foo/bar/baz.txt&quot; =&gt; &quot;//out/Default/gen/foo/bar&quot;

  &quot;abspath&quot;
      The full absolute path name to the file or directory. It will be resolved
      relative to the current directory, and then the source- absolute version
      will be returned. If the input is system- absolute, the same input will
      be returned.
        &quot;foo/bar.txt&quot; =&gt; &quot;//mydir/foo/bar.txt&quot;
        &quot;foo/&quot; =&gt; &quot;//mydir/foo/&quot;
        &quot;//foo/bar&quot; =&gt; &quot;//foo/bar&quot;  (already absolute)
        &quot;/usr/include&quot; =&gt; &quot;/usr/include&quot;  (already absolute)

      If you want to make the path relative to another directory, or to be
      system-absolute, see rebase_path().
</pre><h4><a class="h" name="Buildfile-functions-get_path_info_Extract-parts-of-a-file-or-directory-name-Examples" href="#Buildfile-functions-get_path_info_Extract-parts-of-a-file-or-directory-name-Examples"><span></span></a><a class="h" name="buildfile-functions-get_path_info_extract-parts-of-a-file-or-directory-name-examples" href="#buildfile-functions-get_path_info_extract-parts-of-a-file-or-directory-name-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  sources = [ &quot;foo.cc&quot;, &quot;foo.h&quot; ]
  result = get_path_info(source, &quot;abspath&quot;)
  # result will be [ &quot;//mydir/foo.cc&quot;, &quot;//mydir/foo.h&quot; ]

  result = get_path_info(&quot;//foo/bar/baz.cc&quot;, &quot;dir&quot;)
  # result will be &quot;//foo/bar&quot;

  # Extract the source-absolute directory name,
  result = get_path_info(get_path_info(path, &quot;dir&quot;), &quot;abspath&quot;
</pre><h3><a class="h" name="get_target_outputs" href="#get_target_outputs"><span></span></a><strong>get_target_outputs</strong>: [file list] Get the list of outputs from a target.</h3><pre class="code">  get_target_outputs(target_label)

  Returns a list of output files for the named target. The named target must
  have been previously defined in the current file before this function is
  called (it can&#39;t reference targets in other files because there isn&#39;t a
  defined execution order, and it obviously can&#39;t reference targets that are
  defined after the function call).

  Only copy and action targets are supported. The outputs from binary targets
  will depend on the toolchain definition which won&#39;t necessarily have been
  loaded by the time a given line of code has run, and source sets and groups
  have no useful output file.
</pre><h4><a class="h" name="Buildfile-functions-get_target_outputs_file-list_Get-the-list-of-outputs-from-a-target-Return-value" href="#Buildfile-functions-get_target_outputs_file-list_Get-the-list-of-outputs-from-a-target-Return-value"><span></span></a><a class="h" name="buildfile-functions-get_target_outputs_file-list_get-the-list-of-outputs-from-a-target-return-value" href="#buildfile-functions-get_target_outputs_file-list_get-the-list-of-outputs-from-a-target-return-value"><span></span></a><strong>Return value</strong></h4><pre class="code">  The names in the resulting list will be absolute file paths (normally like
  &quot;//out/Debug/bar.exe&quot;, depending on the build directory).

  action targets: this will just return the files specified in the &quot;outputs&quot;
  variable of the target.

  action_foreach targets: this will return the result of applying the output
  template to the sources (see &quot;gn help source_expansion&quot;). This will be the
  same result (though with guaranteed absolute file paths), as
  process_file_template will return for those inputs (see &quot;gn help
  process_file_template&quot;).

  binary targets (executables, libraries): this will return a list of the
  resulting binary file(s). The &quot;main output&quot; (the actual binary or library)
  will always be the 0th element in the result. Depending on the platform and
  output type, there may be other output files as well (like import libraries)
  which will follow.

  source sets and groups: this will return a list containing the path of the
  &quot;stamp&quot; file that Ninja will produce once all outputs are generated. This
  probably isn&#39;t very useful.
</pre><h4><a class="h" name="Buildfile-functions-get_target_outputs_file-list_Get-the-list-of-outputs-from-a-target-Example" href="#Buildfile-functions-get_target_outputs_file-list_Get-the-list-of-outputs-from-a-target-Example"><span></span></a><a class="h" name="buildfile-functions-get_target_outputs_file-list_get-the-list-of-outputs-from-a-target-example" href="#buildfile-functions-get_target_outputs_file-list_get-the-list-of-outputs-from-a-target-example"><span></span></a><strong>Example</strong></h4><pre class="code">  # Say this action generates a bunch of C source files.
  action_foreach(&quot;my_action&quot;) {
    sources = [ ... ]
    outputs = [ ... ]
  }

  # Compile the resulting source files into a source set.
  source_set(&quot;my_lib&quot;) {
    sources = get_target_outputs(&quot;:my_action&quot;)
  }
</pre><h3><a class="h" name="getenv" href="#getenv"><span></span></a><strong>getenv</strong>: Get an environment variable.</h3><pre class="code">  value = getenv(env_var_name)

  Returns the value of the given enironment variable. If the value is not
  found, it will try to look up the variable with the &quot;opposite&quot; case (based on
  the case of the first letter of the variable), but is otherwise
  case-sensitive.

  If the environment variable is not found, the empty string will be returned.
  Note: it might be nice to extend this if we had the concept of &quot;none&quot; in the
  language to indicate lookup failure.
</pre><h4><a class="h" name="Buildfile-functions-getenv_Get-an-environment-variable-Example" href="#Buildfile-functions-getenv_Get-an-environment-variable-Example"><span></span></a><a class="h" name="buildfile-functions-getenv_get-an-environment-variable-example" href="#buildfile-functions-getenv_get-an-environment-variable-example"><span></span></a><strong>Example</strong></h4><pre class="code">  home_dir = getenv(&quot;HOME&quot;)
</pre><h3><a class="h" name="import" href="#import"><span></span></a><strong>import</strong>: Import a file into the current scope.</h3><pre class="code">  The import command loads the rules and variables resulting from executing the
  given file into the current scope.

  By convention, imported files are named with a .gni extension.

  An import is different than a C++ &quot;include&quot;. The imported file is executed in
  a standalone environment from the caller of the import command. The results
  of this execution are cached for other files that import the same .gni file.

  Note that you can not import a BUILD.gn file that&#39;s otherwise used in the
  build. Files must either be imported or implicitly loaded as a result of deps
  rules, but not both.

  The imported file&#39;s scope will be merged with the scope at the point import
  was called. If there is a conflict (both the current scope and the imported
  file define some variable or rule with the same name but different value), a
  runtime error will be thrown. Therefore, it&#39;s good practice to minimize the
  stuff that an imported file defines.

  Variables and templates beginning with an underscore &#39;_&#39; are considered
  private and will not be imported. Imported files can use such variables for
  internal computation without affecting other files.
</pre><h4><a class="h" name="Buildfile-functions-import_Import-a-file-into-the-current-scope-Examples" href="#Buildfile-functions-import_Import-a-file-into-the-current-scope-Examples"><span></span></a><a class="h" name="buildfile-functions-import_import-a-file-into-the-current-scope-examples" href="#buildfile-functions-import_import-a-file-into-the-current-scope-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  import(&quot;//build/rules/idl_compilation_rule.gni&quot;)

  # Looks in the current directory.
  import(&quot;my_vars.gni&quot;)
</pre><h3><a class="h" name="not_needed" href="#not_needed"><span></span></a><strong>not_needed</strong>: Mark variables from scope as not needed.</h3><pre class="code">  not_needed(variable_list_or_star, variable_to_ignore_list = [])
  not_needed(from_scope, variable_list_or_star,
             variable_to_ignore_list = [])

  Mark the variables in the current or given scope as not needed, which means
  you will not get an error about unused variables for these. The
  variable_to_ignore_list allows excluding variables from &quot;all matches&quot; if
  variable_list_or_star is &quot;*&quot;.
</pre><h4><a class="h" name="Buildfile-functions-not_needed_Mark-variables-from-scope-as-not-needed-Example" href="#Buildfile-functions-not_needed_Mark-variables-from-scope-as-not-needed-Example"><span></span></a><a class="h" name="buildfile-functions-not_needed_mark-variables-from-scope-as-not-needed-example" href="#buildfile-functions-not_needed_mark-variables-from-scope-as-not-needed-example"><span></span></a><strong>Example</strong></h4><pre class="code">  not_needed(&quot;*&quot;, [ &quot;config&quot; ])
  not_needed([ &quot;data_deps&quot;, &quot;deps&quot; ])
  not_needed(invoker, &quot;*&quot;, [ &quot;config&quot; ])
  not_needed(invoker, [ &quot;data_deps&quot;, &quot;deps&quot; ])
</pre><h3><a class="h" name="pool-1" href="#pool-1"><span></span></a><strong>pool</strong>: Defines a pool object.</h3><pre class="code">  Pool objects can be applied to a tool to limit the parallelism of the
  build. This object has a single property &quot;depth&quot; corresponding to
  the number of tasks that may run simultaneously.

  As the file containing the pool definition may be executed in the
  context of more than one toolchain it is recommended to specify an
  explicit toolchain when defining and referencing a pool.

  A pool is referenced by its label just like a target.
</pre><h4><a class="h" name="Buildfile-functions-pool_Defines-a-pool-object-Variables" href="#Buildfile-functions-pool_Defines-a-pool-object-Variables"><span></span></a><a class="h" name="buildfile-functions-pool_defines-a-pool-object-variables" href="#buildfile-functions-pool_defines-a-pool-object-variables"><span></span></a><strong>Variables</strong></h4><pre class="code">  depth*
  * = required
</pre><h4><a class="h" name="Buildfile-functions-pool_Defines-a-pool-object-Example" href="#Buildfile-functions-pool_Defines-a-pool-object-Example"><span></span></a><a class="h" name="buildfile-functions-pool_defines-a-pool-object-example" href="#buildfile-functions-pool_defines-a-pool-object-example"><span></span></a><strong>Example</strong></h4><pre class="code">  if (current_toolchain == default_toolchain) {
    pool(&quot;link_pool&quot;) {
      depth = 1
    }
  }

  toolchain(&quot;toolchain&quot;) {
    tool(&quot;link&quot;) {
      command = &quot;...&quot;
      pool = &quot;:link_pool($default_toolchain)&quot;)
    }
  }
</pre><h3><a class="h" name="print" href="#print"><span></span></a><strong>print</strong>: Prints to the console.</h3><pre class="code">  Prints all arguments to the console separated by spaces. A newline is
  automatically appended to the end.

  This function is intended for debugging. Note that build files are run in
  parallel so you may get interleaved prints. A buildfile may also be executed
  more than once in parallel in the context of different toolchains so the
  prints from one file may be duplicated or
  interleaved with itself.
</pre><h4><a class="h" name="Buildfile-functions-print_Prints-to-the-console-Examples" href="#Buildfile-functions-print_Prints-to-the-console-Examples"><span></span></a><a class="h" name="buildfile-functions-print_prints-to-the-console-examples" href="#buildfile-functions-print_prints-to-the-console-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  print(&quot;Hello world&quot;)

  print(sources, deps)
</pre><h3><a class="h" name="process_file_template" href="#process_file_template"><span></span></a><strong>process_file_template</strong>: Do template expansion over a list of files.</h3><pre class="code">  process_file_template(source_list, template)

  process_file_template applies a template list to a source file list,
  returning the result of applying each template to each source. This is
  typically used for computing output file names from input files.

  In most cases, get_target_outputs() will give the same result with shorter,
  more maintainable code. This function should only be used when that function
  can&#39;t be used (like there&#39;s no target or the target is defined in another
  build file).
</pre><h4><a class="h" name="Buildfile-functions-process_file_template_Do-template-expansion-over-a-list-of-files-Arguments" href="#Buildfile-functions-process_file_template_Do-template-expansion-over-a-list-of-files-Arguments"><span></span></a><a class="h" name="buildfile-functions-process_file_template_do-template-expansion-over-a-list-of-files-arguments" href="#buildfile-functions-process_file_template_do-template-expansion-over-a-list-of-files-arguments"><span></span></a><strong>Arguments</strong></h4><pre class="code">  The source_list is a list of file names.

  The template can be a string or a list. If it is a list, multiple output
  strings are generated for each input.

  The template should contain source expansions to which each name in the
  source list is applied. See &quot;gn help source_expansion&quot;.
</pre><h4><a class="h" name="Buildfile-functions-process_file_template_Do-template-expansion-over-a-list-of-files-Example" href="#Buildfile-functions-process_file_template_Do-template-expansion-over-a-list-of-files-Example"><span></span></a><a class="h" name="buildfile-functions-process_file_template_do-template-expansion-over-a-list-of-files-example" href="#buildfile-functions-process_file_template_do-template-expansion-over-a-list-of-files-example"><span></span></a><strong>Example</strong></h4><pre class="code">  sources = [
    &quot;foo.idl&quot;,
    &quot;bar.idl&quot;,
  ]
  myoutputs = process_file_template(
      sources,
      [ &quot;$target_gen_dir/{{source_name_part}}.cc&quot;,
        &quot;$target_gen_dir/{{source_name_part}}.h&quot; ])

 The result in this case will be:
    [ &quot;//out/Debug/foo.cc&quot;
      &quot;//out/Debug/foo.h&quot;
      &quot;//out/Debug/bar.cc&quot;
      &quot;//out/Debug/bar.h&quot; ]
</pre><h3><a class="h" name="read_file" href="#read_file"><span></span></a><strong>read_file</strong>: Read a file into a variable.</h3><pre class="code">  read_file(filename, input_conversion)

  Whitespace will be trimmed from the end of the file. Throws an error if the
  file can not be opened.
</pre><h4><a class="h" name="Buildfile-functions-read_file_Read-a-file-into-a-variable-Arguments" href="#Buildfile-functions-read_file_Read-a-file-into-a-variable-Arguments"><span></span></a><a class="h" name="buildfile-functions-read_file_read-a-file-into-a-variable-arguments" href="#buildfile-functions-read_file_read-a-file-into-a-variable-arguments"><span></span></a><strong>Arguments</strong></h4><pre class="code">  filename
      Filename to read, relative to the build file.

  input_conversion
      Controls how the file is read and parsed. See &quot;gn help input_conversion&quot;.
</pre><h4><a class="h" name="Buildfile-functions-read_file_Read-a-file-into-a-variable-Example" href="#Buildfile-functions-read_file_Read-a-file-into-a-variable-Example"><span></span></a><a class="h" name="buildfile-functions-read_file_read-a-file-into-a-variable-example" href="#buildfile-functions-read_file_read-a-file-into-a-variable-example"><span></span></a><strong>Example</strong></h4><pre class="code">  lines = read_file(&quot;foo.txt&quot;, &quot;list lines&quot;)
</pre><h3><a class="h" name="rebase_path" href="#rebase_path"><span></span></a><strong>rebase_path</strong>: Rebase a file or directory to another location.</h3><pre class="code">  converted = rebase_path(input,
                          new_base = &quot;&quot;,
                          current_base = &quot;.&quot;)

  Takes a string argument representing a file name, or a list of such strings
  and converts it/them to be relative to a different base directory.

  When invoking the compiler or scripts, GN will automatically convert sources
  and include directories to be relative to the build directory. However, if
  you&#39;re passing files directly in the &quot;args&quot; array or doing other manual
  manipulations where GN doesn&#39;t know something is a file name, you will need
  to convert paths to be relative to what your tool is expecting.

  The common case is to use this to convert paths relative to the current
  directory to be relative to the build directory (which will be the current
  directory when executing scripts).

  If you want to convert a file path to be source-absolute (that is, beginning
  with a double slash like &quot;//foo/bar&quot;), you should use the get_path_info()
  function. This function won&#39;t work because it will always make relative
  paths, and it needs to support making paths relative to the source root, so
  can&#39;t also generate source-absolute paths without more special-cases.
</pre><h4><a class="h" name="Buildfile-functions-rebase_path_Rebase-a-file-or-directory-to-another-location-Arguments" href="#Buildfile-functions-rebase_path_Rebase-a-file-or-directory-to-another-location-Arguments"><span></span></a><a class="h" name="buildfile-functions-rebase_path_rebase-a-file-or-directory-to-another-location-arguments" href="#buildfile-functions-rebase_path_rebase-a-file-or-directory-to-another-location-arguments"><span></span></a><strong>Arguments</strong></h4><pre class="code">  input
      A string or list of strings representing file or directory names These
      can be relative paths (&quot;foo/bar.txt&quot;), system absolute paths
      (&quot;/foo/bar.txt&quot;), or source absolute paths (&quot;//foo/bar.txt&quot;).

  new_base
      The directory to convert the paths to be relative to. This can be an
      absolute path or a relative path (which will be treated as being relative
      to the current BUILD-file&#39;s directory).

      As a special case, if new_base is the empty string (the default), all
      paths will be converted to system-absolute native style paths with system
      path separators. This is useful for invoking external programs.

  current_base
      Directory representing the base for relative paths in the input. If this
      is not an absolute path, it will be treated as being relative to the
      current build file. Use &quot;.&quot; (the default) to convert paths from the
      current BUILD-file&#39;s directory.
</pre><h4><a class="h" name="Buildfile-functions-rebase_path_Rebase-a-file-or-directory-to-another-location-Return-value" href="#Buildfile-functions-rebase_path_Rebase-a-file-or-directory-to-another-location-Return-value"><span></span></a><a class="h" name="buildfile-functions-rebase_path_rebase-a-file-or-directory-to-another-location-return-value" href="#buildfile-functions-rebase_path_rebase-a-file-or-directory-to-another-location-return-value"><span></span></a><strong>Return value</strong></h4><pre class="code">  The return value will be the same type as the input value (either a string or
  a list of strings). All relative and source-absolute file names will be
  converted to be relative to the requested output System-absolute paths will
  be unchanged.

  Whether an output path will end in a slash will match whether the
  corresponding input path ends in a slash. It will return &quot;.&quot; or &quot;./&quot;
  (depending on whether the input ends in a slash) to avoid returning empty
  strings. This means if you want a root path (&quot;//&quot; or &quot;/&quot;) not ending in a
  slash, you can add a dot (&quot;//.&quot;).
</pre><h4><a class="h" name="Buildfile-functions-rebase_path_Rebase-a-file-or-directory-to-another-location-Example" href="#Buildfile-functions-rebase_path_Rebase-a-file-or-directory-to-another-location-Example"><span></span></a><a class="h" name="buildfile-functions-rebase_path_rebase-a-file-or-directory-to-another-location-example" href="#buildfile-functions-rebase_path_rebase-a-file-or-directory-to-another-location-example"><span></span></a><strong>Example</strong></h4><pre class="code">  # Convert a file in the current directory to be relative to the build
  # directory (the current dir when executing compilers and scripts).
  foo = rebase_path(&quot;myfile.txt&quot;, root_build_dir)
  # might produce &quot;../../project/myfile.txt&quot;.

  # Convert a file to be system absolute:
  foo = rebase_path(&quot;myfile.txt&quot;)
  # Might produce &quot;D:\\source\\project\\myfile.txt&quot; on Windows or
  # &quot;/home/you/source/project/myfile.txt&quot; on Linux.

  # Typical usage for converting to the build directory for a script.
  action(&quot;myscript&quot;) {
    # Don&#39;t convert sources, GN will automatically convert these to be relative
    # to the build directory when it constructs the command line for your
    # script.
    sources = [ &quot;foo.txt&quot;, &quot;bar.txt&quot; ]

    # Extra file args passed manually need to be explicitly converted
    # to be relative to the build directory:
    args = [
      &quot;--data&quot;,
      rebase_path(&quot;//mything/data/input.dat&quot;, root_build_dir),
      &quot;--rel&quot;,
      rebase_path(&quot;relative_path.txt&quot;, root_build_dir)
    ] + rebase_path(sources, root_build_dir)
  }
</pre><h3><a class="h" name="set_default_toolchain" href="#set_default_toolchain"><span></span></a><strong>set_default_toolchain</strong>: Sets the default toolchain name.</h3><pre class="code">  set_default_toolchain(toolchain_label)

  The given label should identify a toolchain definition (see &quot;gn help
  toolchain&quot;). This toolchain will be used for all targets unless otherwise
  specified.

  This function is only valid to call during the processing of the build
  configuration file. Since the build configuration file is processed
  separately for each toolchain, this function will be a no-op when called
  under any non-default toolchains.

  For example, the default toolchain should be appropriate for the current
  environment. If the current environment is 32-bit and somebody references a
  target with a 64-bit toolchain, we wouldn&#39;t want processing of the build
  config file for the 64-bit toolchain to reset the default toolchain to
  64-bit, we want to keep it 32-bits.
</pre><h4><a class="h" name="Argument" href="#Argument"><span></span></a><a class="h" name="argument" href="#argument"><span></span></a><strong>Argument</strong></h4><pre class="code">  toolchain_label
      Toolchain name.
</pre><h4><a class="h" name="Buildfile-functions-set_default_toolchain_Sets-the-default-toolchain-name-Example" href="#Buildfile-functions-set_default_toolchain_Sets-the-default-toolchain-name-Example"><span></span></a><a class="h" name="buildfile-functions-set_default_toolchain_sets-the-default-toolchain-name-example" href="#buildfile-functions-set_default_toolchain_sets-the-default-toolchain-name-example"><span></span></a><strong>Example</strong></h4><pre class="code">  # Set default toolchain only has an effect when run in the context of the
  # default toolchain. Pick the right one according to the current CPU
  # architecture.
  if (target_cpu == &quot;x64&quot;) {
    set_default_toolchain(&quot;//toolchains:64&quot;)
  } else if (target_cpu == &quot;x86&quot;) {
    set_default_toolchain(&quot;//toolchains:32&quot;)
  }
</pre><h3><a class="h" name="set_defaults" href="#set_defaults"><span></span></a><strong>set_defaults</strong>: Set default values for a target type.</h3><pre class="code">  set_defaults(&lt;target_type_name&gt;) { &lt;values...&gt; }

  Sets the default values for a given target type. Whenever target_type_name is
  seen in the future, the values specified in set_default&#39;s block will be
  copied into the current scope.

  When the target type is used, the variable copying is very strict. If a
  variable with that name is already in scope, the build will fail with an
  error.

  set_defaults can be used for built-in target types (&quot;executable&quot;,
  &quot;shared_library&quot;, etc.) and custom ones defined via the &quot;template&quot; command.
  It can be called more than once and the most recent call in any scope will
  apply, but there is no way to refer to the previous defaults and modify them
  (each call to set_defaults must supply a complete list of all defaults it
  wants). If you want to share defaults, store them in a separate variable.
</pre><h4><a class="h" name="Buildfile-functions-set_defaults_Set-default-values-for-a-target-type-Example" href="#Buildfile-functions-set_defaults_Set-default-values-for-a-target-type-Example"><span></span></a><a class="h" name="buildfile-functions-set_defaults_set-default-values-for-a-target-type-example" href="#buildfile-functions-set_defaults_set-default-values-for-a-target-type-example"><span></span></a><strong>Example</strong></h4><pre class="code">  set_defaults(&quot;static_library&quot;) {
    configs = [ &quot;//tools/mything:settings&quot; ]
  }

  static_library(&quot;mylib&quot;)
    # The configs will be auto-populated as above. You can remove it if
    # you don&#39;t want the default for a particular default:
    configs -= [ &quot;//tools/mything:settings&quot; ]
  }
</pre><h3><a class="h" name="set_sources_assignment_filter" href="#set_sources_assignment_filter"><span></span></a><strong>set_sources_assignment_filter</strong>: Set a pattern to filter source files.</h3><pre class="code">  The sources assignment filter is a list of patterns that remove files from
  the list implicitly whenever the &quot;sources&quot; variable is assigned to. This will
  do nothing for non-lists.

  This is intended to be used to globally filter out files with
  platform-specific naming schemes when they don&#39;t apply, for example you may
  want to filter out all &quot;*_win.cc&quot; files on non-Windows platforms.

  Typically this will be called once in the master build config script to set
  up the filter for the current platform. Subsequent calls will overwrite the
  previous values.

  If you want to bypass the filter and add a file even if it might be filtered
  out, call set_sources_assignment_filter([]) to clear the list of filters.
  This will apply until the current scope exits
</pre><h4><a class="h" name="How-to-use-patterns" href="#How-to-use-patterns"><span></span></a><a class="h" name="how-to-use-patterns" href="#how-to-use-patterns"><span></span></a><strong>How to use patterns</strong></h4><pre class="code">  File patterns are VERY limited regular expressions. They must match the
  entire input string to be counted as a match. In regular expression parlance,
  there is an implicit &quot;^...$&quot; surrounding your input. If you want to match a
  substring, you need to use wildcards at the beginning and end.

  There are only two special tokens understood by the pattern matcher.
  Everything else is a literal.

   - &quot;*&quot; Matches zero or more of any character. It does not depend on the
     preceding character (in regular expression parlance it is equivalent to
     &quot;.*&quot;).

   - &quot;\b&quot; Matches a path boundary. This will match the beginning or end of a
     string, or a slash.
</pre><h4><a class="h" name="Pattern-examples" href="#Pattern-examples"><span></span></a><a class="h" name="pattern-examples" href="#pattern-examples"><span></span></a><strong>Pattern examples</strong></h4><pre class="code">  &quot;*asdf*&quot;
      Matches a string containing &quot;asdf&quot; anywhere.

  &quot;asdf&quot;
      Matches only the exact string &quot;asdf&quot;.

  &quot;*.cc&quot;
      Matches strings ending in the literal &quot;.cc&quot;.

  &quot;\bwin/*&quot;
      Matches &quot;win/foo&quot; and &quot;foo/win/bar.cc&quot; but not &quot;iwin/foo&quot;.
</pre><h4><a class="h" name="Sources-assignment-example" href="#Sources-assignment-example"><span></span></a><a class="h" name="sources-assignment-example" href="#sources-assignment-example"><span></span></a><strong>Sources assignment example</strong></h4><pre class="code">  # Filter out all _win files.
  set_sources_assignment_filter([ &quot;*_win.cc&quot;, &quot;*_win.h&quot; ])
  sources = [ &quot;a.cc&quot;, &quot;b_win.cc&quot; ]
  print(sources)
  # Will print [ &quot;a.cc&quot; ]. b_win one was filtered out.
</pre><h3><a class="h" name="split_list" href="#split_list"><span></span></a><strong>split_list</strong>: Splits a list into N different sub-lists.</h3><pre class="code">  result = split_list(input, n)

  Given a list and a number N, splits the list into N sub-lists of
  approximately equal size. The return value is a list of the sub-lists. The
  result will always be a list of size N. If N is greater than the number of
  elements in the input, it will be padded with empty lists.

  The expected use is to divide source files into smaller uniform chunks.
</pre><h4><a class="h" name="Buildfile-functions-split_list_Splits-a-list-into-N-different-sub_lists-Example" href="#Buildfile-functions-split_list_Splits-a-list-into-N-different-sub_lists-Example"><span></span></a><a class="h" name="buildfile-functions-split_list_splits-a-list-into-n-different-sub_lists-example" href="#buildfile-functions-split_list_splits-a-list-into-n-different-sub_lists-example"><span></span></a><strong>Example</strong></h4><pre class="code">  The code:
    mylist = [1, 2, 3, 4, 5, 6]
    print(split_list(mylist, 3))

  Will print:
    [[1, 2], [3, 4], [5, 6]
</pre><h3><a class="h" name="template" href="#template"><span></span></a><strong>template</strong>: Define a template rule.</h3><pre class="code">  A template defines a custom name that acts like a function. It provides a way
  to add to the built-in target types.

  The template() function is used to declare a template. To invoke the
  template, just use the name of the template like any other target type.

  Often you will want to declare your template in a special file that other
  files will import (see &quot;gn help import&quot;) so your template rule can be shared
  across build files.
</pre><h4><a class="h" name="Variables-and-templates" href="#Variables-and-templates"><span></span></a><a class="h" name="variables-and-templates" href="#variables-and-templates"><span></span></a><strong>Variables and templates</strong>:</h4><pre class="code">  When you call template() it creates a closure around all variables currently
  in scope with the code in the template block. When the template is invoked,
  the closure will be executed.

  When the template is invoked, the code in the caller is executed and passed
  to the template code as an implicit &quot;invoker&quot; variable. The template uses
  this to read state out of the invoking code.

  One thing explicitly excluded from the closure is the &quot;current directory&quot;
  against which relative file names are resolved. The current directory will be
  that of the invoking code, since typically that code specifies the file
  names. This means all files internal to the template should use absolute
  names.

  A template will typically forward some or all variables from the invoking
  scope to a target that it defines. Often, such variables might be optional.
  Use the pattern:

    if (defined(invoker.deps)) {
      deps = invoker.deps
    }

  The function forward_variables_from() provides a shortcut to forward one or
  more or possibly all variables in this manner:

    forward_variables_from(invoker, [&quot;deps&quot;, &quot;public_deps&quot;])
</pre><h4><a class="h" name="Target-naming" href="#Target-naming"><span></span></a><a class="h" name="target-naming" href="#target-naming"><span></span></a><strong>Target naming</strong></h4><pre class="code">  Your template should almost always define a built-in target with the name the
  template invoker specified. For example, if you have an IDL template and
  somebody does:
    idl(&quot;foo&quot;) {...
  you will normally want this to expand to something defining a source_set or
  static_library named &quot;foo&quot; (among other things you may need). This way, when
  another target specifies a dependency on &quot;foo&quot;, the static_library or
  source_set will be linked.

  It is also important that any other targets your template expands to have
  unique names, or you will get collisions.

  Access the invoking name in your template via the implicit &quot;target_name&quot;
  variable. This should also be the basis for how other targets that a template
  expands to ensure uniqueness.

  A typical example would be a template that defines an action to generate some
  source files, and a source_set to compile that source. Your template would
  name the source_set &quot;target_name&quot; because that&#39;s what you want external
  targets to depend on to link your code. And you would name the action
  something like &quot;${target_name}_action&quot; to make it unique. The source set
  would have a dependency on the action to make it run.
</pre><h4><a class="h" name="Overriding-builtin-targets" href="#Overriding-builtin-targets"><span></span></a><a class="h" name="overriding-builtin-targets" href="#overriding-builtin-targets"><span></span></a><strong>Overriding builtin targets</strong></h4><pre class="code">  You can use template to redefine a built-in target in which case your template
  takes a precedence over the built-in one. All uses of the target from within
  the template definition will refer to the built-in target which makes it
  possible to extend the behavior of the built-in target:

    template(&quot;shared_library&quot;) {
      shared_library(shlib) {
        forward_variables_from(invoker, [ &quot;*&quot; ])
        ...
      }
    }
</pre><h4><a class="h" name="Example-of-defining-a-template" href="#Example-of-defining-a-template"><span></span></a><a class="h" name="example-of-defining-a-template" href="#example-of-defining-a-template"><span></span></a><strong>Example of defining a template</strong></h4><pre class="code">  template(&quot;my_idl&quot;) {
    # Be nice and help callers debug problems by checking that the variables
    # the template requires are defined. This gives a nice message rather than
    # giving the user an error about an undefined variable in the file defining
    # the template
    #
    # You can also use defined() to give default values to variables
    # unspecified by the invoker.
    assert(defined(invoker.sources),
           &quot;Need sources in $target_name listing the idl files.&quot;)

    # Name of the intermediate target that does the code gen. This must
    # incorporate the target name so it&#39;s unique across template
    # instantiations.
    code_gen_target_name = target_name + &quot;_code_gen&quot;

    # Intermediate target to convert IDL to C source. Note that the name is
    # based on the name the invoker of the template specified. This way, each
    # time the template is invoked we get a unique intermediate action name
    # (since all target names are in the global scope).
    action_foreach(code_gen_target_name) {
      # Access the scope defined by the invoker via the implicit &quot;invoker&quot;
      # variable.
      sources = invoker.sources

      # Note that we need an absolute path for our script file name. The
      # current directory when executing this code will be that of the invoker
      # (this is why we can use the &quot;sources&quot; directly above without having to
      # rebase all of the paths). But if we need to reference a script relative
      # to the template file, we&#39;ll need to use an absolute path instead.
      script = &quot;//tools/idl/idl_code_generator.py&quot;

      # Tell GN how to expand output names given the sources.
      # See &quot;gn help source_expansion&quot; for more.
      outputs = [ &quot;$target_gen_dir/{{source_name_part}}.cc&quot;,
                  &quot;$target_gen_dir/{{source_name_part}}.h&quot; ]
    }

    # Name the source set the same as the template invocation so instancing
    # this template produces something that other targets can link to in their
    # deps.
    source_set(target_name) {
      # Generates the list of sources, we get these from the action_foreach
      # above.
      sources = get_target_outputs(&quot;:$code_gen_target_name&quot;)

      # This target depends on the files produced by the above code gen target.
      deps = [ &quot;:$code_gen_target_name&quot; ]
    }
  }
</pre><h4><a class="h" name="Example-of-invoking-the-resulting-template" href="#Example-of-invoking-the-resulting-template"><span></span></a><a class="h" name="example-of-invoking-the-resulting-template" href="#example-of-invoking-the-resulting-template"><span></span></a><strong>Example of invoking the resulting template</strong></h4><pre class="code">  # This calls the template code above, defining target_name to be
  # &quot;foo_idl_files&quot; and &quot;invoker&quot; to be the set of stuff defined in the curly
  # brackets.
  my_idl(&quot;foo_idl_files&quot;) {
    # Goes into the template as &quot;invoker.sources&quot;.
    sources = [ &quot;foo.idl&quot;, &quot;bar.idl&quot; ]
  }

  # Here is a target that depends on our template.
  executable(&quot;my_exe&quot;) {
    # Depend on the name we gave the template call above. Internally, this will
    # produce a dependency from executable to the source_set inside the
    # template (since it has this name), which will in turn depend on the code
    # gen action.
    deps = [ &quot;:foo_idl_files&quot; ]
  }
</pre><h3><a class="h" name="tool" href="#tool"><span></span></a><strong>tool</strong>: Specify arguments to a toolchain tool.</h3><h4><a class="h" name="Buildfile-functions-tool_Specify-arguments-to-a-toolchain-tool-Usage" href="#Buildfile-functions-tool_Specify-arguments-to-a-toolchain-tool-Usage"><span></span></a><a class="h" name="buildfile-functions-tool_specify-arguments-to-a-toolchain-tool-usage" href="#buildfile-functions-tool_specify-arguments-to-a-toolchain-tool-usage"><span></span></a><strong>Usage</strong></h4><pre class="code">  tool(&lt;tool type&gt;) {
    &lt;tool variables...&gt;
  }
</pre><h4><a class="h" name="Tool-types" href="#Tool-types"><span></span></a><a class="h" name="tool-types" href="#tool-types"><span></span></a><strong>Tool types</strong></h4><pre class="code">    Compiler tools:
      &quot;cc&quot;: C compiler
      &quot;cxx&quot;: C++ compiler
      &quot;objc&quot;: Objective C compiler
      &quot;objcxx&quot;: Objective C++ compiler
      &quot;rc&quot;: Resource compiler (Windows .rc files)
      &quot;asm&quot;: Assembler

    Linker tools:
      &quot;alink&quot;: Linker for static libraries (archives)
      &quot;solink&quot;: Linker for shared libraries
      &quot;link&quot;: Linker for executables

    Other tools:
      &quot;stamp&quot;: Tool for creating stamp files
      &quot;copy&quot;: Tool to copy files.
      &quot;action&quot;: Defaults for actions

    Platform specific tools:
      &quot;copy_bundle_data&quot;: [iOS, macOS] Tool to copy files in a bundle.
      &quot;compile_xcassets&quot;: [iOS, macOS] Tool to compile asset catalogs.
</pre><h4><a class="h" name="Tool-variables" href="#Tool-variables"><span></span></a><a class="h" name="tool-variables" href="#tool-variables"><span></span></a><strong>Tool variables</strong></h4><pre class="code">    command  [string with substitutions]
        Valid for: all tools except &quot;action&quot; (required)

        The command to run.

    default_output_dir  [string with substitutions]
        Valid for: linker tools

        Default directory name for the output file relative to the
        root_build_dir. It can contain other substitution patterns. This will
        be the default value for the {{output_dir}} expansion (discussed below)
        but will be overridden by the &quot;output_dir&quot; variable in a target, if one
        is specified.

        GN doesn&#39;t do anything with this string other than pass it along,
        potentially with target-specific overrides. It is the tool&#39;s job to use
        the expansion so that the files will be in the right place.

    default_output_extension  [string]
        Valid for: linker tools

        Extension for the main output of a linkable tool. It includes the
        leading dot. This will be the default value for the
        {{output_extension}} expansion (discussed below) but will be overridden
        by by the &quot;output extension&quot; variable in a target, if one is specified.
        Empty string means no extension.

        GN doesn&#39;t actually do anything with this extension other than pass it
        along, potentially with target-specific overrides. One would typically
        use the {{output_extension}} value in the &quot;outputs&quot; to read this value.

        Example: default_output_extension = &quot;.exe&quot;

    depfile  [string with substitutions]
        Valid for: compiler tools (optional)

        If the tool can write &quot;.d&quot; files, this specifies the name of the
        resulting file. These files are used to list header file dependencies
        (or other implicit input dependencies) that are discovered at build
        time. See also &quot;depsformat&quot;.

        Example: depfile = &quot;{{output}}.d&quot;

    depsformat  [string]
        Valid for: compiler tools (when depfile is specified)

        Format for the deps outputs. This is either &quot;gcc&quot; or &quot;msvc&quot;. See the
        ninja documentation for &quot;deps&quot; for more information.

        Example: depsformat = &quot;gcc&quot;

    description  [string with substitutions, optional]
        Valid for: all tools

        What to print when the command is run.

        Example: description = &quot;Compiling {{source}}&quot;

    lib_switch  [string, optional, link tools only]
    lib_dir_switch  [string, optional, link tools only]
        Valid for: Linker tools except &quot;alink&quot;

        These strings will be prepended to the libraries and library search
        directories, respectively, because linkers differ on how specify them.
        If you specified:
          lib_switch = &quot;-l&quot;
          lib_dir_switch = &quot;-L&quot;
        then the &quot;{{libs}}&quot; expansion for [ &quot;freetype&quot;, &quot;expat&quot;] would be
        &quot;-lfreetype -lexpat&quot;.

    outputs  [list of strings with substitutions]
        Valid for: Linker and compiler tools (required)

        An array of names for the output files the tool produces. These are
        relative to the build output directory. There must always be at least
        one output file. There can be more than one output (a linker might
        produce a library and an import library, for example).

        This array just declares to GN what files the tool will produce. It is
        your responsibility to specify the tool command that actually produces
        these files.

        If you specify more than one output for shared library links, you
        should consider setting link_output, depend_output, and
        runtime_outputs.

        Example for a compiler tool that produces .obj files:
          outputs = [
            &quot;{{source_out_dir}}/{{source_name_part}}.obj&quot;
          ]

        Example for a linker tool that produces a .dll and a .lib. The use of
        {{target_output_name}}, {{output_extension}} and {{output_dir}} allows
        the target to override these values.
          outputs = [
            &quot;{{output_dir}}/{{target_output_name}}&quot;
                &quot;{{output_extension}}&quot;,
            &quot;{{output_dir}}/{{target_output_name}}.lib&quot;,
          ]

    pool [label, optional]
        Valid for: all tools (optional)

        Label of the pool to use for the tool. Pools are used to limit the
        number of tasks that can execute concurrently during the build.

        See also &quot;gn help pool&quot;.

    link_output  [string with substitutions]
    depend_output  [string with substitutions]
        Valid for: &quot;solink&quot; only (optional)

        These two files specify which of the outputs from the solink tool
        should be used for linking and dependency tracking. These should match
        entries in the &quot;outputs&quot;. If unspecified, the first item in the
        &quot;outputs&quot; array will be used for all. See &quot;Separate linking and
        dependencies for shared libraries&quot; below for more.

        On Windows, where the tools produce a .dll shared library and a .lib
        import library, you will want the first two to be the import library
        and the third one to be the .dll file. On Linux, if you&#39;re not doing
        the separate linking/dependency optimization, all of these should be
        the .so output.

    output_prefix  [string]
        Valid for: Linker tools (optional)

        Prefix to use for the output name. Defaults to empty. This prefix will
        be prepended to the name of the target (or the output_name if one is
        manually specified for it) if the prefix is not already there. The
        result will show up in the {{output_name}} substitution pattern.

        Individual targets can opt-out of the output prefix by setting:
          output_prefix_override = true
        (see &quot;gn help output_prefix_override&quot;).

        This is typically used to prepend &quot;lib&quot; to libraries on
        Posix systems:
          output_prefix = &quot;lib&quot;

    precompiled_header_type  [string]
        Valid for: &quot;cc&quot;, &quot;cxx&quot;, &quot;objc&quot;, &quot;objcxx&quot;

        Type of precompiled headers. If undefined or the empty string,
        precompiled headers will not be used for this tool. Otherwise use &quot;gcc&quot;
        or &quot;msvc&quot;.

        For precompiled headers to be used for a given target, the target (or a
        config applied to it) must also specify a &quot;precompiled_header&quot; and, for
        &quot;msvc&quot;-style headers, a &quot;precompiled_source&quot; value. If the type is
        &quot;gcc&quot;, then both &quot;precompiled_header&quot; and &quot;precompiled_source&quot; must
        resolve to the same file, despite the different formats required for
        each.&quot;

        See &quot;gn help precompiled_header&quot; for more.

    restat  [boolean]
        Valid for: all tools (optional, defaults to false)

        Requests that Ninja check the file timestamp after this tool has run to
        determine if anything changed. Set this if your tool has the ability to
        skip writing output if the output file has not changed.

        Normally, Ninja will assume that when a tool runs the output be new and
        downstream dependents must be rebuild. When this is set to trye, Ninja
        can skip rebuilding downstream dependents for input changes that don&#39;t
        actually affect the output.

        Example:
          restat = true

    rspfile  [string with substitutions]
        Valid for: all tools except &quot;action&quot; (optional)

        Name of the response file. If empty, no response file will be
        used. See &quot;rspfile_content&quot;.

    rspfile_content  [string with substitutions]
        Valid for: all tools except &quot;action&quot; (required when &quot;rspfile&quot; is used)

        The contents to be written to the response file. This may include all
        or part of the command to send to the tool which allows you to get
        around OS command-line length limits.

        This example adds the inputs and libraries to a response file, but
        passes the linker flags directly on the command line:
          tool(&quot;link&quot;) {
            command = &quot;link -o {{output}} {{ldflags}} @{{output}}.rsp&quot;
            rspfile = &quot;{{output}}.rsp&quot;
            rspfile_content = &quot;{{inputs}} {{solibs}} {{libs}}&quot;
          }

    runtime_outputs  [string list with substitutions]
        Valid for: linker tools

        If specified, this list is the subset of the outputs that should be
        added to runtime deps (see &quot;gn help runtime_deps&quot;). By default (if
        runtime_outputs is empty or unspecified), it will be the link_output.
</pre><h4><a class="h" name="Expansions-for-tool-variables" href="#Expansions-for-tool-variables"><span></span></a><a class="h" name="expansions-for-tool-variables" href="#expansions-for-tool-variables"><span></span></a><strong>Expansions for tool variables</strong></h4><pre class="code">  All paths are relative to the root build directory, which is the current
  directory for running all tools. These expansions are available to all tools:

    {{label}}
        The label of the current target. This is typically used in the
        &quot;description&quot; field for link tools. The toolchain will be omitted from
        the label for targets in the default toolchain, and will be included
        for targets in other toolchains.

    {{label_name}}
        The short name of the label of the target. This is the part after the
        colon. For &quot;//foo/bar:baz&quot; this will be &quot;baz&quot;. Unlike
        {{target_output_name}}, this is not affected by the &quot;output_prefix&quot; in
        the tool or the &quot;output_name&quot; set on the target.

    {{output}}
        The relative path and name of the output(s) of the current build step.
        If there is more than one output, this will expand to a list of all of
        them. Example: &quot;out/base/my_file.o&quot;

    {{target_gen_dir}}
    {{target_out_dir}}
        The directory of the generated file and output directories,
        respectively, for the current target. There is no trailing slash. See
        also {{output_dir}} for linker tools. Example: &quot;out/base/test&quot;

    {{target_output_name}}
        The short name of the current target with no path information, or the
        value of the &quot;output_name&quot; variable if one is specified in the target.
        This will include the &quot;output_prefix&quot; if any. See also {{label_name}}.

        Example: &quot;libfoo&quot; for the target named &quot;foo&quot; and an output prefix for
        the linker tool of &quot;lib&quot;.

  Compiler tools have the notion of a single input and a single output, along
  with a set of compiler-specific flags. The following expansions are
  available:

    {{asmflags}}
    {{cflags}}
    {{cflags_c}}
    {{cflags_cc}}
    {{cflags_objc}}
    {{cflags_objcc}}
    {{defines}}
    {{include_dirs}}
        Strings correspond that to the processed flags/defines/include
        directories specified for the target.
        Example: &quot;--enable-foo --enable-bar&quot;

        Defines will be prefixed by &quot;-D&quot; and include directories will be
        prefixed by &quot;-I&quot; (these work with Posix tools as well as Microsoft
        ones).

    {{source}}
        The relative path and name of the current input file.
        Example: &quot;../../base/my_file.cc&quot;

    {{source_file_part}}
        The file part of the source including the extension (with no directory
        information).
        Example: &quot;foo.cc&quot;

    {{source_name_part}}
        The filename part of the source file with no directory or extension.
        Example: &quot;foo&quot;

    {{source_gen_dir}}
    {{source_out_dir}}
        The directory in the generated file and output directories,
        respectively, for the current input file. If the source file is in the
        same directory as the target is declared in, they will will be the same
        as the &quot;target&quot; versions above. Example: &quot;gen/base/test&quot;

  Linker tools have multiple inputs and (potentially) multiple outputs The
  static library tool (&quot;alink&quot;) is not considered a linker tool. The following
  expansions are available:

    {{inputs}}
    {{inputs_newline}}
        Expands to the inputs to the link step. This will be a list of object
        files and static libraries.
        Example: &quot;obj/foo.o obj/bar.o obj/somelibrary.a&quot;

        The &quot;_newline&quot; version will separate the input files with newlines
        instead of spaces. This is useful in response files: some linkers can
        take a &quot;-filelist&quot; flag which expects newline separated files, and some
        Microsoft tools have a fixed-sized buffer for parsing each line of a
        response file.

    {{ldflags}}
        Expands to the processed set of ldflags and library search paths
        specified for the target.
        Example: &quot;-m64 -fPIC -pthread -L/usr/local/mylib&quot;

    {{libs}}
        Expands to the list of system libraries to link to. Each will be
        prefixed by the &quot;lib_prefix&quot;.

        As a special case to support Mac, libraries with names ending in
        &quot;.framework&quot; will be added to the {{libs}} with &quot;-framework&quot; preceeding
        it, and the lib prefix will be ignored.

        Example: &quot;-lfoo -lbar&quot;

    {{output_dir}}
        The value of the &quot;output_dir&quot; variable in the target, or the the value
        of the &quot;default_output_dir&quot; value in the tool if the target does not
        override the output directory. This will be relative to the
        root_build_dir and will not end in a slash. Will be &quot;.&quot; for output to
        the root_build_dir.

        This is subtly different than {{target_out_dir}} which is defined by GN
        based on the target&#39;s path and not overridable. {{output_dir}} is for
        the final output, {{target_out_dir}} is generally for object files and
        other outputs.

        Usually {{output_dir}} would be defined in terms of either
        {{target_out_dir}} or {{root_out_dir}}

    {{output_extension}}
        The value of the &quot;output_extension&quot; variable in the target, or the
        value of the &quot;default_output_extension&quot; value in the tool if the target
        does not specify an output extension.
        Example: &quot;.so&quot;

    {{solibs}}
        Extra libraries from shared library dependencide not specified in the
        {{inputs}}. This is the list of link_output files from shared libraries
        (if the solink tool specifies a &quot;link_output&quot; variable separate from
        the &quot;depend_output&quot;).

        These should generally be treated the same as libs by your tool.

        Example: &quot;libfoo.so libbar.so&quot;

  The static library (&quot;alink&quot;) tool allows {{arflags}} plus the common tool
  substitutions.

  The copy tool allows the common compiler/linker substitutions, plus
  {{source}} which is the source of the copy. The stamp tool allows only the
  common tool substitutions.

  The copy_bundle_data and compile_xcassets tools only allows the common tool
  substitutions. Both tools are required to create iOS/macOS bundles and need
  only be defined on those platforms.

  The copy_bundle_data tool will be called with one source and needs to copy
  (optionally optimizing the data representation) to its output. It may be
  called with a directory as input and it needs to be recursively copied.

  The compile_xcassets tool will be called with one or more source (each an
  asset catalog) that needs to be compiled to a single output. The following
  substitutions are avaiable:

    {{inputs}}
        Expands to the list of .xcassets to use as input to compile the asset
        catalog.

    {{bundle_product_type}}
        Expands to the product_type of the bundle that will contain the
        compiled asset catalog. Usually corresponds to the product_type
        property of the corresponding create_bundle target.

    {{bundle_partial_info_plist}}
        Expands to the path to the partial Info.plist generated by the
        assets catalog compiler. Usually based on the target_name of
        the create_bundle target.
</pre><h4><a class="h" name="Separate-linking-and-dependencies-for-shared-libraries" href="#Separate-linking-and-dependencies-for-shared-libraries"><span></span></a><a class="h" name="separate-linking-and-dependencies-for-shared-libraries" href="#separate-linking-and-dependencies-for-shared-libraries"><span></span></a><strong>Separate linking and dependencies for shared libraries</strong></h4><pre class="code">  Shared libraries are special in that not all changes to them require that
  dependent targets be re-linked. If the shared library is changed but no
  imports or exports are different, dependent code needn&#39;t be relinked, which
  can speed up the build.

  If your link step can output a list of exports from a shared library and
  writes the file only if the new one is different, the timestamp of this file
  can be used for triggering re-links, while the actual shared library would be
  used for linking.

  You will need to specify
    restat = true
  in the linker tool to make this work, so Ninja will detect if the timestamp
  of the dependency file has changed after linking (otherwise it will always
  assume that running a command updates the output):

    tool(&quot;solink&quot;) {
      command = &quot;...&quot;
      outputs = [
        &quot;{{output_dir}}/{{target_output_name}}{{output_extension}}&quot;,
        &quot;{{output_dir}}/{{target_output_name}}&quot;
            &quot;{{output_extension}}.TOC&quot;,
      ]
      link_output =
        &quot;{{output_dir}}/{{target_output_name}}{{output_extension}}&quot;
      depend_output =
        &quot;{{output_dir}}/{{target_output_name}}&quot;
            &quot;{{output_extension}}.TOC&quot;
      restat = true
    }
</pre><h4><a class="h" name="Buildfile-functions-tool_Specify-arguments-to-a-toolchain-tool-Example" href="#Buildfile-functions-tool_Specify-arguments-to-a-toolchain-tool-Example"><span></span></a><a class="h" name="buildfile-functions-tool_specify-arguments-to-a-toolchain-tool-example" href="#buildfile-functions-tool_specify-arguments-to-a-toolchain-tool-example"><span></span></a><strong>Example</strong></h4><pre class="code">  toolchain(&quot;my_toolchain&quot;) {
    # Put these at the top to apply to all tools below.
    lib_prefix = &quot;-l&quot;
    lib_dir_prefix = &quot;-L&quot;

    tool(&quot;cc&quot;) {
      command = &quot;gcc {{source}} -o {{output}}&quot;
      outputs = [ &quot;{{source_out_dir}}/{{source_name_part}}.o&quot; ]
      description = &quot;GCC {{source}}&quot;
    }
    tool(&quot;cxx&quot;) {
      command = &quot;g++ {{source}} -o {{output}}&quot;
      outputs = [ &quot;{{source_out_dir}}/{{source_name_part}}.o&quot; ]
      description = &quot;G++ {{source}}&quot;
    }
  };
</pre><h3><a class="h" name="toolchain" href="#toolchain"><span></span></a><strong>toolchain</strong>: Defines a toolchain.</h3><pre class="code">  A toolchain is a set of commands and build flags used to compile the source
  code. The toolchain() function defines these commands.
</pre><h4><a class="h" name="Toolchain-overview" href="#Toolchain-overview"><span></span></a><a class="h" name="toolchain-overview" href="#toolchain-overview"><span></span></a><strong>Toolchain overview</strong></h4><pre class="code">  You can have more than one toolchain in use at once in a build and a target
  can exist simultaneously in multiple toolchains. A build file is executed
  once for each toolchain it is referenced in so the GN code can vary all
  parameters of each target (or which targets exist) on a per-toolchain basis.

  When you have a simple build with only one toolchain, the build config file
  is loaded only once at the beginning of the build. It must call
  set_default_toolchain() (see &quot;gn help set_default_toolchain&quot;) to tell GN the
  label of the toolchain definition to use. The &quot;toolchain_args&quot; section of the
  toolchain definition is ignored.

  When a target has a dependency on a target using different toolchain (see &quot;gn
  help labels&quot; for how to specify this), GN will start a build using that
  secondary toolchain to resolve the target. GN will load the build config file
  with the build arguements overridden as specified in the toolchain_args.
  Because the default toolchain is already known, calls to
  set_default_toolchain() are ignored.

  To load a file in an alternate toolchain, GN does the following:

    1. Loads the file with the toolchain definition in it (as determined by the
       toolchain label).
    2. Re-runs the master build configuration file, applying the arguments
       specified by the toolchain_args section of the toolchain definition.
    3. Loads the destination build file in the context of the configuration file
       in the previous step.

  The toolchain configuration is two-way. In the default toolchain (i.e. the
  main build target) the configuration flows from the build config file to the
  toolchain. The build config file looks at the state of the build (OS type,
  CPU architecture, etc.) and decides which toolchain to use (via
  set_default_toolchain()). In secondary toolchains, the configuration flows
  from the toolchain to the build config file: the &quot;toolchain_args&quot; in the
  toolchain definition specifies the arguments to re-invoke the build.
</pre><h4><a class="h" name="Functions-and-variables" href="#Functions-and-variables"><span></span></a><a class="h" name="functions-and-variables" href="#functions-and-variables"><span></span></a><strong>Functions and variables</strong></h4><pre class="code">  tool()
    The tool() function call specifies the commands commands to run for a given
    step. See &quot;gn help tool&quot;.

  toolchain_args
    Overrides for build arguments to pass to the toolchain when invoking it.
    This is a variable of type &quot;scope&quot; where the variable names correspond to
    variables in declare_args() blocks.

    When you specify a target using an alternate toolchain, the master build
    configuration file is re-interpreted in the context of that toolchain.
    toolchain_args allows you to control the arguments passed into this
    alternate invocation of the build.

    Any default system arguments or arguments passed in via &quot;gn args&quot; will also
    be passed to the alternate invocation unless explicitly overridden by
    toolchain_args.

    The toolchain_args will be ignored when the toolchain being defined is the
    default. In this case, it&#39;s expected you want the default argument values.

    See also &quot;gn help buildargs&quot; for an overview of these arguments.

  deps
    Dependencies of this toolchain. These dependencies will be resolved before
    any target in the toolchain is compiled. To avoid circular dependencies
    these must be targets defined in another toolchain.

    This is expressed as a list of targets, and generally these targets will
    always specify a toolchain:
      deps = [ &quot;//foo/bar:baz(//build/toolchain:bootstrap)&quot; ]

    This concept is somewhat inefficient to express in Ninja (it requires a lot
    of duplicate of rules) so should only be used when absolutely necessary.
</pre><h4><a class="h" name="Example-of-defining-a-toolchain" href="#Example-of-defining-a-toolchain"><span></span></a><a class="h" name="example-of-defining-a-toolchain" href="#example-of-defining-a-toolchain"><span></span></a><strong>Example of defining a toolchain</strong></h4><pre class="code">  toolchain(&quot;32&quot;) {
    tool(&quot;cc&quot;) {
      command = &quot;gcc {{source}}&quot;
      ...
    }

    toolchain_args = {
      use_doom_melon = true  # Doom melon always required for 32-bit builds.
      current_cpu = &quot;x86&quot;
    }
  }

  toolchain(&quot;64&quot;) {
    tool(&quot;cc&quot;) {
      command = &quot;gcc {{source}}&quot;
      ...
    }

    toolchain_args = {
      # use_doom_melon is not overridden here, it will take the default.
      current_cpu = &quot;x64&quot;
    }
  }
</pre><h4><a class="h" name="Example-of-cross_toolchain-dependencies" href="#Example-of-cross_toolchain-dependencies"><span></span></a><a class="h" name="example-of-cross_toolchain-dependencies" href="#example-of-cross_toolchain-dependencies"><span></span></a><strong>Example of cross-toolchain dependencies</strong></h4><pre class="code">  If a 64-bit target wants to depend on a 32-bit binary, it would specify a
  dependency using data_deps (data deps are like deps that are only needed at
  runtime and aren&#39;t linked, since you can&#39;t link a 32-bit and a 64-bit
  library).

    executable(&quot;my_program&quot;) {
      ...
      if (target_cpu == &quot;x64&quot;) {
        # The 64-bit build needs this 32-bit helper.
        data_deps = [ &quot;:helper(//toolchains:32)&quot; ]
      }
    }

    if (target_cpu == &quot;x86&quot;) {
      # Our helper library is only compiled in 32-bits.
      shared_library(&quot;helper&quot;) {
        ...
      }
    }
</pre><h3><a class="h" name="write_file" href="#write_file"><span></span></a><strong>write_file</strong>: Write a file to disk.</h3><pre class="code">  write_file(filename, data)

  If data is a list, the list will be written one-item-per-line with no quoting
  or brackets.

  If the file exists and the contents are identical to that being written, the
  file will not be updated. This will prevent unnecessary rebuilds of targets
  that depend on this file.

  One use for write_file is to write a list of inputs to an script that might
  be too long for the command line. However, it is preferrable to use response
  files for this purpose. See &quot;gn help response_file_contents&quot;.

  TODO(brettw) we probably need an optional third argument to control list
  formatting.
</pre><h4><a class="h" name="Buildfile-functions-write_file_Write-a-file-to-disk-Arguments" href="#Buildfile-functions-write_file_Write-a-file-to-disk-Arguments"><span></span></a><a class="h" name="buildfile-functions-write_file_write-a-file-to-disk-arguments" href="#buildfile-functions-write_file_write-a-file-to-disk-arguments"><span></span></a><strong>Arguments</strong></h4><pre class="code">  filename
      Filename to write. This must be within the output directory.

  data
      The list or string to write.
</pre><h2><a class="h" name="predefined_variables" href="#predefined_variables"><span></span></a>Built-in predefined variables</h2><h3><a class="h" name="current_cpu" href="#current_cpu"><span></span></a><strong>current_cpu</strong>: The processor architecture of the current toolchain.</h3><pre class="code">  The build configuration usually sets this value based on the value of
  &quot;host_cpu&quot; (see &quot;gn help host_cpu&quot;) and then threads this through the
  toolchain definitions to ensure that it always reflects the appropriate
  value.

  This value is not used internally by GN for any purpose. It is set it to the
  empty string (&quot;&quot;) by default but is declared so that it can be overridden on
  the command line if so desired.

  See &quot;gn help target_cpu&quot; for a list of common values returned.
</pre><h3><a class="h" name="current_os" href="#current_os"><span></span></a><strong>current_os</strong>: The operating system of the current toolchain.</h3><pre class="code">  The build configuration usually sets this value based on the value of
  &quot;target_os&quot; (see &quot;gn help target_os&quot;), and then threads this through the
  toolchain definitions to ensure that it always reflects the appropriate
  value.

  This value is not used internally by GN for any purpose. It is set it to the
  empty string (&quot;&quot;) by default but is declared so that it can be overridden on
  the command line if so desired.

  See &quot;gn help target_os&quot; for a list of common values returned.
</pre><h3><a class="h" name="current_toolchain" href="#current_toolchain"><span></span></a><strong>current_toolchain</strong>: Label of the current toolchain.</h3><pre class="code">  A fully-qualified label representing the current toolchain. You can use this
  to make toolchain-related decisions in the build. See also
  &quot;default_toolchain&quot;.
</pre><h4><a class="h" name="Built_in-predefined-variables-current_toolchain_Label-of-the-current-toolchain-Example" href="#Built_in-predefined-variables-current_toolchain_Label-of-the-current-toolchain-Example"><span></span></a><a class="h" name="built_in-predefined-variables-current_toolchain_label-of-the-current-toolchain-example" href="#built_in-predefined-variables-current_toolchain_label-of-the-current-toolchain-example"><span></span></a><strong>Example</strong></h4><pre class="code">  if (current_toolchain == &quot;//build:64_bit_toolchain&quot;) {
    executable(&quot;output_thats_64_bit_only&quot;) {
      ...
</pre><h3><a class="h" name="default_toolchain" href="#default_toolchain"><span></span></a><strong>default_toolchain</strong>: [string] Label of the default toolchain.</h3><pre class="code">  A fully-qualified label representing the default toolchain, which may not
  necessarily be the current one (see &quot;current_toolchain&quot;).
</pre><h3><a class="h" name="host_cpu" href="#host_cpu"><span></span></a><strong>host_cpu</strong>: The processor architecture that GN is running on.</h3><pre class="code">  This is value is exposed so that cross-compile toolchains can access the host
  architecture when needed.

  The value should generally be considered read-only, but it can be overriden
  in order to handle unusual cases where there might be multiple plausible
  values for the host architecture (e.g., if you can do either 32-bit or 64-bit
  builds). The value is not used internally by GN for any purpose.
</pre><h4><a class="h" name="Built_in-predefined-variables-host_cpu_The-processor-architecture-that-GN-is-running-on-Some-possible-values" href="#Built_in-predefined-variables-host_cpu_The-processor-architecture-that-GN-is-running-on-Some-possible-values"><span></span></a><a class="h" name="built_in-predefined-variables-host_cpu_the-processor-architecture-that-gn-is-running-on-some-possible-values" href="#built_in-predefined-variables-host_cpu_the-processor-architecture-that-gn-is-running-on-some-possible-values"><span></span></a><strong>Some possible values</strong></h4><pre class="code">  - &quot;x64&quot;
  - &quot;x86&quot;
</pre><h3><a class="h" name="host_os" href="#host_os"><span></span></a><strong>host_os</strong>: [string] The operating system that GN is running on.</h3><pre class="code">  This value is exposed so that cross-compiles can access the host build
  system&#39;s settings.

  This value should generally be treated as read-only. It, however, is not used
  internally by GN for any purpose.
</pre><h4><a class="h" name="Built_in-predefined-variables-host_os_string_The-operating-system-that-GN-is-running-on-Some-possible-values" href="#Built_in-predefined-variables-host_os_string_The-operating-system-that-GN-is-running-on-Some-possible-values"><span></span></a><a class="h" name="built_in-predefined-variables-host_os_string_the-operating-system-that-gn-is-running-on-some-possible-values" href="#built_in-predefined-variables-host_os_string_the-operating-system-that-gn-is-running-on-some-possible-values"><span></span></a><strong>Some possible values</strong></h4><pre class="code">  - &quot;linux&quot;
  - &quot;mac&quot;
  - &quot;win&quot;
</pre><h3><a class="h" name="invoker" href="#invoker"><span></span></a><strong>invoker</strong>: [string] The invoking scope inside a template.</h3><pre class="code">  Inside a template invocation, this variable refers to the scope of the
  invoker of the template. Outside of template invocations, this variable is
  undefined.

  All of the variables defined inside the template invocation are accessible as
  members of the &quot;invoker&quot; scope. This is the way that templates read values
  set by the callers.

  This is often used with &quot;defined&quot; to see if a value is set on the invoking
  scope.

  See &quot;gn help template&quot; for more examples.
</pre><h4><a class="h" name="Built_in-predefined-variables-invoker_string_The-invoking-scope-inside-a-template-Example" href="#Built_in-predefined-variables-invoker_string_The-invoking-scope-inside-a-template-Example"><span></span></a><a class="h" name="built_in-predefined-variables-invoker_string_the-invoking-scope-inside-a-template-example" href="#built_in-predefined-variables-invoker_string_the-invoking-scope-inside-a-template-example"><span></span></a><strong>Example</strong></h4><pre class="code">  template(&quot;my_template&quot;) {
    print(invoker.sources)       # Prints [ &quot;a.cc&quot;, &quot;b.cc&quot; ]
    print(defined(invoker.foo))  # Prints false.
    print(defined(invoker.bar))  # Prints true.
  }

  my_template(&quot;doom_melon&quot;) {
    sources = [ &quot;a.cc&quot;, &quot;b.cc&quot; ]
    bar = 123
  }
</pre><h3><a class="h" name="python_path" href="#python_path"><span></span></a><strong>python_path</strong>: Absolute path of Python.</h3><pre class="code">  Normally used in toolchain definitions if running some command requires
  Python. You will normally not need this when invoking scripts since GN
  automatically finds it for you.
</pre><h3><a class="h" name="root_build_dir" href="#root_build_dir"><span></span></a><strong>root_build_dir</strong>: [string] Directory where build commands are run.</h3><pre class="code">  This is the root build output directory which will be the current directory
  when executing all compilers and scripts.

  Most often this is used with rebase_path (see &quot;gn help rebase_path&quot;) to
  convert arguments to be relative to a script&#39;s current directory.
</pre><h3><a class="h" name="root_gen_dir" href="#root_gen_dir"><span></span></a><strong>root_gen_dir</strong>: Directory for the toolchain&#39;s generated files.</h3><pre class="code">  Absolute path to the root of the generated output directory tree for the
  current toolchain. An example would be &quot;//out/Debug/gen&quot; for the default
  toolchain, or &quot;//out/Debug/arm/gen&quot; for the &quot;arm&quot; toolchain.

  This is primarily useful for setting up include paths for generated files. If
  you are passing this to a script, you will want to pass it through
  rebase_path() (see &quot;gn help rebase_path&quot;) to convert it to be relative to the
  build directory.

  See also &quot;target_gen_dir&quot; which is usually a better location for generated
  files. It will be inside the root generated dir.
</pre><h3><a class="h" name="root_out_dir" href="#root_out_dir"><span></span></a><strong>root_out_dir</strong>: [string] Root directory for toolchain output files.</h3><pre class="code">  Absolute path to the root of the output directory tree for the current
  toolchain. It will not have a trailing slash.

  For the default toolchain this will be the same as the root_build_dir. An
  example would be &quot;//out/Debug&quot; for the default toolchain, or
  &quot;//out/Debug/arm&quot; for the &quot;arm&quot; toolchain.

  This is primarily useful for setting up script calls. If you are passing this
  to a script, you will want to pass it through rebase_path() (see &quot;gn help
  rebase_path&quot;) to convert it to be relative to the build directory.

  See also &quot;target_out_dir&quot; which is usually a better location for output
  files. It will be inside the root output dir.
</pre><h4><a class="h" name="Built_in-predefined-variables-root_out_dir_string_Root-directory-for-toolchain-output-files-Example" href="#Built_in-predefined-variables-root_out_dir_string_Root-directory-for-toolchain-output-files-Example"><span></span></a><a class="h" name="built_in-predefined-variables-root_out_dir_string_root-directory-for-toolchain-output-files-example" href="#built_in-predefined-variables-root_out_dir_string_root-directory-for-toolchain-output-files-example"><span></span></a><strong>Example</strong></h4><pre class="code">  action(&quot;myscript&quot;) {
    # Pass the output dir to the script.
    args = [ &quot;-o&quot;, rebase_path(root_out_dir, root_build_dir) ]
  }
</pre><h3><a class="h" name="target_cpu" href="#target_cpu"><span></span></a><strong>target_cpu</strong>: The desired cpu architecture for the build.</h3><pre class="code">  This value should be used to indicate the desired architecture for the
  primary objects of the build. It will match the cpu architecture of the
  default toolchain, but not necessarily the current toolchain.

  In many cases, this is the same as &quot;host_cpu&quot;, but in the case of
  cross-compiles, this can be set to something different. This value is
  different from &quot;current_cpu&quot; in that it does not change based on the current
  toolchain. When writing rules, &quot;current_cpu&quot; should be used rather than
  &quot;target_cpu&quot; most of the time.

  This value is not used internally by GN for any purpose, so it may be set to
  whatever value is needed for the build. GN defaults this value to the empty
  string (&quot;&quot;) and the configuration files should set it to an appropriate value
  (e.g., setting it to the value of &quot;host_cpu&quot;) if it is not overridden on the
  command line or in the args.gn file.
</pre><h4><a class="h" name="Built_in-predefined-variables-target_cpu_The-desired-cpu-architecture-for-the-build-Possible-values" href="#Built_in-predefined-variables-target_cpu_The-desired-cpu-architecture-for-the-build-Possible-values"><span></span></a><a class="h" name="built_in-predefined-variables-target_cpu_the-desired-cpu-architecture-for-the-build-possible-values" href="#built_in-predefined-variables-target_cpu_the-desired-cpu-architecture-for-the-build-possible-values"><span></span></a><strong>Possible values</strong></h4><pre class="code">  - &quot;x86&quot;
  - &quot;x64&quot;
  - &quot;arm&quot;
  - &quot;arm64&quot;
  - &quot;mipsel&quot;
</pre><h3><a class="h" name="target_gen_dir" href="#target_gen_dir"><span></span></a><strong>target_gen_dir</strong>: Directory for a target&#39;s generated files.</h3><pre class="code">  Absolute path to the target&#39;s generated file directory. This will be the
  &quot;root_gen_dir&quot; followed by the relative path to the current build file. If
  your file is in &quot;//tools/doom_melon&quot; then target_gen_dir would be
  &quot;//out/Debug/gen/tools/doom_melon&quot;. It will not have a trailing slash.

  This is primarily useful for setting up include paths for generated files. If
  you are passing this to a script, you will want to pass it through
  rebase_path() (see &quot;gn help rebase_path&quot;) to convert it to be relative to the
  build directory.

  See also &quot;gn help root_gen_dir&quot;.
</pre><h4><a class="h" name="Built_in-predefined-variables-target_gen_dir_Directory-for-a-target_s-generated-files-Example" href="#Built_in-predefined-variables-target_gen_dir_Directory-for-a-target_s-generated-files-Example"><span></span></a><a class="h" name="built_in-predefined-variables-target_gen_dir_directory-for-a-target_s-generated-files-example" href="#built_in-predefined-variables-target_gen_dir_directory-for-a-target_s-generated-files-example"><span></span></a><strong>Example</strong></h4><pre class="code">  action(&quot;myscript&quot;) {
    # Pass the generated output dir to the script.
    args = [ &quot;-o&quot;, rebase_path(target_gen_dir, root_build_dir) ]&quot;
  }
</pre><h3><a class="h" name="target_name" href="#target_name"><span></span></a><strong>target_name</strong>: [string] The name of the current target.</h3><pre class="code">  Inside a target or template invocation, this variable refers to the name
  given to the target or template invocation. Outside of these, this variable
  is undefined.

  This is most often used in template definitions to name targets defined in
  the template based on the name of the invocation. This is necessary both to
  ensure generated targets have unique names and to generate a target with the
  exact name of the invocation that other targets can depend on.

  Be aware that this value will always reflect the innermost scope. So when
  defining a target inside a template, target_name will refer to the target
  rather than the template invocation. To get the name of the template
  invocation in this case, you should save target_name to a temporary variable
  outside of any target definitions.

  See &quot;gn help template&quot; for more examples.
</pre><h4><a class="h" name="Built_in-predefined-variables-target_name_string_The-name-of-the-current-target-Example" href="#Built_in-predefined-variables-target_name_string_The-name-of-the-current-target-Example"><span></span></a><a class="h" name="built_in-predefined-variables-target_name_string_the-name-of-the-current-target-example" href="#built_in-predefined-variables-target_name_string_the-name-of-the-current-target-example"><span></span></a><strong>Example</strong></h4><pre class="code">  executable(&quot;doom_melon&quot;) {
    print(target_name)    # Prints &quot;doom_melon&quot;.
  }

  template(&quot;my_template&quot;) {
    print(target_name)    # Prints &quot;space_ray&quot; when invoked below.

    executable(target_name + &quot;_impl&quot;) {
      print(target_name)  # Prints &quot;space_ray_impl&quot;.
    }
  }

  my_template(&quot;space_ray&quot;) {
  }
</pre><h3><a class="h" name="target_os" href="#target_os"><span></span></a><strong>target_os</strong>: The desired operating system for the build.</h3><pre class="code">  This value should be used to indicate the desired operating system for the
  primary object(s) of the build. It will match the OS of the default
  toolchain.

  In many cases, this is the same as &quot;host_os&quot;, but in the case of
  cross-compiles, it may be different. This variable differs from &quot;current_os&quot;
  in that it can be referenced from inside any toolchain and will always return
  the initial value.

  This should be set to the most specific value possible. So, &quot;android&quot; or
  &quot;chromeos&quot; should be used instead of &quot;linux&quot; where applicable, even though
  Android and ChromeOS are both Linux variants. This can mean that one needs to
  write

      if (target_os == &quot;android&quot; || target_os == &quot;linux&quot;) {
          # ...
      }

  and so forth.

  This value is not used internally by GN for any purpose, so it may be set to
  whatever value is needed for the build. GN defaults this value to the empty
  string (&quot;&quot;) and the configuration files should set it to an appropriate value
  (e.g., setting it to the value of &quot;host_os&quot;) if it is not set via the command
  line or in the args.gn file.
</pre><h4><a class="h" name="Built_in-predefined-variables-target_os_The-desired-operating-system-for-the-build-Possible-values" href="#Built_in-predefined-variables-target_os_The-desired-operating-system-for-the-build-Possible-values"><span></span></a><a class="h" name="built_in-predefined-variables-target_os_the-desired-operating-system-for-the-build-possible-values" href="#built_in-predefined-variables-target_os_the-desired-operating-system-for-the-build-possible-values"><span></span></a><strong>Possible values</strong></h4><pre class="code">  - &quot;android&quot;
  - &quot;chromeos&quot;
  - &quot;ios&quot;
  - &quot;linux&quot;
  - &quot;nacl&quot;
  - &quot;mac&quot;
  - &quot;win&quot;
</pre><h3><a class="h" name="target_out_dir" href="#target_out_dir"><span></span></a><strong>target_out_dir</strong>: [string] Directory for target output files.</h3><pre class="code">  Absolute path to the target&#39;s generated file directory. If your current
  target is in &quot;//tools/doom_melon&quot; then this value might be
  &quot;//out/Debug/obj/tools/doom_melon&quot;. It will not have a trailing slash.

  This is primarily useful for setting up arguments for calling scripts. If you
  are passing this to a script, you will want to pass it through rebase_path()
  (see &quot;gn help rebase_path&quot;) to convert it to be relative to the build
  directory.

  See also &quot;gn help root_out_dir&quot;.
</pre><h4><a class="h" name="Built_in-predefined-variables-target_out_dir_string_Directory-for-target-output-files-Example" href="#Built_in-predefined-variables-target_out_dir_string_Directory-for-target-output-files-Example"><span></span></a><a class="h" name="built_in-predefined-variables-target_out_dir_string_directory-for-target-output-files-example" href="#built_in-predefined-variables-target_out_dir_string_directory-for-target-output-files-example"><span></span></a><strong>Example</strong></h4><pre class="code">  action(&quot;myscript&quot;) {
    # Pass the output dir to the script.
    args = [ &quot;-o&quot;, rebase_path(target_out_dir, root_build_dir) ]&quot;

  }
</pre><h2><a class="h" name="target_variables" href="#target_variables"><span></span></a>Variables you set in targets</h2><h3><a class="h" name="all_dependent_configs" href="#all_dependent_configs"><span></span></a><strong>all_dependent_configs</strong>: Configs to be forced on dependents.</h3><pre class="code">  A list of config labels.

  All targets depending on this one, and recursively, all targets depending on
  those, will have the configs listed in this variable added to them. These
  configs will also apply to the current target.

  This addition happens in a second phase once a target and all of its
  dependencies have been resolved. Therefore, a target will not see these
  force-added configs in their &quot;configs&quot; variable while the script is running,
  and they can not be removed. As a result, this capability should generally
  only be used to add defines and include directories necessary to compile a
  target&#39;s headers.

  See also &quot;public_configs&quot;.
</pre><h4><a class="h" name="Variables-you-set-in-targets-all_dependent_configs_Configs-to-be-forced-on-dependents-Ordering-of-flags-and-values" href="#Variables-you-set-in-targets-all_dependent_configs_Configs-to-be-forced-on-dependents-Ordering-of-flags-and-values"><span></span></a><a class="h" name="variables-you-set-in-targets-all_dependent_configs_configs-to-be-forced-on-dependents-ordering-of-flags-and-values" href="#variables-you-set-in-targets-all_dependent_configs_configs-to-be-forced-on-dependents-ordering-of-flags-and-values"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.
</pre><h3><a class="h" name="allow_circular_includes_from" href="#allow_circular_includes_from"><span></span></a><strong>allow_circular_includes_from</strong>: Permit includes from deps.</h3><pre class="code">  A list of target labels. Must be a subset of the target&#39;s &quot;deps&quot;. These
  targets will be permitted to include headers from the current target despite
  the dependency going in the opposite direction.

  When you use this, both targets must be included in a final binary for it to
  link. To keep linker errors from happening, it is good practice to have all
  external dependencies depend only on one of the two targets, and to set the
  visibility on the other to enforce this. Thus the targets will always be
  linked together in any output.
</pre><h4><a class="h" name="Details" href="#Details"><span></span></a><a class="h" name="details" href="#details"><span></span></a><strong>Details</strong></h4><pre class="code">  Normally, for a file in target A to include a file from target B, A must list
  B as a dependency. This invariant is enforced by the &quot;gn check&quot; command (and
  the --check flag to &quot;gn gen&quot; -- see &quot;gn help check&quot;).

  Sometimes, two targets might be the same unit for linking purposes (two
  source sets or static libraries that would always be linked together in a
  final executable or shared library) and they each include headers from the
  other: you want A to be able to include B&#39;s headers, and B to include A&#39;s
  headers. This is not an ideal situation but is sometimes unavoidable.

  This list, if specified, lists which of the dependencies of the current
  target can include header files from the current target. That is, if A
  depends on B, B can only include headers from A if it is in A&#39;s
  allow_circular_includes_from list. Normally includes must follow the
  direction of dependencies, this flag allows them to go in the opposite
  direction.
</pre><h4><a class="h" name="Danger" href="#Danger"><span></span></a><a class="h" name="danger" href="#danger"><span></span></a><strong>Danger</strong></h4><pre class="code">  In the above example, A&#39;s headers are likely to include headers from A&#39;s
  dependencies. Those dependencies may have public_configs that apply flags,
  defines, and include paths that make those headers work properly.

  With allow_circular_includes_from, B can include A&#39;s headers, and
  transitively from A&#39;s dependencies, without having the dependencies that
  would bring in the public_configs those headers need. The result may be
  errors or inconsistent builds.

  So when you use allow_circular_includes_from, make sure that any compiler
  settings, flags, and include directories are the same between both targets
  (consider putting such things in a shared config they can both reference).
  Make sure the dependencies are also the same (you might consider a group to
  collect such dependencies they both depend on).
</pre><h4><a class="h" name="Variables-you-set-in-targets-allow_circular_includes_from_Permit-includes-from-deps-Example" href="#Variables-you-set-in-targets-allow_circular_includes_from_Permit-includes-from-deps-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-allow_circular_includes_from_permit-includes-from-deps-example" href="#variables-you-set-in-targets-allow_circular_includes_from_permit-includes-from-deps-example"><span></span></a><strong>Example</strong></h4><pre class="code">  source_set(&quot;a&quot;) {
    deps = [ &quot;:b&quot;, &quot;:a_b_shared_deps&quot; ]
    allow_circular_includes_from = [ &quot;:b&quot; ]
    ...
  }

  source_set(&quot;b&quot;) {
    deps = [ &quot;:a_b_shared_deps&quot; ]
    # Sources here can include headers from a despite lack of deps.
    ...
  }

  group(&quot;a_b_shared_deps&quot;) {
    public_deps = [ &quot;:c&quot; ]
  }
</pre><h3><a class="h" name="arflags" href="#arflags"><span></span></a><strong>arflags</strong>: Arguments passed to static_library archiver.</h3><pre class="code">  A list of flags passed to the archive/lib command that creates static
  libraries.

  arflags are NOT pushed to dependents, so applying arflags to source sets or
  any other target type will be a no-op. As with ldflags, you could put the
  arflags in a config and set that as a public or &quot;all dependent&quot; config, but
  that will likely not be what you want. If you have a chain of static
  libraries dependent on each other, this can cause the flags to propagate up
  to other static libraries. Due to the nature of how arflags are typically
  used, you will normally want to apply them directly on static_library targets
  themselves.
</pre><h4><a class="h" name="Variables-you-set-in-targets-arflags_Arguments-passed-to-static_library-archiver-Ordering-of-flags-and-values" href="#Variables-you-set-in-targets-arflags_Arguments-passed-to-static_library-archiver-Ordering-of-flags-and-values"><span></span></a><a class="h" name="variables-you-set-in-targets-arflags_arguments-passed-to-static_library-archiver-ordering-of-flags-and-values" href="#variables-you-set-in-targets-arflags_arguments-passed-to-static_library-archiver-ordering-of-flags-and-values"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.
</pre><h3><a class="h" name="args-2" href="#args-2"><span></span></a><strong>args</strong>: Arguments passed to an action.</h3><pre class="code">  For action and action_foreach targets, args is the list of arguments to pass
  to the script. Typically you would use source expansion (see &quot;gn help
  source_expansion&quot;) to insert the source file names.

  See also &quot;gn help action&quot; and &quot;gn help action_foreach&quot;.
</pre><h3><a class="h" name="asmflags" href="#asmflags"><span></span></a><strong>asmflags</strong>: Flags passed to the assembler.</h3><pre class="code">  A list of strings.

  &quot;asmflags&quot; are passed to any invocation of a tool that takes an .asm or .S
  file as input.
</pre><h4><a class="h" name="Variables-you-set-in-targets-asmflags_Flags-passed-to-the-assembler-Ordering-of-flags-and-values" href="#Variables-you-set-in-targets-asmflags_Flags-passed-to-the-assembler-Ordering-of-flags-and-values"><span></span></a><a class="h" name="variables-you-set-in-targets-asmflags_flags-passed-to-the-assembler-ordering-of-flags-and-values" href="#variables-you-set-in-targets-asmflags_flags-passed-to-the-assembler-ordering-of-flags-and-values"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.
</pre><h3><a class="h" name="assert_no_deps" href="#assert_no_deps"><span></span></a><strong>assert_no_deps</strong>: Ensure no deps on these targets.</h3><pre class="code">  A list of label patterns.

  This list is a list of patterns that must not match any of the transitive
  dependencies of the target. These include all public, private, and data
  dependencies, and cross shared library boundaries. This allows you to express
  that undesirable code isn&#39;t accidentally added to downstream dependencies in
  a way that might otherwise be difficult to notice.

  Checking does not cross executable boundaries. If a target depends on an
  executable, it&#39;s assumed that the executable is a tool that is producing part
  of the build rather than something that is linked and distributed. This
  allows assert_no_deps to express what is distributed in the final target
  rather than depend on the internal build steps (which may include
  non-distributable code).

  See &quot;gn help label_pattern&quot; for the format of the entries in the list. These
  patterns allow blacklisting individual targets or whole directory
  hierarchies.

  Sometimes it is desirable to enforce that many targets have no dependencies
  on a target or set of targets. One efficient way to express this is to create
  a group with the assert_no_deps rule on it, and make that group depend on all
  targets you want to apply that assertion to.
</pre><h4><a class="h" name="Variables-you-set-in-targets-assert_no_deps_Ensure-no-deps-on-these-targets-Example" href="#Variables-you-set-in-targets-assert_no_deps_Ensure-no-deps-on-these-targets-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-assert_no_deps_ensure-no-deps-on-these-targets-example" href="#variables-you-set-in-targets-assert_no_deps_ensure-no-deps-on-these-targets-example"><span></span></a><strong>Example</strong></h4><pre class="code">  executable(&quot;doom_melon&quot;) {
    deps = [ &quot;//foo:bar&quot; ]
    ...
    assert_no_deps = [
      &quot;//evil/*&quot;,  # Don&#39;t link any code from the evil directory.
      &quot;//foo:test_support&quot;,  # This target is also disallowed.
    ]
  }
</pre><h3><a class="h" name="bundle_contents_dir" href="#bundle_contents_dir"><span></span></a><strong>bundle_contents_dir</strong>: Expansion of {{bundle_contents_dir}} in</h3><pre class="code">                             create_bundle.

  A string corresponding to a path in $root_build_dir.

  This string is used by the &quot;create_bundle&quot; target to expand the
  {{bundle_contents_dir}} of the &quot;bundle_data&quot; target it depends on. This must
  correspond to a path under &quot;bundle_root_dir&quot;.

  See &quot;gn help bundle_root_dir&quot; for examples.
</pre><h3><a class="h" name="bundle_deps_filter" href="#bundle_deps_filter"><span></span></a><strong>bundle_deps_filter</strong>: [label list] A list of labels that are filtered out.</h3><pre class="code">  A list of target labels.

  This list contains target label patterns that should be filtered out when
  creating the bundle. Any target matching one of those label will be removed
  from the dependencies of the create_bundle target.

  This is mostly useful when creating application extension bundle as the
  application extension has access to runtime resources from the application
  bundle and thus do not require a second copy.

  See &quot;gn help create_bundle&quot; for more information.
</pre><h4><a class="h" name="Variables-you-set-in-targets-bundle_deps_filter_label-list_A-list-of-labels-that-are-filtered-out-Example" href="#Variables-you-set-in-targets-bundle_deps_filter_label-list_A-list-of-labels-that-are-filtered-out-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-bundle_deps_filter_label-list_a-list-of-labels-that-are-filtered-out-example" href="#variables-you-set-in-targets-bundle_deps_filter_label-list_a-list-of-labels-that-are-filtered-out-example"><span></span></a><strong>Example</strong></h4><pre class="code">  create_bundle(&quot;today_extension&quot;) {
    deps = [
      &quot;//base&quot;
    ]
    bundle_root_dir = &quot;$root_out_dir/today_extension.appex&quot;
    bundle_deps_filter = [
      # The extension uses //base but does not use any function calling into
      # third_party/icu and thus does not need the icudtl.dat file.
      &quot;//third_party/icu:icudata&quot;,
    ]
  }
</pre><h3><a class="h" name="bundle_executable_dir" href="#bundle_executable_dir"><span></span></a><strong>bundle_executable_dir</strong>: Expansion of {{bundle_executable_dir}} in</h3><pre class="code">                              create_bundle.

  A string corresponding to a path in $root_build_dir.

  This string is used by the &quot;create_bundle&quot; target to expand the
  {{bundle_executable_dir}} of the &quot;bundle_data&quot; target it depends on. This
  must correspond to a path under &quot;bundle_root_dir&quot;.

  See &quot;gn help bundle_root_dir&quot; for examples.
</pre><h3><a class="h" name="bundle_plugins_dir" href="#bundle_plugins_dir"><span></span></a><strong>bundle_plugins_dir</strong>: Expansion of {{bundle_plugins_dir}} in create_bundle.</h3><pre class="code">  A string corresponding to a path in $root_build_dir.

  This string is used by the &quot;create_bundle&quot; target to expand the
  {{bundle_plugins_dir}} of the &quot;bundle_data&quot; target it depends on. This must
  correspond to a path under &quot;bundle_root_dir&quot;.

  See &quot;gn help bundle_root_dir&quot; for examples.
</pre><h3><a class="h" name="bundle_resources_dir" href="#bundle_resources_dir"><span></span></a><strong>bundle_resources_dir</strong>: Expansion of {{bundle_resources_dir}} in</h3><pre class="code">                             create_bundle.

  A string corresponding to a path in $root_build_dir.

  This string is used by the &quot;create_bundle&quot; target to expand the
  {{bundle_resources_dir}} of the &quot;bundle_data&quot; target it depends on. This must
  correspond to a path under &quot;bundle_root_dir&quot;.

  See &quot;gn help bundle_root_dir&quot; for examples.
</pre><h3><a class="h" name="bundle_root_dir" href="#bundle_root_dir"><span></span></a><strong>bundle_root_dir</strong>: Expansion of {{bundle_root_dir}} in create_bundle.</h3><pre class="code">  A string corresponding to a path in root_build_dir.

  This string is used by the &quot;create_bundle&quot; target to expand the
  {{bundle_root_dir}} of the &quot;bundle_data&quot; target it depends on. This must
  correspond to a path under root_build_dir.
</pre><h4><a class="h" name="Variables-you-set-in-targets-bundle_root_dir_Expansion-of-bundle_root_dir_in-create_bundle-Example" href="#Variables-you-set-in-targets-bundle_root_dir_Expansion-of-bundle_root_dir_in-create_bundle-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-bundle_root_dir_expansion-of-bundle_root_dir_in-create_bundle-example" href="#variables-you-set-in-targets-bundle_root_dir_expansion-of-bundle_root_dir_in-create_bundle-example"><span></span></a><strong>Example</strong></h4><pre class="code">  bundle_data(&quot;info_plist&quot;) {
    sources = [ &quot;Info.plist&quot; ]
    outputs = [ &quot;{{bundle_contents_dir}}/Info.plist&quot; ]
  }

  create_bundle(&quot;doom_melon.app&quot;) {
    deps = [ &quot;:info_plist&quot; ]
    bundle_root_dir = &quot;${root_build_dir}/doom_melon.app&quot;
    bundle_contents_dir = &quot;${bundle_root_dir}/Contents&quot;
    bundle_resources_dir = &quot;${bundle_contents_dir}/Resources&quot;
    bundle_executable_dir = &quot;${bundle_contents_dir}/MacOS&quot;
    bundle_plugins_dir = &quot;${bundle_contents_dir}/PlugIns&quot;
  }
</pre><h3><a class="h" name="cflags*-1" href="#cflags*-1"><span></span></a><strong>cflags</strong>*: Flags passed to the C compiler.</h3><pre class="code">  A list of strings.

  &quot;cflags&quot; are passed to all invocations of the C, C++, Objective C, and
  Objective C++ compilers.

  To target one of these variants individually, use &quot;cflags_c&quot;, &quot;cflags_cc&quot;,
  &quot;cflags_objc&quot;, and &quot;cflags_objcc&quot;, respectively. These variant-specific
  versions of cflags* will be appended on the compiler command line after
  &quot;cflags&quot;.

  See also &quot;asmflags&quot; for flags for assembly-language files.
</pre><h4><a class="h" name="Variables-you-set-in-targets-cflags_Flags-passed-to-the-C-compiler-Ordering-of-flags-and-values-1" href="#Variables-you-set-in-targets-cflags_Flags-passed-to-the-C-compiler-Ordering-of-flags-and-values-1"><span></span></a><a class="h" name="variables-you-set-in-targets-cflags_flags-passed-to-the-c-compiler-ordering-of-flags-and-values-1" href="#variables-you-set-in-targets-cflags_flags-passed-to-the-c-compiler-ordering-of-flags-and-values-1"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.
</pre><h3><a class="h" name="cflags*-2" href="#cflags*-2"><span></span></a><strong>cflags</strong>*: Flags passed to the C compiler.</h3><pre class="code">  A list of strings.

  &quot;cflags&quot; are passed to all invocations of the C, C++, Objective C, and
  Objective C++ compilers.

  To target one of these variants individually, use &quot;cflags_c&quot;, &quot;cflags_cc&quot;,
  &quot;cflags_objc&quot;, and &quot;cflags_objcc&quot;, respectively. These variant-specific
  versions of cflags* will be appended on the compiler command line after
  &quot;cflags&quot;.

  See also &quot;asmflags&quot; for flags for assembly-language files.
</pre><h4><a class="h" name="Variables-you-set-in-targets-cflags_Flags-passed-to-the-C-compiler-Ordering-of-flags-and-values-2" href="#Variables-you-set-in-targets-cflags_Flags-passed-to-the-C-compiler-Ordering-of-flags-and-values-2"><span></span></a><a class="h" name="variables-you-set-in-targets-cflags_flags-passed-to-the-c-compiler-ordering-of-flags-and-values-2" href="#variables-you-set-in-targets-cflags_flags-passed-to-the-c-compiler-ordering-of-flags-and-values-2"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.
</pre><h3><a class="h" name="cflags*-3" href="#cflags*-3"><span></span></a><strong>cflags</strong>*: Flags passed to the C compiler.</h3><pre class="code">  A list of strings.

  &quot;cflags&quot; are passed to all invocations of the C, C++, Objective C, and
  Objective C++ compilers.

  To target one of these variants individually, use &quot;cflags_c&quot;, &quot;cflags_cc&quot;,
  &quot;cflags_objc&quot;, and &quot;cflags_objcc&quot;, respectively. These variant-specific
  versions of cflags* will be appended on the compiler command line after
  &quot;cflags&quot;.

  See also &quot;asmflags&quot; for flags for assembly-language files.
</pre><h4><a class="h" name="Variables-you-set-in-targets-cflags_Flags-passed-to-the-C-compiler-Ordering-of-flags-and-values-3" href="#Variables-you-set-in-targets-cflags_Flags-passed-to-the-C-compiler-Ordering-of-flags-and-values-3"><span></span></a><a class="h" name="variables-you-set-in-targets-cflags_flags-passed-to-the-c-compiler-ordering-of-flags-and-values-3" href="#variables-you-set-in-targets-cflags_flags-passed-to-the-c-compiler-ordering-of-flags-and-values-3"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.
</pre><h3><a class="h" name="cflags*-4" href="#cflags*-4"><span></span></a><strong>cflags</strong>*: Flags passed to the C compiler.</h3><pre class="code">  A list of strings.

  &quot;cflags&quot; are passed to all invocations of the C, C++, Objective C, and
  Objective C++ compilers.

  To target one of these variants individually, use &quot;cflags_c&quot;, &quot;cflags_cc&quot;,
  &quot;cflags_objc&quot;, and &quot;cflags_objcc&quot;, respectively. These variant-specific
  versions of cflags* will be appended on the compiler command line after
  &quot;cflags&quot;.

  See also &quot;asmflags&quot; for flags for assembly-language files.
</pre><h4><a class="h" name="Variables-you-set-in-targets-cflags_Flags-passed-to-the-C-compiler-Ordering-of-flags-and-values-4" href="#Variables-you-set-in-targets-cflags_Flags-passed-to-the-C-compiler-Ordering-of-flags-and-values-4"><span></span></a><a class="h" name="variables-you-set-in-targets-cflags_flags-passed-to-the-c-compiler-ordering-of-flags-and-values-4" href="#variables-you-set-in-targets-cflags_flags-passed-to-the-c-compiler-ordering-of-flags-and-values-4"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.
</pre><h3><a class="h" name="cflags*-5" href="#cflags*-5"><span></span></a><strong>cflags</strong>*: Flags passed to the C compiler.</h3><pre class="code">  A list of strings.

  &quot;cflags&quot; are passed to all invocations of the C, C++, Objective C, and
  Objective C++ compilers.

  To target one of these variants individually, use &quot;cflags_c&quot;, &quot;cflags_cc&quot;,
  &quot;cflags_objc&quot;, and &quot;cflags_objcc&quot;, respectively. These variant-specific
  versions of cflags* will be appended on the compiler command line after
  &quot;cflags&quot;.

  See also &quot;asmflags&quot; for flags for assembly-language files.
</pre><h4><a class="h" name="Variables-you-set-in-targets-cflags_Flags-passed-to-the-C-compiler-Ordering-of-flags-and-values-5" href="#Variables-you-set-in-targets-cflags_Flags-passed-to-the-C-compiler-Ordering-of-flags-and-values-5"><span></span></a><a class="h" name="variables-you-set-in-targets-cflags_flags-passed-to-the-c-compiler-ordering-of-flags-and-values-5" href="#variables-you-set-in-targets-cflags_flags-passed-to-the-c-compiler-ordering-of-flags-and-values-5"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.
</pre><h3><a class="h" name="check_includes" href="#check_includes"><span></span></a><strong>check_includes</strong>: [boolean] Controls whether a target&#39;s files are checked.</h3><pre class="code">  When true (the default), the &quot;gn check&quot; command (as well as &quot;gn gen&quot; with the
  --check flag) will check this target&#39;s sources and headers for proper
  dependencies.

  When false, the files in this target will be skipped by default. This does
  not affect other targets that depend on the current target, it just skips
  checking the includes of the current target&#39;s files.

  If there are a few conditionally included headers that trip up checking, you
  can exclude headers individually by annotating them with &quot;nogncheck&quot; (see &quot;gn
  help nogncheck&quot;).

  The topic &quot;gn help check&quot; has general information on how checking works and
  advice on how to pass a check in problematic cases.
</pre><h4><a class="h" name="Variables-you-set-in-targets-check_includes_boolean_Controls-whether-a-target_s-files-are-checked-Example" href="#Variables-you-set-in-targets-check_includes_boolean_Controls-whether-a-target_s-files-are-checked-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-check_includes_boolean_controls-whether-a-target_s-files-are-checked-example" href="#variables-you-set-in-targets-check_includes_boolean_controls-whether-a-target_s-files-are-checked-example"><span></span></a><strong>Example</strong></h4><pre class="code">  source_set(&quot;busted_includes&quot;) {
    # This target&#39;s includes are messed up, exclude it from checking.
    check_includes = false
    ...
  }
</pre><h3><a class="h" name="code_signing_args" href="#code_signing_args"><span></span></a><strong>code_signing_args</strong>: [string list] Arguments passed to code signing script.</h3><pre class="code">  For create_bundle targets, code_signing_args is the list of arguments to pass
  to the code signing script. Typically you would use source expansion (see &quot;gn
  help source_expansion&quot;) to insert the source file names.

  See also &quot;gn help create_bundle&quot;.
</pre><h3><a class="h" name="code_signing_outputs" href="#code_signing_outputs"><span></span></a><strong>code_signing_outputs</strong>: [file list] Output files for code signing step.</h3><pre class="code">  Outputs from the code signing step of a create_bundle target. Must refer to
  files in the build directory.

  See also &quot;gn help create_bundle&quot;.
</pre><h3><a class="h" name="code_signing_script" href="#code_signing_script"><span></span></a><strong>code_signing_script</strong>: [file name] Script for code signing.&quot;</h3><pre class="code">  An absolute or buildfile-relative file name of a Python script to run for a
  create_bundle target to perform code signing step.

  See also &quot;gn help create_bundle&quot;.
</pre><h3><a class="h" name="code_signing_sources" href="#code_signing_sources"><span></span></a><strong>code_signing_sources</strong>: [file list] Sources for code signing step.</h3><pre class="code">  A list of files used as input for code signing script step of a create_bundle
  target. Non-absolute paths will be resolved relative to the current build
  file.

  See also &quot;gn help create_bundle&quot;.
</pre><h3><a class="h" name="complete_static_lib" href="#complete_static_lib"><span></span></a><strong>complete_static_lib</strong>: [boolean] Links all deps into a static library.</h3><pre class="code">  A static library normally doesn&#39;t include code from dependencies, but instead
  forwards the static libraries and source sets in its deps up the dependency
  chain until a linkable target (an executable or shared library) is reached.
  The final linkable target only links each static library once, even if it
  appears more than once in its dependency graph.

  In some cases the static library might be the final desired output. For
  example, you may be producing a static library for distribution to third
  parties. In this case, the static library should include code for all
  dependencies in one complete package. However, complete static libraries
  themselves are never linked into other complete static libraries. All
  complete static libraries are for distribution and linking them in would
  cause code duplication in this case. If the static library is not for
  distribution, it should not be complete.

  GN treats non-complete static libraries as source sets when they are linked
  into complete static libraries. This is done because some tools like AR do
  not handle dependent static libraries properly. This makes it easier to write
  &quot;alink&quot; rules.

  In rare cases it makes sense to list a header in more than one target if it
  could be considered conceptually a member of both. libraries.
</pre><h4><a class="h" name="Variables-you-set-in-targets-complete_static_lib_boolean_Links-all-deps-into-a-static-library-Example" href="#Variables-you-set-in-targets-complete_static_lib_boolean_Links-all-deps-into-a-static-library-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-complete_static_lib_boolean_links-all-deps-into-a-static-library-example" href="#variables-you-set-in-targets-complete_static_lib_boolean_links-all-deps-into-a-static-library-example"><span></span></a><strong>Example</strong></h4><pre class="code">  static_library(&quot;foo&quot;) {
    complete_static_lib = true
    deps = [ &quot;bar&quot; ]
  }
</pre><h3><a class="h" name="configs" href="#configs"><span></span></a><strong>configs</strong>: Configs applying to this target or config.</h3><pre class="code">  A list of config labels.
</pre><h4><a class="h" name="Configs-on-a-target" href="#Configs-on-a-target"><span></span></a><a class="h" name="configs-on-a-target" href="#configs-on-a-target"><span></span></a><strong>Configs on a target</strong></h4><pre class="code">  When used on a target, the include_dirs, defines, etc. in each config are
  appended in the order they appear to the compile command for each file in the
  target. They will appear after the include_dirs, defines, etc. that the
  target sets directly.

  Since configs apply after the values set on a target, directly setting a
  compiler flag will prepend it to the command line. If you want to append a
  flag instead, you can put that flag in a one-off config and append that
  config to the target&#39;s configs list.

  The build configuration script will generally set up the default configs
  applying to a given target type (see &quot;set_defaults&quot;). When a target is being
  defined, it can add to or remove from this list.
</pre><h4><a class="h" name="Configs-on-a-config" href="#Configs-on-a-config"><span></span></a><a class="h" name="configs-on-a-config" href="#configs-on-a-config"><span></span></a><strong>Configs on a config</strong></h4><pre class="code">  It is possible to create composite configs by specifying configs on a config.
  One might do this to forward values, or to factor out blocks of settings from
  very large configs into more manageable named chunks.

  In this case, the composite config is expanded to be the concatenation of its
  own values, and in order, the values from its sub-configs *before* anything
  else happens. This has some ramifications:

   - A target has no visibility into a config&#39;s sub-configs. Target code only
     sees the name of the composite config. It can&#39;t remove sub-configs or opt
     in to only parts of it. The composite config may not even be defined
     before the target is.

   - You can get duplication of values if a config is listed twice, say, on a
     target and in a sub-config that also applies. In other cases, the configs
     applying to a target are de-duped. It&#39;s expected that if a config is
     listed as a sub-config that it is only used in that context. (Note that
     it&#39;s possible to fix this and de-dupe, but it&#39;s not normally relevant and
     complicates the implementation.)
</pre><h4><a class="h" name="Variables-you-set-in-targets-configs_Configs-applying-to-this-target-or-config-Ordering-of-flags-and-values" href="#Variables-you-set-in-targets-configs_Configs-applying-to-this-target-or-config-Ordering-of-flags-and-values"><span></span></a><a class="h" name="variables-you-set-in-targets-configs_configs-applying-to-this-target-or-config-ordering-of-flags-and-values" href="#variables-you-set-in-targets-configs_configs-applying-to-this-target-or-config-ordering-of-flags-and-values"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.
</pre><h4><a class="h" name="Variables-you-set-in-targets-configs_Configs-applying-to-this-target-or-config-Example" href="#Variables-you-set-in-targets-configs_Configs-applying-to-this-target-or-config-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-configs_configs-applying-to-this-target-or-config-example" href="#variables-you-set-in-targets-configs_configs-applying-to-this-target-or-config-example"><span></span></a><strong>Example</strong></h4><pre class="code">  # Configs on a target.
  source_set(&quot;foo&quot;) {
    # Don&#39;t use the default RTTI config that BUILDCONFIG applied to us.
    configs -= [ &quot;//build:no_rtti&quot; ]

    # Add some of our own settings.
    configs += [ &quot;:mysettings&quot; ]
  }

  # Create a default_optimization config that forwards to one of a set of more
  # specialized configs depending on build flags. This pattern is useful
  # because it allows a target to opt in to either a default set, or a more
  # specific set, while avoid duplicating the settings in two places.
  config(&quot;super_optimization&quot;) {
    cflags = [ ... ]
  }
  config(&quot;default_optimization&quot;) {
    if (optimize_everything) {
      configs = [ &quot;:super_optimization&quot; ]
    } else {
      configs = [ &quot;:no_optimization&quot; ]
    }
  }
</pre><h3><a class="h" name="data" href="#data"><span></span></a><strong>data</strong>: Runtime data file dependencies.</h3><pre class="code">  Lists files or directories required to run the given target. These are
  typically data files or directories of data files. The paths are interpreted
  as being relative to the current build file. Since these are runtime
  dependencies, they do not affect which targets are built or when. To declare
  input files to a script, use &quot;inputs&quot;.

  Appearing in the &quot;data&quot; section does not imply any special handling such as
  copying them to the output directory. This is just used for declaring runtime
  dependencies. Runtime dependencies can be queried using the &quot;runtime_deps&quot;
  category of &quot;gn desc&quot; or written during build generation via
  &quot;--runtime-deps-list-file&quot;.

  GN doesn&#39;t require data files to exist at build-time. So actions that produce
  files that are in turn runtime dependencies can list those generated files
  both in the &quot;outputs&quot; list as well as the &quot;data&quot; list.

  By convention, directories are listed with a trailing slash:
    data = [ &quot;test/data/&quot; ]
  However, no verification is done on these so GN doesn&#39;t enforce this. The
  paths are just rebased and passed along when requested.

  Note: On iOS and macOS, create_bundle targets will not be recursed into when
  gathering data. See &quot;gn help create_bundle&quot; for details.

  See &quot;gn help runtime_deps&quot; for how these are used.
</pre><h3><a class="h" name="data_deps" href="#data_deps"><span></span></a><strong>data_deps</strong>: Non-linked dependencies.</h3><pre class="code">  A list of target labels.

  Specifies dependencies of a target that are not actually linked into the
  current target. Such dependencies will be built and will be available at
  runtime.

  This is normally used for things like plugins or helper programs that a
  target needs at runtime.

  Note: On iOS and macOS, create_bundle targets will not be recursed into when
  gathering data_deps. See &quot;gn help create_bundle&quot; for details.

  See also &quot;gn help deps&quot; and &quot;gn help data&quot;.
</pre><h4><a class="h" name="Variables-you-set-in-targets-data_deps_Non_linked-dependencies-Example" href="#Variables-you-set-in-targets-data_deps_Non_linked-dependencies-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-data_deps_non_linked-dependencies-example" href="#variables-you-set-in-targets-data_deps_non_linked-dependencies-example"><span></span></a><strong>Example</strong></h4><pre class="code">  executable(&quot;foo&quot;) {
    deps = [ &quot;//base&quot; ]
    data_deps = [ &quot;//plugins:my_runtime_plugin&quot; ]
  }
</pre><h3><a class="h" name="defines" href="#defines"><span></span></a><strong>defines</strong>: C preprocessor defines.</h3><pre class="code">  A list of strings

  These strings will be passed to the C/C++ compiler as #defines. The strings
  may or may not include an &quot;=&quot; to assign a value.
</pre><h4><a class="h" name="Variables-you-set-in-targets-defines_C-preprocessor-defines-Ordering-of-flags-and-values" href="#Variables-you-set-in-targets-defines_C-preprocessor-defines-Ordering-of-flags-and-values"><span></span></a><a class="h" name="variables-you-set-in-targets-defines_c-preprocessor-defines-ordering-of-flags-and-values" href="#variables-you-set-in-targets-defines_c-preprocessor-defines-ordering-of-flags-and-values"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.
</pre><h4><a class="h" name="Variables-you-set-in-targets-defines_C-preprocessor-defines-Example" href="#Variables-you-set-in-targets-defines_C-preprocessor-defines-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-defines_c-preprocessor-defines-example" href="#variables-you-set-in-targets-defines_c-preprocessor-defines-example"><span></span></a><strong>Example</strong></h4><pre class="code">  defines = [ &quot;AWESOME_FEATURE&quot;, &quot;LOG_LEVEL=3&quot; ]
</pre><h3><a class="h" name="depfile" href="#depfile"><span></span></a><strong>depfile</strong>: [string] File name for input dependencies for actions.</h3><pre class="code">  If nonempty, this string specifies that the current action or action_foreach
  target will generate the given &quot;.d&quot; file containing the dependencies of the
  input. Empty or unset means that the script doesn&#39;t generate the files.

  A depfile should be used only when a target depends on files that are not
  already specified by a target&#39;s inputs and sources. Likewise, depfiles should
  specify only those dependencies not already included in sources or inputs.

  The .d file should go in the target output directory. If you have more than
  one source file that the script is being run over, you can use the output
  file expansions described in &quot;gn help action_foreach&quot; to name the .d file
  according to the input.&quot;

  The format is that of a Makefile and all paths must be relative to the root
  build directory. Only one output may be listed and it must match the first
  output of the action.

  Although depfiles are created by an action, they should not be listed in the
  action&#39;s &quot;outputs&quot; unless another target will use the file as an input.
</pre><h4><a class="h" name="Variables-you-set-in-targets-depfile_string_File-name-for-input-dependencies-for-actions-Example" href="#Variables-you-set-in-targets-depfile_string_File-name-for-input-dependencies-for-actions-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-depfile_string_file-name-for-input-dependencies-for-actions-example" href="#variables-you-set-in-targets-depfile_string_file-name-for-input-dependencies-for-actions-example"><span></span></a><strong>Example</strong></h4><pre class="code">  action_foreach(&quot;myscript_target&quot;) {
    script = &quot;myscript.py&quot;
    sources = [ ... ]

    # Locate the depfile in the output directory named like the
    # inputs but with a &quot;.d&quot; appended.
    depfile = &quot;$relative_target_output_dir/{{source_name}}.d&quot;

    # Say our script uses &quot;-o &lt;d file&gt;&quot; to indicate the depfile.
    args = [ &quot;{{source}}&quot;, &quot;-o&quot;, depfile ]
  }
</pre><h3><a class="h" name="deps" href="#deps"><span></span></a><strong>deps</strong>: Private linked dependencies.</h3><pre class="code">  A list of target labels.

  Specifies private dependencies of a target. Private dependencies are
  propagated up the dependency tree and linked to dependant targets, but do not
  grant the ability to include headers from the dependency. Public configs are
  not forwarded.
</pre><h4><a class="h" name="Details-of-dependency-propagation" href="#Details-of-dependency-propagation"><span></span></a><a class="h" name="details-of-dependency-propagation" href="#details-of-dependency-propagation"><span></span></a><strong>Details of dependency propagation</strong></h4><pre class="code">  Source sets, shared libraries, and non-complete static libraries will be
  propagated up the dependency tree across groups, non-complete static
  libraries and source sets.

  Executables, shared libraries, and complete static libraries will link all
  propagated targets and stop propagation. Actions and copy steps also stop
  propagation, allowing them to take a library as an input but not force
  dependants to link to it.

  Propagation of all_dependent_configs and public_configs happens independently
  of target type. all_dependent_configs are always propagated across all types
  of targets, and public_configs are always propagated across public deps of
  all types of targets.

  Data dependencies are propagated differently. See &quot;gn help data_deps&quot; and
  &quot;gn help runtime_deps&quot;.

  See also &quot;public_deps&quot;.
</pre><h3><a class="h" name="include_dirs" href="#include_dirs"><span></span></a><strong>include_dirs</strong>: Additional include directories.</h3><pre class="code">  A list of source directories.

  The directories in this list will be added to the include path for the files
  in the affected target.
</pre><h4><a class="h" name="Variables-you-set-in-targets-include_dirs_Additional-include-directories-Ordering-of-flags-and-values" href="#Variables-you-set-in-targets-include_dirs_Additional-include-directories-Ordering-of-flags-and-values"><span></span></a><a class="h" name="variables-you-set-in-targets-include_dirs_additional-include-directories-ordering-of-flags-and-values" href="#variables-you-set-in-targets-include_dirs_additional-include-directories-ordering-of-flags-and-values"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.
</pre><h4><a class="h" name="Variables-you-set-in-targets-include_dirs_Additional-include-directories-Example" href="#Variables-you-set-in-targets-include_dirs_Additional-include-directories-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-include_dirs_additional-include-directories-example" href="#variables-you-set-in-targets-include_dirs_additional-include-directories-example"><span></span></a><strong>Example</strong></h4><pre class="code">  include_dirs = [ &quot;src/include&quot;, &quot;//third_party/foo&quot; ]
</pre><h3><a class="h" name="inputs" href="#inputs"><span></span></a><strong>inputs</strong>: Additional compile-time dependencies.</h3><pre class="code">  Inputs are compile-time dependencies of the current target. This means that
  all inputs must be available before compiling any of the sources or executing
  any actions.

  Inputs are typically only used for action and action_foreach targets.
</pre><h4><a class="h" name="Inputs-for-actions" href="#Inputs-for-actions"><span></span></a><a class="h" name="inputs-for-actions" href="#inputs-for-actions"><span></span></a><strong>Inputs for actions</strong></h4><pre class="code">  For action and action_foreach targets, inputs should be the inputs to script
  that don&#39;t vary. These should be all .py files that the script uses via
  imports (the main script itself will be an implicit dependency of the action
  so need not be listed).

  For action targets, inputs and sources are treated the same, but from a style
  perspective, it&#39;s recommended to follow the same rule as action_foreach and
  put helper files in the inputs, and the data used by the script (if any) in
  sources.

  Note that another way to declare input dependencies from an action is to have
  the action write a depfile (see &quot;gn help depfile&quot;). This allows the script to
  dynamically write input dependencies, that might not be known until actually
  executing the script. This is more efficient than doing processing while
  running GN to determine the inputs, and is easier to keep in-sync than
  hardcoding the list.
</pre><h4><a class="h" name="Script-input-gotchas" href="#Script-input-gotchas"><span></span></a><a class="h" name="script-input-gotchas" href="#script-input-gotchas"><span></span></a><strong>Script input gotchas</strong></h4><pre class="code">  It may be tempting to write a script that enumerates all files in a directory
  as inputs. Don&#39;t do this! Even if you specify all the files in the inputs or
  sources in the GN target (or worse, enumerate the files in an exec_script
  call when running GN, which will be slow), the dependencies will be broken.

  The problem happens if a file is ever removed because the inputs are not
  listed on the command line to the script. Because the script hasn&#39;t changed
  and all inputs are up to date, the script will not re-run and you will get a
  stale build. Instead, either list all inputs on the command line to the
  script, or if there are many, create a separate list file that the script
  reads. As long as this file is listed in the inputs, the build will detect
  when it has changed in any way and the action will re-run.
</pre><h4><a class="h" name="Inputs-for-binary-targets" href="#Inputs-for-binary-targets"><span></span></a><a class="h" name="inputs-for-binary-targets" href="#inputs-for-binary-targets"><span></span></a><strong>Inputs for binary targets</strong></h4><pre class="code">  Any input dependencies will be resolved before compiling any sources.
  Normally, all actions that a target depends on will be run before any files
  in a target are compiled. So if you depend on generated headers, you do not
  typically need to list them in the inputs section.

  Inputs for binary targets will be treated as implicit dependencies, meaning
  that changes in any of the inputs will force all sources in the target to be
  recompiled. If an input only applies to a subset of source files, you may
  want to split those into a separate target to avoid unnecessary recompiles.
</pre><h4><a class="h" name="Variables-you-set-in-targets-inputs_Additional-compile_time-dependencies-Example" href="#Variables-you-set-in-targets-inputs_Additional-compile_time-dependencies-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-inputs_additional-compile_time-dependencies-example" href="#variables-you-set-in-targets-inputs_additional-compile_time-dependencies-example"><span></span></a><strong>Example</strong></h4><pre class="code">  action(&quot;myscript&quot;) {
    script = &quot;domything.py&quot;
    inputs = [ &quot;input.data&quot; ]
  }
</pre><h3><a class="h" name="ldflags" href="#ldflags"><span></span></a><strong>ldflags</strong>: Flags passed to the linker.</h3><pre class="code">  A list of strings.

  These flags are passed on the command-line to the linker and generally
  specify various linking options. Most targets will not need these and will
  use &quot;libs&quot; and &quot;lib_dirs&quot; instead.

  ldflags are NOT pushed to dependents, so applying ldflags to source sets or
  static libraries will be a no-op. If you want to apply ldflags to dependent
  targets, put them in a config and set it in the all_dependent_configs or
  public_configs.
</pre><h4><a class="h" name="Variables-you-set-in-targets-ldflags_Flags-passed-to-the-linker-Ordering-of-flags-and-values" href="#Variables-you-set-in-targets-ldflags_Flags-passed-to-the-linker-Ordering-of-flags-and-values"><span></span></a><a class="h" name="variables-you-set-in-targets-ldflags_flags-passed-to-the-linker-ordering-of-flags-and-values" href="#variables-you-set-in-targets-ldflags_flags-passed-to-the-linker-ordering-of-flags-and-values"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.
</pre><h3><a class="h" name="lib_dirs" href="#lib_dirs"><span></span></a><strong>lib_dirs</strong>: Additional library directories.</h3><pre class="code">  A list of directories.

  Specifies additional directories passed to the linker for searching for the
  required libraries. If an item is not an absolute path, it will be treated as
  being relative to the current build file.

  libs and lib_dirs work differently than other flags in two respects.
  First, then are inherited across static library boundaries until a
  shared library or executable target is reached. Second, they are
  uniquified so each one is only passed once (the first instance of it
  will be the one used).
</pre><h4><a class="h" name="Variables-you-set-in-targets-lib_dirs_Additional-library-directories-Ordering-of-flags-and-values" href="#Variables-you-set-in-targets-lib_dirs_Additional-library-directories-Ordering-of-flags-and-values"><span></span></a><a class="h" name="variables-you-set-in-targets-lib_dirs_additional-library-directories-ordering-of-flags-and-values" href="#variables-you-set-in-targets-lib_dirs_additional-library-directories-ordering-of-flags-and-values"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.

  For &quot;libs&quot; and &quot;lib_dirs&quot; only, the values propagated from
  dependencies (as described above) are applied last assuming they
  are not already in the list.
</pre><h4><a class="h" name="Variables-you-set-in-targets-lib_dirs_Additional-library-directories-Example" href="#Variables-you-set-in-targets-lib_dirs_Additional-library-directories-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-lib_dirs_additional-library-directories-example" href="#variables-you-set-in-targets-lib_dirs_additional-library-directories-example"><span></span></a><strong>Example</strong></h4><pre class="code">  lib_dirs = [ &quot;/usr/lib/foo&quot;, &quot;lib/doom_melon&quot; ]
</pre><h3><a class="h" name="libs" href="#libs"><span></span></a><strong>libs</strong>: Additional libraries to link.</h3><pre class="code">  A list of library names or library paths.

  These libraries will be linked into the final binary (executable or shared
  library) containing the current target.

  libs and lib_dirs work differently than other flags in two respects.
  First, then are inherited across static library boundaries until a
  shared library or executable target is reached. Second, they are
  uniquified so each one is only passed once (the first instance of it
  will be the one used).
</pre><h4><a class="h" name="Types-of-libs" href="#Types-of-libs"><span></span></a><a class="h" name="types-of-libs" href="#types-of-libs"><span></span></a><strong>Types of libs</strong></h4><pre class="code">  There are several different things that can be expressed in libs:

  File paths
      Values containing &#39;/&#39; will be treated as references to files in the
      checkout. They will be rebased to be relative to the build directory and
      specified in the &quot;libs&quot; for linker tools. This facility should be used
      for libraries that are checked in to the version control. For libraries
      that are generated by the build, use normal GN deps to link them.

  System libraries
      Values not containing &#39;/&#39; will be treated as system library names. These
      will be passed unmodified to the linker and prefixed with the
      &quot;lib_prefix&quot; attribute of the linker tool. Generally you would set the
      &quot;lib_dirs&quot; so the given library is found. Your BUILD.gn file should not
      specify the switch (like &quot;-l&quot;): this will be encoded in the &quot;lib_prefix&quot;
      of the tool.

  Apple frameworks
      System libraries ending in &quot;.framework&quot; will be special-cased: the switch
      &quot;-framework&quot; will be prepended instead of the lib_prefix, and the
      &quot;.framework&quot; suffix will be trimmed. This is to support the way Mac links
      framework dependencies.
</pre><h4><a class="h" name="Variables-you-set-in-targets-libs_Additional-libraries-to-link-Ordering-of-flags-and-values" href="#Variables-you-set-in-targets-libs_Additional-libraries-to-link-Ordering-of-flags-and-values"><span></span></a><a class="h" name="variables-you-set-in-targets-libs_additional-libraries-to-link-ordering-of-flags-and-values" href="#variables-you-set-in-targets-libs_additional-libraries-to-link-ordering-of-flags-and-values"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.

  For &quot;libs&quot; and &quot;lib_dirs&quot; only, the values propagated from
  dependencies (as described above) are applied last assuming they
  are not already in the list.
</pre><h4><a class="h" name="Variables-you-set-in-targets-libs_Additional-libraries-to-link-Examples" href="#Variables-you-set-in-targets-libs_Additional-libraries-to-link-Examples"><span></span></a><a class="h" name="variables-you-set-in-targets-libs_additional-libraries-to-link-examples" href="#variables-you-set-in-targets-libs_additional-libraries-to-link-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  On Windows:
    libs = [ &quot;ctl3d.lib&quot; ]

  On Linux:
    libs = [ &quot;ld&quot; ]
</pre><h3><a class="h" name="output_dir" href="#output_dir"><span></span></a><strong>output_dir</strong>: [directory] Directory to put output file in.</h3><pre class="code">  For library and executable targets, overrides the directory for the final
  output. This must be in the root_build_dir or a child thereof.

  This should generally be in the root_out_dir or a subdirectory thereof (the
  root_out_dir will be the same as the root_build_dir for the default
  toolchain, and will be a subdirectory for other toolchains). Not putting the
  output in a subdirectory of root_out_dir can result in collisions between
  different toolchains, so you will need to take steps to ensure that your
  target is only present in one toolchain.

  Normally the toolchain specifies the output directory for libraries and
  executables (see &quot;gn help tool&quot;). You will have to consult that for the
  default location. The default location will be used if output_dir is
  undefined or empty.
</pre><h4><a class="h" name="Variables-you-set-in-targets-output_dir_directory_Directory-to-put-output-file-in-Example" href="#Variables-you-set-in-targets-output_dir_directory_Directory-to-put-output-file-in-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-output_dir_directory_directory-to-put-output-file-in-example" href="#variables-you-set-in-targets-output_dir_directory_directory-to-put-output-file-in-example"><span></span></a><strong>Example</strong></h4><pre class="code">  shared_library(&quot;doom_melon&quot;) {
    output_dir = &quot;$root_out_dir/plugin_libs&quot;
    ...
  }
</pre><h3><a class="h" name="output_extension" href="#output_extension"><span></span></a><strong>output_extension</strong>: Value to use for the output&#39;s file extension.</h3><pre class="code">  Normally the file extension for a target is based on the target type and the
  operating system, but in rare cases you will need to override the name (for
  example to use &quot;libfreetype.so.6&quot; instead of libfreetype.so on Linux).

  This value should not include a leading dot. If undefined, the default
  specified on the tool will be used. If set to the empty string, no output
  extension will be used.

  The output_extension will be used to set the &quot;{{output_extension}}&quot; expansion
  which the linker tool will generally use to specify the output file name. See
  &quot;gn help tool&quot;.
</pre><h4><a class="h" name="Variables-you-set-in-targets-output_extension_Value-to-use-for-the-output_s-file-extension-Example" href="#Variables-you-set-in-targets-output_extension_Value-to-use-for-the-output_s-file-extension-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-output_extension_value-to-use-for-the-output_s-file-extension-example" href="#variables-you-set-in-targets-output_extension_value-to-use-for-the-output_s-file-extension-example"><span></span></a><strong>Example</strong></h4><pre class="code">  shared_library(&quot;freetype&quot;) {
    if (is_linux) {
      # Call the output &quot;libfreetype.so.6&quot;
      output_extension = &quot;so.6&quot;
    }
    ...
  }

  # On Windows, generate a &quot;mysettings.cpl&quot; control panel applet. Control panel
  # applets are actually special shared libraries.
  if (is_win) {
    shared_library(&quot;mysettings&quot;) {
      output_extension = &quot;cpl&quot;
      ...
    }
  }
</pre><h3><a class="h" name="output_name" href="#output_name"><span></span></a><strong>output_name</strong>: Define a name for the output file other than the default.</h3><pre class="code">  Normally the output name of a target will be based on the target name, so the
  target &quot;//foo/bar:bar_unittests&quot; will generate an output file such as
  &quot;bar_unittests.exe&quot; (using Windows as an example).

  Sometimes you will want an alternate name to avoid collisions or if the
  internal name isn&#39;t appropriate for public distribution.

  The output name should have no extension or prefixes, these will be added
  using the default system rules. For example, on Linux an output name of &quot;foo&quot;
  will produce a shared library &quot;libfoo.so&quot;. There is no way to override the
  output prefix of a linker tool on a per- target basis. If you need more
  flexibility, create a copy target to produce the file you want.

  This variable is valid for all binary output target types.
</pre><h4><a class="h" name="Variables-you-set-in-targets-output_name_Define-a-name-for-the-output-file-other-than-the-default-Example" href="#Variables-you-set-in-targets-output_name_Define-a-name-for-the-output-file-other-than-the-default-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-output_name_define-a-name-for-the-output-file-other-than-the-default-example" href="#variables-you-set-in-targets-output_name_define-a-name-for-the-output-file-other-than-the-default-example"><span></span></a><strong>Example</strong></h4><pre class="code">  static_library(&quot;doom_melon&quot;) {
    output_name = &quot;fluffy_bunny&quot;
  }
</pre><h3><a class="h" name="output_prefix_override" href="#output_prefix_override"><span></span></a><strong>output_prefix_override</strong>: Don&#39;t use prefix for output name.</h3><pre class="code">  A boolean that overrides the output prefix for a target. Defaults to false.

  Some systems use prefixes for the names of the final target output file. The
  normal example is &quot;libfoo.so&quot; on Linux for a target named &quot;foo&quot;.

  The output prefix for a given target type is specified on the linker tool
  (see &quot;gn help tool&quot;). Sometimes this prefix is undesired.

  See also &quot;gn help output_extension&quot;.
</pre><h4><a class="h" name="Variables-you-set-in-targets-output_prefix_override_Don_t-use-prefix-for-output-name-Example" href="#Variables-you-set-in-targets-output_prefix_override_Don_t-use-prefix-for-output-name-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-output_prefix_override_don_t-use-prefix-for-output-name-example" href="#variables-you-set-in-targets-output_prefix_override_don_t-use-prefix-for-output-name-example"><span></span></a><strong>Example</strong></h4><pre class="code">  shared_library(&quot;doom_melon&quot;) {
    # Normally this will produce &quot;libdoom_melon.so&quot; on Linux. Setting this flag
    # will produce &quot;doom_melon.so&quot;.
    output_prefix_override = true
    ...
  }
</pre><h3><a class="h" name="outputs" href="#outputs"><span></span></a><strong>outputs</strong>: Output files for actions and copy targets.</h3><pre class="code">  Outputs is valid for &quot;copy&quot;, &quot;action&quot;, and &quot;action_foreach&quot; target types and
  indicates the resulting files. Outputs must always refer to files in the
  build directory.

  copy
    Copy targets should have exactly one entry in the outputs list. If there is
    exactly one source, this can be a literal file name or a source expansion.
    If there is more than one source, this must contain a source expansion to
    map a single input name to a single output name. See &quot;gn help copy&quot;.

  action_foreach
    Action_foreach targets must always use source expansions to map input files
    to output files. There can be more than one output, which means that each
    invocation of the script will produce a set of files (presumably based on
    the name of the input file). See &quot;gn help action_foreach&quot;.

  action
    Action targets (excluding action_foreach) must list literal output file(s)
    with no source expansions. See &quot;gn help action&quot;.
</pre><h3><a class="h" name="partial_info_plist" href="#partial_info_plist"><span></span></a><strong>partial_info_plist</strong>: [filename] Path plist from asset catalog compiler.</h3><pre class="code">  Valid for create_bundle target, corresponds to the path for the partial
  Info.plist created by the asset catalog compiler that needs to be merged
  with the application Info.plist (usually done by the code signing script).

  The file will be generated regardless of whether the asset compiler has
  been invoked or not. See &quot;gn help create_bundle&quot;.
</pre><h3><a class="h" name="pool-2" href="#pool-2"><span></span></a><strong>pool</strong>: Label of the pool used by the action.</h3><pre class="code">  A fully-qualified label representing the pool that will be used for the
  action. Pools are defined using the pool() {...} declaration.
</pre><h4><a class="h" name="Variables-you-set-in-targets-pool_Label-of-the-pool-used-by-the-action-Example" href="#Variables-you-set-in-targets-pool_Label-of-the-pool-used-by-the-action-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-pool_label-of-the-pool-used-by-the-action-example" href="#variables-you-set-in-targets-pool_label-of-the-pool-used-by-the-action-example"><span></span></a><strong>Example</strong></h4><pre class="code">  action(&quot;action&quot;) {
    pool = &quot;//build:custom_pool&quot;
    ...
  }
</pre><h3><a class="h" name="precompiled_header" href="#precompiled_header"><span></span></a><strong>precompiled_header</strong>: [string] Header file to precompile.</h3><pre class="code">  Precompiled headers will be used when a target specifies this value, or a
  config applying to this target specifies this value. In addition, the tool
  corresponding to the source files must also specify precompiled headers (see
  &quot;gn help tool&quot;). The tool will also specify what type of precompiled headers
  to use, by setting precompiled_header_type to either &quot;gcc&quot; or &quot;msvc&quot;.

  The precompiled header/source variables can be specified on a target or a
  config, but must be the same for all configs applying to a given target since
  a target can only have one precompiled header.

  If you use both C and C++ sources, the precompiled header and source file
  will be compiled once per language. You will want to make sure to wrap C++
  includes in __cplusplus #ifdefs so the file will compile in C mode.
</pre><h4><a class="h" name="GCC-precompiled-headers" href="#GCC-precompiled-headers"><span></span></a><a class="h" name="gcc-precompiled-headers" href="#gcc-precompiled-headers"><span></span></a><strong>GCC precompiled headers</strong></h4><pre class="code">  When using GCC-style precompiled headers, &quot;precompiled_source&quot; contains the
  path of a .h file that is precompiled and then included by all source files
  in targets that set &quot;precompiled_source&quot;.

  The value of &quot;precompiled_header&quot; is not used with GCC-style precompiled
  headers.
</pre><h4><a class="h" name="MSVC-precompiled-headers" href="#MSVC-precompiled-headers"><span></span></a><a class="h" name="msvc-precompiled-headers" href="#msvc-precompiled-headers"><span></span></a><strong>MSVC precompiled headers</strong></h4><pre class="code">  When using MSVC-style precompiled headers, the &quot;precompiled_header&quot; value is
  a string corresponding to the header. This is NOT a path to a file that GN
  recognises, but rather the exact string that appears in quotes after
  an #include line in source code. The compiler will match this string against
  includes or forced includes (/FI).

  MSVC also requires a source file to compile the header with. This must be
  specified by the &quot;precompiled_source&quot; value. In contrast to the header value,
  this IS a GN-style file name, and tells GN which source file to compile to
  make the .pch file used for subsequent compiles.

  For example, if the toolchain specifies MSVC headers:

    toolchain(&quot;vc_x64&quot;) {
      ...
      tool(&quot;cxx&quot;) {
        precompiled_header_type = &quot;msvc&quot;
        ...

  You might make a config like this:

    config(&quot;use_precompiled_headers&quot;) {
      precompiled_header = &quot;build/precompile.h&quot;
      precompiled_source = &quot;//build/precompile.cc&quot;

      # Either your source files should #include &quot;build/precompile.h&quot;
      # first, or you can do this to force-include the header.
      cflags = [ &quot;/FI$precompiled_header&quot; ]
    }

  And then define a target that uses the config:

    executable(&quot;doom_melon&quot;) {
      configs += [ &quot;:use_precompiled_headers&quot; ]
      ...
</pre><h3><a class="h" name="precompiled_header_type" href="#precompiled_header_type"><span></span></a><strong>precompiled_header_type</strong>: [string] &ldquo;gcc&rdquo; or &ldquo;msvc&rdquo;.</h3><pre class="code">  See &quot;gn help precompiled_header&quot;.
</pre><h3><a class="h" name="precompiled_source" href="#precompiled_source"><span></span></a><strong>precompiled_source</strong>: [file name] Source file to precompile.</h3><pre class="code">  The source file that goes along with the precompiled_header when using
  &quot;msvc&quot;-style precompiled headers. It will be implicitly added to the sources
  of the target. See &quot;gn help precompiled_header&quot;.
</pre><h3><a class="h" name="product_type" href="#product_type"><span></span></a><strong>product_type</strong>: Product type for Xcode projects.</h3><pre class="code">  Correspond to the type of the product of a create_bundle target. Only
  meaningful to Xcode (used as part of the Xcode project generation).

  When generating Xcode project files, only create_bundle target with a
  non-empty product_type will have a corresponding target in Xcode project.
</pre><h3><a class="h" name="public" href="#public"><span></span></a><strong>public</strong>: Declare public header files for a target.</h3><pre class="code">  A list of files that other targets can include. These permissions are checked
  via the &quot;check&quot; command (see &quot;gn help check&quot;).

  If no public files are declared, other targets (assuming they have visibility
  to depend on this target) can include any file in the sources list. If this
  variable is defined on a target, dependent targets may only include files on
  this whitelist.

  Header file permissions are also subject to visibility. A target must be
  visible to another target to include any files from it at all and the public
  headers indicate which subset of those files are permitted. See &quot;gn help
  visibility&quot; for more.

  Public files are inherited through the dependency tree. So if there is a
  dependency A -&gt; B -&gt; C, then A can include C&#39;s public headers. However, the
  same is NOT true of visibility, so unless A is in C&#39;s visibility list, the
  include will be rejected.

  GN only knows about files declared in the &quot;sources&quot; and &quot;public&quot; sections of
  targets. If a file is included that is not known to the build, it will be
  allowed.
</pre><h4><a class="h" name="Variables-you-set-in-targets-public_Declare-public-header-files-for-a-target-Examples" href="#Variables-you-set-in-targets-public_Declare-public-header-files-for-a-target-Examples"><span></span></a><a class="h" name="variables-you-set-in-targets-public_declare-public-header-files-for-a-target-examples" href="#variables-you-set-in-targets-public_declare-public-header-files-for-a-target-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  These exact files are public:
    public = [ &quot;foo.h&quot;, &quot;bar.h&quot; ]

  No files are public (no targets may include headers from this one):
    public = []
</pre><h3><a class="h" name="public_configs" href="#public_configs"><span></span></a><strong>public_configs</strong>: Configs to be applied on dependents.</h3><pre class="code">  A list of config labels.

  Targets directly depending on this one will have the configs listed in this
  variable added to them. These configs will also apply to the current target.

  This addition happens in a second phase once a target and all of its
  dependencies have been resolved. Therefore, a target will not see these
  force-added configs in their &quot;configs&quot; variable while the script is running,
  and they can not be removed. As a result, this capability should generally
  only be used to add defines and include directories necessary to compile a
  target&#39;s headers.

  See also &quot;all_dependent_configs&quot;.
</pre><h4><a class="h" name="Variables-you-set-in-targets-public_configs_Configs-to-be-applied-on-dependents-Ordering-of-flags-and-values" href="#Variables-you-set-in-targets-public_configs_Configs-to-be-applied-on-dependents-Ordering-of-flags-and-values"><span></span></a><a class="h" name="variables-you-set-in-targets-public_configs_configs-to-be-applied-on-dependents-ordering-of-flags-and-values" href="#variables-you-set-in-targets-public_configs_configs-to-be-applied-on-dependents-ordering-of-flags-and-values"><span></span></a><strong>Ordering of flags and values</strong></h4><pre class="code">  1. Those set on the current target (not in a config).
  2. Those set on the &quot;configs&quot; on the target in order that the
     configs appear in the list.
  3. Those set on the &quot;all_dependent_configs&quot; on the target in order
     that the configs appear in the list.
  4. Those set on the &quot;public_configs&quot; on the target in order that
     those configs appear in the list.
  5. all_dependent_configs pulled from dependencies, in the order of
     the &quot;deps&quot; list. This is done recursively. If a config appears
     more than once, only the first occurance will be used.
  6. public_configs pulled from dependencies, in the order of the
     &quot;deps&quot; list. If a dependency is public, they will be applied
     recursively.
</pre><h3><a class="h" name="public_deps" href="#public_deps"><span></span></a><strong>public_deps</strong>: Declare public dependencies.</h3><pre class="code">  Public dependencies are like private dependencies (see &quot;gn help deps&quot;) but
  additionally express that the current target exposes the listed deps as part
  of its public API.

  This has several ramifications:

    - public_configs that are part of the dependency are forwarded to direct
      dependents.

    - Public headers in the dependency are usable by dependents (includes do
      not require a direct dependency or visibility).

    - If the current target is a shared library, other shared libraries that it
      publicly depends on (directly or indirectly) are propagated up the
      dependency tree to dependents for linking.
</pre><h4><a class="h" name="Discussion" href="#Discussion"><span></span></a><a class="h" name="discussion" href="#discussion"><span></span></a><strong>Discussion</strong></h4><pre class="code">  Say you have three targets: A -&gt; B -&gt; C. C&#39;s visibility may allow B to depend
  on it but not A. Normally, this would prevent A from including any headers
  from C, and C&#39;s public_configs would apply only to B.

  If B lists C in its public_deps instead of regular deps, A will now inherit
  C&#39;s public_configs and the ability to include C&#39;s public headers.

  Generally if you are writing a target B and you include C&#39;s headers as part
  of B&#39;s public headers, or targets depending on B should consider B and C to
  be part of a unit, you should use public_deps instead of deps.
</pre><h4><a class="h" name="Variables-you-set-in-targets-public_deps_Declare-public-dependencies-Example" href="#Variables-you-set-in-targets-public_deps_Declare-public-dependencies-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-public_deps_declare-public-dependencies-example" href="#variables-you-set-in-targets-public_deps_declare-public-dependencies-example"><span></span></a><strong>Example</strong></h4><pre class="code">  # This target can include files from &quot;c&quot; but not from
  # &quot;super_secret_implementation_details&quot;.
  executable(&quot;a&quot;) {
    deps = [ &quot;:b&quot; ]
  }

  shared_library(&quot;b&quot;) {
    deps = [ &quot;:super_secret_implementation_details&quot; ]
    public_deps = [ &quot;:c&quot; ]
  }
</pre><h3><a class="h" name="response_file_contents" href="#response_file_contents"><span></span></a><strong>response_file_contents</strong>: Contents of a response file for actions.</h3><pre class="code">  Sometimes the arguments passed to a script can be too long for the system&#39;s
  command-line capabilities. This is especially the case on Windows where the
  maximum command-line length is less than 8K. A response file allows you to
  pass an unlimited amount of data to a script in a temporary file for an
  action or action_foreach target.

  If the response_file_contents variable is defined and non-empty, the list
  will be treated as script args (including possibly substitution patterns)
  that will be written to a temporary file at build time. The name of the
  temporary file will be substituted for &quot;{{response_file_name}}&quot; in the script
  args.

  The response file contents will always be quoted and escaped according to
  Unix shell rules. To parse the response file, the Python script should use
  &quot;shlex.split(file_contents)&quot;.
</pre><h4><a class="h" name="Variables-you-set-in-targets-response_file_contents_Contents-of-a-response-file-for-actions-Example" href="#Variables-you-set-in-targets-response_file_contents_Contents-of-a-response-file-for-actions-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-response_file_contents_contents-of-a-response-file-for-actions-example" href="#variables-you-set-in-targets-response_file_contents_contents-of-a-response-file-for-actions-example"><span></span></a><strong>Example</strong></h4><pre class="code">  action(&quot;process_lots_of_files&quot;) {
    script = &quot;process.py&quot;,
    inputs = [ ... huge list of files ... ]

    # Write all the inputs to a response file for the script. Also,
    # make the paths relative to the script working directory.
    response_file_contents = rebase_path(inputs, root_build_dir)

    # The script expects the name of the response file in --file-list.
    args = [
      &quot;--enable-foo&quot;,
      &quot;--file-list={{response_file_name}}&quot;,
    ]
  }
</pre><h3><a class="h" name="script" href="#script"><span></span></a><strong>script</strong>: Script file for actions.</h3><pre class="code">  An absolute or buildfile-relative file name of a Python script to run for a
  action and action_foreach targets (see &quot;gn help action&quot; and &quot;gn help
  action_foreach&quot;).
</pre><h3><a class="h" name="sources" href="#sources"><span></span></a><strong>sources</strong>: Source files for a target</h3><pre class="code">  A list of files. Non-absolute paths will be resolved relative to the current
  build file.
</pre><h4><a class="h" name="Sources-for-binary-targets" href="#Sources-for-binary-targets"><span></span></a><a class="h" name="sources-for-binary-targets" href="#sources-for-binary-targets"><span></span></a><strong>Sources for binary targets</strong></h4><pre class="code">  For binary targets (source sets, executables, and libraries), the known file
  types will be compiled with the associated tools. Unknown file types and
  headers will be skipped. However, you should still list all C/C+ header files
  so GN knows about the existence of those files for the purposes of include
  checking.

  As a special case, a file ending in &quot;.def&quot; will be treated as a Windows
  module definition file. It will be appended to the link line with a
  preceeding &quot;/DEF:&quot; string. There must be at most one .def file in a target
  and they do not cross dependency boundaries (so specifying a .def file in a
  static library or source set will have no effect on the executable or shared
  library they&#39;re linked into).
</pre><h4><a class="h" name="Sources-for-non_binary-targets" href="#Sources-for-non_binary-targets"><span></span></a><a class="h" name="sources-for-non_binary-targets" href="#sources-for-non_binary-targets"><span></span></a><strong>Sources for non-binary targets</strong></h4><pre class="code">  action_foreach
    The sources are the set of files that the script will be executed over. The
    script will run once per file.

  action
    The sources will be treated the same as inputs. See &quot;gn help inputs&quot; for
    more information and usage advice.

  copy
    The source are the source files to copy.
</pre><h3><a class="h" name="testonly" href="#testonly"><span></span></a><strong>testonly</strong>: Declares a target must only be used for testing.</h3><pre class="code">  Boolean. Defaults to false.

  When a target is marked &quot;testonly = true&quot;, it must only be depended on by
  other test-only targets. Otherwise, GN will issue an error that the
  depenedency is not allowed.

  This feature is intended to prevent accidentally shipping test code in a
  final product.
</pre><h4><a class="h" name="Variables-you-set-in-targets-testonly_Declares-a-target-must-only-be-used-for-testing-Example" href="#Variables-you-set-in-targets-testonly_Declares-a-target-must-only-be-used-for-testing-Example"><span></span></a><a class="h" name="variables-you-set-in-targets-testonly_declares-a-target-must-only-be-used-for-testing-example" href="#variables-you-set-in-targets-testonly_declares-a-target-must-only-be-used-for-testing-example"><span></span></a><strong>Example</strong></h4><pre class="code">  source_set(&quot;test_support&quot;) {
    testonly = true
    ...
  }
</pre><h3><a class="h" name="visibility" href="#visibility"><span></span></a><strong>visibility</strong>: A list of labels that can depend on a target.</h3><pre class="code">  A list of labels and label patterns that define which targets can depend on
  the current one. These permissions are checked via the &quot;check&quot; command (see
  &quot;gn help check&quot;).

  If visibility is not defined, it defaults to public (&quot;*&quot;).

  If visibility is defined, only the targets with labels that match it can
  depend on the current target. The empty list means no targets can depend on
  the current target.

  Tip: Often you will want the same visibility for all targets in a BUILD file.
  In this case you can just put the definition at the top, outside of any
  target, and the targets will inherit that scope and see the definition.
</pre><h4><a class="h" name="Patterns" href="#Patterns"><span></span></a><a class="h" name="patterns" href="#patterns"><span></span></a><strong>Patterns</strong></h4><pre class="code">  See &quot;gn help label_pattern&quot; for more details on what types of patterns are
  supported. If a toolchain is specified, only targets in that toolchain will
  be matched. If a toolchain is not specified on a pattern, targets in all
  toolchains will be matched.
</pre><h4><a class="h" name="Variables-you-set-in-targets-visibility_A-list-of-labels-that-can-depend-on-a-target-Examples" href="#Variables-you-set-in-targets-visibility_A-list-of-labels-that-can-depend-on-a-target-Examples"><span></span></a><a class="h" name="variables-you-set-in-targets-visibility_a-list-of-labels-that-can-depend-on-a-target-examples" href="#variables-you-set-in-targets-visibility_a-list-of-labels-that-can-depend-on-a-target-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  Only targets in the current buildfile (&quot;private&quot;):
    visibility = [ &quot;:*&quot; ]

  No targets (used for targets that should be leaf nodes):
    visibility = []

  Any target (&quot;public&quot;, the default):
    visibility = [ &quot;*&quot; ]

  All targets in the current directory and any subdirectory:
    visibility = [ &quot;./*&quot; ]

  Any target in &quot;//bar/BUILD.gn&quot;:
    visibility = [ &quot;//bar:*&quot; ]

  Any target in &quot;//bar/&quot; or any subdirectory thereof:
    visibility = [ &quot;//bar/*&quot; ]

  Just these specific targets:
    visibility = [ &quot;:mything&quot;, &quot;//foo:something_else&quot; ]

  Any target in the current directory and any subdirectory thereof, plus
  any targets in &quot;//bar/&quot; and any subdirectory thereof.
    visibility = [ &quot;./*&quot;, &quot;//bar/*&quot; ]
</pre><h3><a class="h" name="write_runtime_deps" href="#write_runtime_deps"><span></span></a><strong>write_runtime_deps</strong>: Writes the target&#39;s runtime_deps to the given path.</h3><pre class="code">  Does not synchronously write the file, but rather schedules it to be written
  at the end of generation.

  If the file exists and the contents are identical to that being written, the
  file will not be updated. This will prevent unnecessary rebuilds of targets
  that depend on this file.

  Path must be within the output directory.

  See &quot;gn help runtime_deps&quot; for how the runtime dependencies are computed.

  The format of this file will list one file per line with no escaping. The
  files will be relative to the root_build_dir. The first line of the file will
  be the main output file of the target itself. The file contents will be the
  same as requesting the runtime deps be written on the command line (see &quot;gn
  help --runtime-deps-list-file&quot;).
</pre><h3><a class="h" name="xcode_extra_attributes" href="#xcode_extra_attributes"><span></span></a><strong>xcode_extra_attributes</strong>: [scope] Extra attributes for Xcode projects.</h3><pre class="code">  The value defined in this scope will be copied to the EXTRA_ATTRIBUTES
  property of the generated Xcode project. They are only meaningful when
  generating with --ide=xcode.

  See &quot;gn help create_bundle&quot; for more information.
</pre><h3><a class="h" name="test_application_name" href="#test_application_name"><span></span></a><strong>test_application_name</strong>: Test application name for unit or ui test target.</h3><pre class="code">  Each unit and ui test target must have a test application target, and this
  value is used to specify the relationship. Only meaningful to Xcode (used as
  part of the Xcode project generation).

  See &quot;gn help create_bundle&quot; for more information.
</pre><h4><a class="h" name="Exmaple" href="#Exmaple"><span></span></a><a class="h" name="exmaple" href="#exmaple"><span></span></a><strong>Exmaple</strong></h4><pre class="code">  create_bundle(&quot;chrome_xctest&quot;) {
    test_application_name = &quot;chrome&quot;
    ...
  }
</pre><h2><a class="h" name="other" href="#other"><span></span></a>Other help topics</h2><h3><a class="h" name="buildargs" href="#buildargs"><span></span></a><strong>Build Arguments Overview</strong></h3><pre class="code">  Build arguments are variables passed in from outside of the build that build
  files can query to determine how the build works.
</pre><h4><a class="h" name="How-build-arguments-are-set" href="#How-build-arguments-are-set"><span></span></a><a class="h" name="how-build-arguments-are-set" href="#how-build-arguments-are-set"><span></span></a><strong>How build arguments are set</strong></h4><pre class="code">  First, system default arguments are set based on the current system. The
  built-in arguments are:
   - host_cpu
   - host_os
   - current_cpu
   - current_os
   - target_cpu
   - target_os

  Next, project-specific overrides are applied. These are specified inside
  the default_args variable of //.gn. See &quot;gn help dotfile&quot; for more.

  If specified, arguments from the --args command line flag are used. If that
  flag is not specified, args from previous builds in the build directory will
  be used (this is in the file args.gn in the build directory).

  Last, for targets being compiled with a non-default toolchain, the toolchain
  overrides are applied. These are specified in the toolchain_args section of a
  toolchain definition. The use-case for this is that a toolchain may be
  building code for a different platform, and that it may want to always
  specify Posix, for example. See &quot;gn help toolchain&quot; for more.

  If you specify an override for a build argument that never appears in a
  &quot;declare_args&quot; call, a nonfatal error will be displayed.
</pre><h4><a class="h" name="Other-help-topics-Build-Arguments-Overview-Examples" href="#Other-help-topics-Build-Arguments-Overview-Examples"><span></span></a><a class="h" name="other-help-topics-build-arguments-overview-examples" href="#other-help-topics-build-arguments-overview-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  gn args out/FooBar
      Create the directory out/FooBar and open an editor. You would type
      something like this into that file:
          enable_doom_melon=false
          os=&quot;android&quot;

  gn gen out/FooBar --args=&quot;enable_doom_melon=true os=\&quot;android\&quot;&quot;
      This will overwrite the build directory with the given arguments. (Note
      that the quotes inside the args command will usually need to be escaped
      for your shell to pass through strings values.)
</pre><h4><a class="h" name="How-build-arguments-are-used" href="#How-build-arguments-are-used"><span></span></a><a class="h" name="how-build-arguments-are-used" href="#how-build-arguments-are-used"><span></span></a><strong>How build arguments are used</strong></h4><pre class="code">  If you want to use an argument, you use declare_args() and specify default
  values. These default values will apply if none of the steps listed in the
  &quot;How build arguments are set&quot; section above apply to the given argument, but
  the defaults will not override any of these.

  Often, the root build config file will declare global arguments that will be
  passed to all buildfiles. Individual build files can also specify arguments
  that apply only to those files. It is also useful to specify build args in an
  &quot;import&quot;-ed file if you want such arguments to apply to multiple buildfiles.
</pre><h3><a class="h" name="dotfile" href="#dotfile"><span></span></a><strong>.gn file</strong></h3><pre class="code">  When gn starts, it will search the current directory and parent directories
  for a file called &quot;.gn&quot;. This indicates the source root. You can override
  this detection by using the --root command-line argument

  The .gn file in the source root will be executed. The syntax is the same as a
  buildfile, but with very limited build setup-specific meaning.

  If you specify --root, by default GN will look for the file .gn in that
  directory. If you want to specify a different file, you can additionally pass
  --dotfile:

    gn gen out/Debug --root=/home/build --dotfile=/home/my_gn_file.gn
</pre><h4><a class="h" name="Other-help-topics-gn-file-Variables" href="#Other-help-topics-gn-file-Variables"><span></span></a><a class="h" name="other-help-topics-gn-file-variables" href="#other-help-topics-gn-file-variables"><span></span></a><strong>Variables</strong></h4><pre class="code">  arg_file_template [optional]
      Path to a file containing the text that should be used as the default
      args.gn content when you run `gn args`.

  buildconfig [required]
      Path to the build config file. This file will be used to set up the
      build file execution environment for each toolchain.

  check_targets [optional]
      A list of labels and label patterns that should be checked when running
      &quot;gn check&quot; or &quot;gn gen --check&quot;. If unspecified, all targets will be
      checked. If it is the empty list, no targets will be checked.

      The format of this list is identical to that of &quot;visibility&quot; so see &quot;gn
      help visibility&quot; for examples.

  exec_script_whitelist [optional]
      A list of .gn/.gni files (not labels) that have permission to call the
      exec_script function. If this list is defined, calls to exec_script will
      be checked against this list and GN will fail if the current file isn&#39;t
      in the list.

      This is to allow the use of exec_script to be restricted since is easy to
      use inappropriately. Wildcards are not supported. Files in the
      secondary_source tree (if defined) should be referenced by ignoring the
      secondary tree and naming them as if they are in the main tree.

      If unspecified, the ability to call exec_script is unrestricted.

      Example:
        exec_script_whitelist = [
          &quot;//base/BUILD.gn&quot;,
          &quot;//build/my_config.gni&quot;,
        ]

  root [optional]
      Label of the root build target. The GN build will start by loading the
      build file containing this target name. This defaults to &quot;//:&quot; which will
      cause the file //BUILD.gn to be loaded.

  script_executable [optional]
      Path to specific Python executable or potentially a different language
      interpreter that is used to execute scripts in action targets and
      exec_script calls.

  secondary_source [optional]
      Label of an alternate directory tree to find input files. When searching
      for a BUILD.gn file (or the build config file discussed above), the file
      will first be looked for in the source root. If it&#39;s not found, the
      secondary source root will be checked (which would contain a parallel
      directory hierarchy).

      This behavior is intended to be used when BUILD.gn files can&#39;t be checked
      in to certain source directories for whatever reason.

      The secondary source root must be inside the main source tree.

  default_args [optional]
      Scope containing the default overrides for declared arguments. These
      overrides take precedence over the default values specified in the
      declare_args() block, but can be overriden using --args or the
      args.gn file.

      This is intended to be used when subprojects declare arguments with
      default values that need to be changed for whatever reason.
</pre><h4><a class="h" name="Example-gn-file-contents" href="#Example-gn-file-contents"><span></span></a><a class="h" name="example-gn-file-contents" href="#example-gn-file-contents"><span></span></a><strong>Example .gn file contents</strong></h4><pre class="code">  buildconfig = &quot;//build/config/BUILDCONFIG.gn&quot;

  check_targets = [
    &quot;//doom_melon/*&quot;,  # Check everything in this subtree.
    &quot;//tools:mind_controlling_ant&quot;,  # Check this specific target.
  ]

  root = &quot;//:root&quot;

  secondary_source = &quot;//build/config/temporary_buildfiles/&quot;

  default_args = {
    # Default to release builds for this project.
    is_debug = false
    is_component_build = false
  }
</pre><h3><a class="h" name="execution" href="#execution"><span></span></a><strong>Build graph and execution overview</strong></h3><h4><a class="h" name="Overall-build-flow" href="#Overall-build-flow"><span></span></a><a class="h" name="overall-build-flow" href="#overall-build-flow"><span></span></a><strong>Overall build flow</strong></h4><pre class="code">  1. Look for &quot;.gn&quot; file (see &quot;gn help dotfile&quot;) in the current directory and
     walk up the directory tree until one is found. Set this directory to be
     the &quot;source root&quot; and interpret this file to find the name of the build
     config file.

  2. Execute the build config file identified by .gn to set up the global
     variables and default toolchain name. Any arguments, variables, defaults,
     etc. set up in this file will be visible to all files in the build.

  3. Load the //BUILD.gn (in the source root directory).

  4. Recursively evaluate rules and load BUILD.gn in other directories as
     necessary to resolve dependencies. If a BUILD file isn&#39;t found in the
     specified location, GN will look in the corresponding location inside
     the secondary_source defined in the dotfile (see &quot;gn help dotfile&quot;).

  5. When a target&#39;s dependencies are resolved, write out the `.ninja`
     file to disk.

  6. When all targets are resolved, write out the root build.ninja file.
</pre><h4><a class="h" name="Executing-target-definitions-and-templates" href="#Executing-target-definitions-and-templates"><span></span></a><a class="h" name="executing-target-definitions-and-templates" href="#executing-target-definitions-and-templates"><span></span></a><strong>Executing target definitions and templates</strong></h4><pre class="code">  Build files are loaded in parallel. This means it is impossible to
  interrogate a target from GN code for any information not derivable from its
  label (see &quot;gn help label&quot;). The exception is the get_target_outputs()
  function which requires the target being interrogated to have been defined
  previously in the same file.

  Targets are declared by their type and given a name:

    static_library(&quot;my_static_library&quot;) {
      ... target parameter definitions ...
    }

  There is also a generic &quot;target&quot; function for programatically defined types
  (see &quot;gn help target&quot;). You can define new types using templates (see &quot;gn
  help template&quot;). A template defines some custom code that expands to one or
  more other targets.

  Before executing the code inside the target&#39;s { }, the target defaults are
  applied (see &quot;gn help set_defaults&quot;). It will inject implicit variable
  definitions that can be overridden by the target code as necessary. Typically
  this mechanism is used to inject a default set of configs that define the
  global compiler and linker flags.
</pre><h4><a class="h" name="Which-targets-are-built" href="#Which-targets-are-built"><span></span></a><a class="h" name="which-targets-are-built" href="#which-targets-are-built"><span></span></a><strong>Which targets are built</strong></h4><pre class="code">  All targets encountered in the default toolchain (see &quot;gn help toolchain&quot;)
  will have build rules generated for them, even if no other targets reference
  them. Their dependencies must resolve and they will be added to the implicit
  &quot;all&quot; rule (see &quot;gn help ninja_rules&quot;).

  Targets in non-default toolchains will only be generated when they are
  required (directly or transitively) to build a target in the default
  toolchain.

  See also &quot;gn help ninja_rules&quot;.
</pre><h4><a class="h" name="Dependencies" href="#Dependencies"><span></span></a><a class="h" name="dependencies" href="#dependencies"><span></span></a><strong>Dependencies</strong></h4><pre class="code">  The only difference between &quot;public_deps&quot; and &quot;deps&quot; except for pushing
  configs around the build tree and allowing includes for the purposes of &quot;gn
  check&quot;.

  A target&#39;s &quot;data_deps&quot; are guaranteed to be built whenever the target is
  built, but the ordering is not defined. The meaning of this is dependencies
  required at runtime. Currently data deps will be complete before the target
  is linked, but this is not semantically guaranteed and this is undesirable
  from a build performance perspective. Since we hope to change this in the
  future, do not rely on this behavior.
</pre><h3><a class="h" name="grammar" href="#grammar"><span></span></a><strong>Language and grammar for GN build files</strong></h3><h4><a class="h" name="Tokens" href="#Tokens"><span></span></a><a class="h" name="tokens" href="#tokens"><span></span></a><strong>Tokens</strong></h4><pre class="code">  GN build files are read as sequences of tokens.  While splitting the file
  into tokens, the next token is the longest sequence of characters that form a
  valid token.
</pre><h4><a class="h" name="White-space-and-comments" href="#White-space-and-comments"><span></span></a><a class="h" name="white-space-and-comments" href="#white-space-and-comments"><span></span></a><strong>White space and comments</strong></h4><pre class="code">  White space is comprised of spaces (U+0020), horizontal tabs (U+0009),
  carriage returns (U+000D), and newlines (U+000A).

  Comments start at the character &quot;#&quot; and stop at the next newline.

  White space and comments are ignored except that they may separate tokens
  that would otherwise combine into a single token.
</pre><h4><a class="h" name="Identifiers" href="#Identifiers"><span></span></a><a class="h" name="identifiers" href="#identifiers"><span></span></a><strong>Identifiers</strong></h4><pre class="code">  Identifiers name variables and functions.

      identifier = letter { letter | digit } .
      letter     = &quot;A&quot; ... &quot;Z&quot; | &quot;a&quot; ... &quot;z&quot; | &quot;_&quot; .
      digit      = &quot;0&quot; ... &quot;9&quot; .
</pre><h4><a class="h" name="Keywords" href="#Keywords"><span></span></a><a class="h" name="keywords" href="#keywords"><span></span></a><strong>Keywords</strong></h4><pre class="code">  The following keywords are reserved and may not be used as identifiers:

          else    false   if      true
</pre><h4><a class="h" name="Integer-literals" href="#Integer-literals"><span></span></a><a class="h" name="integer-literals" href="#integer-literals"><span></span></a><strong>Integer literals</strong></h4><pre class="code">  An integer literal represents a decimal integer value.

      integer = [ &quot;-&quot; ] digit { digit } .

  Leading zeros and negative zero are disallowed.
</pre><h4><a class="h" name="String-literals" href="#String-literals"><span></span></a><a class="h" name="string-literals" href="#string-literals"><span></span></a><strong>String literals</strong></h4><pre class="code">  A string literal represents a string value consisting of the quoted
  characters with possible escape sequences and variable expansions.

      string           = `&quot;` { char | escape | expansion } `&quot;` .
      escape           = `\` ( &quot;$&quot; | `&quot;` | char ) .
      BracketExpansion = &quot;{&quot; ( identifier | ArrayAccess | ScopeAccess &quot;
                         &quot;) &quot;}&quot; .
      Hex              = &quot;0x&quot; [0-9A-Fa-f][0-9A-Fa-f]
      expansion        = &quot;$&quot; ( identifier | BracketExpansion | Hex ) .
      char             = /* any character except &quot;$&quot;, `&quot;`, or newline &quot;
                        &quot;*/ .

  After a backslash, certain sequences represent special characters:

          \&quot;    U+0022    quotation mark
          \$    U+0024    dollar sign
          \\    U+005C    backslash

  All other backslashes represent themselves.

  To insert an arbitrary byte value, use $0xFF. For example, to insert a
  newline character: &quot;Line one$0x0ALine two&quot;.

  An expansion will evaluate the variable following the &#39;$&#39; and insert a
  stringified version of it into the result. For example, to concat two path
  components with a slash separating them:
    &quot;$var_one/$var_two&quot;
  Use the &quot;${var_one}&quot; format to be explicitly deliniate the variable for
  otherwise-ambiguous cases.
</pre><h4><a class="h" name="Punctuation" href="#Punctuation"><span></span></a><a class="h" name="punctuation" href="#punctuation"><span></span></a><strong>Punctuation</strong></h4><pre class="code">  The following character sequences represent punctuation:

          +       +=      ==      !=      (       )
          -       -=      &lt;       &lt;=      [       ]
          !       =       &gt;       &gt;=      {       }
                          &amp;&amp;      ||      .       ,
</pre><h4><a class="h" name="Grammar" href="#Grammar"><span></span></a><a class="h" name="grammar" href="#grammar"><span></span></a><strong>Grammar</strong></h4><pre class="code">  The input tokens form a syntax tree following a context-free grammar:

      File = StatementList .

      Statement     = Assignment | Call | Condition .
      LValue        = identifier | ArrayAccess | ScopeAccess .
      Assignment    = LValue AssignOp Expr .
      Call          = identifier &quot;(&quot; [ ExprList ] &quot;)&quot; [ Block ] .
      Condition     = &quot;if&quot; &quot;(&quot; Expr &quot;)&quot; Block
                      [ &quot;else&quot; ( Condition | Block ) ] .
      Block         = &quot;{&quot; StatementList &quot;}&quot; .
      StatementList = { Statement } .

      ArrayAccess = identifier &quot;[&quot; Expr &quot;]&quot; .
      ScopeAccess = identifier &quot;.&quot; identifier .
      Expr        = UnaryExpr | Expr BinaryOp Expr .
      UnaryExpr   = PrimaryExpr | UnaryOp UnaryExpr .
      PrimaryExpr = identifier | integer | string | Call
                  | ArrayAccess | ScopeAccess | Block
                  | &quot;(&quot; Expr &quot;)&quot;
                  | &quot;[&quot; [ ExprList [ &quot;,&quot; ] ] &quot;]&quot; .
      ExprList    = Expr { &quot;,&quot; Expr } .

      AssignOp = &quot;=&quot; | &quot;+=&quot; | &quot;-=&quot; .
      UnaryOp  = &quot;!&quot; .
      BinaryOp = &quot;+&quot; | &quot;-&quot;                  // highest priority
               | &quot;&lt;&quot; | &quot;&lt;=&quot; | &quot;&gt;&quot; | &quot;&gt;=&quot;
               | &quot;==&quot; | &quot;!=&quot;
               | &quot;&amp;&amp;&quot;
               | &quot;||&quot; .                     // lowest priority

  All binary operators are left-associative.
</pre><h4><a class="h" name="Types" href="#Types"><span></span></a><a class="h" name="types" href="#types"><span></span></a><strong>Types</strong></h4><pre class="code">  The GN language is dynamically typed. The following types are used:

   - Boolean: Uses the keywords &quot;true&quot; and &quot;false&quot;. There is no implicit
     conversion between booleans and integers.

   - Integers: All numbers in GN are signed 64-bit integers.

   - Strings: Strings are 8-bit with no enforced encoding. When a string is
     used to interact with other systems with particular encodings (like the
     Windows and Mac filesystems) it is assumed to be UTF-8. See &quot;String
     literals&quot; above for more.

   - Lists: Lists are arbitrary-length ordered lists of values. See &quot;Lists&quot;
     below for more.

   - Scopes: Scopes are like dictionaries that use variable names for keys. See
     &quot;Scopes&quot; below for more.
</pre><h4><a class="h" name="Lists" href="#Lists"><span></span></a><a class="h" name="lists" href="#lists"><span></span></a><strong>Lists</strong></h4><pre class="code">  Lists are created with [] and using commas to separate items:

       mylist = [ 0, 1, 2, &quot;some string&quot; ]

  A comma after the last item is optional. Lists are dereferenced using 0-based
  indexing:

       mylist[0] += 1
       var = mylist[2]

  Lists can be concatenated using the &#39;+&#39; and &#39;+=&#39; operators. Bare values can
  not be concatenated with lists, to add a single item, it must be put into a
  list of length one.

  Items can be removed from lists using the &#39;-&#39; and &#39;-=&#39; operators. This will
  remove all occurrences of every item in the right-hand list from the
  left-hand list. It is an error to remove an item not in the list. This is to
  prevent common typos and to detect dead code that is removing things that no
  longer apply.

  It is an error to use &#39;=&#39; to replace a nonempty list with another nonempty
  list. This is to prevent accidentally overwriting data when in most cases
  &#39;+=&#39; was intended. To overwrite a list on purpose, first assign it to the
  empty list:

    mylist = []
    mylist = otherlist

  When assigning to a list named &#39;sources&#39; using &#39;=&#39; or &#39;+=&#39;, list items may be
  automatically filtered out. See &quot;gn help set_sources_assignment_filter&quot; for
  more.
</pre><h4><a class="h" name="Scopes" href="#Scopes"><span></span></a><a class="h" name="scopes" href="#scopes"><span></span></a><strong>Scopes</strong></h4><pre class="code">  All execution happens in the context of a scope which holds the current state
  (like variables). With the exception of loops and conditions, &#39;{&#39; introduces
  a new scope that has a parent reference to the old scope.

  Variable reads recursively search all nested scopes until the variable is
  found or there are no more scopes. Variable writes always go into the current
  scope. This means that after the closing &#39;}&#39; (again excepting loops and
  conditions), all local variables will be restored to the previous values.
  This also means that &quot;foo = foo&quot; can do useful work by copying a variable
  into the current scope that was defined in a containing scope.

  Scopes can also be assigned to variables. Such scopes can be created by
  functions like exec_script, when invoking a template (the template code
  refers to the variables set by the invoking code by the implicitly-created
  &quot;invoker&quot; scope), or explicitly like:

    empty_scope = {}
    myvalues = {
      foo = 21
      bar = &quot;something&quot;
    }

  Inside such a scope definition can be any GN code including conditionals and
  function calls. After the close of the scope, it will contain all variables
  explicitly set by the code contained inside it. After this, the values can be
  read, modified, or added to:

    myvalues.foo += 2
    empty_scope.new_thing = [ 1, 2, 3 ]
</pre><h3><a class="h" name="input_conversion" href="#input_conversion"><span></span></a><strong>input_conversion</strong>: Specifies how to transform input to a variable.</h3><pre class="code">  input_conversion is an argument to read_file and exec_script that specifies
  how the result of the read operation should be converted into a variable.

  &quot;&quot; (the default)
      Discard the result and return None.

  &quot;list lines&quot;
      Return the file contents as a list, with a string for each line. The
      newlines will not be present in the result. The last line may or may not
      end in a newline.

      After splitting, each individual line will be trimmed of whitespace on
      both ends.

  &quot;scope&quot;
      Execute the block as GN code and return a scope with the resulting values
      in it. If the input was:
        a = [ &quot;hello.cc&quot;, &quot;world.cc&quot; ]
        b = 26
      and you read the result into a variable named &quot;val&quot;, then you could
      access contents the &quot;.&quot; operator on &quot;val&quot;:
        sources = val.a
        some_count = val.b

  &quot;string&quot;
      Return the file contents into a single string.

  &quot;value&quot;
      Parse the input as if it was a literal rvalue in a buildfile. Examples of
      typical program output using this mode:
        [ &quot;foo&quot;, &quot;bar&quot; ]     (result will be a list)
      or
        &quot;foo bar&quot;            (result will be a string)
      or
        5                    (result will be an integer)

      Note that if the input is empty, the result will be a null value which
      will produce an error if assigned to a variable.

  &quot;trim ...&quot;
      Prefixing any of the other transformations with the word &quot;trim&quot; will
      result in whitespace being trimmed from the beginning and end of the
      result before processing.

      Examples: &quot;trim string&quot; or &quot;trim list lines&quot;

      Note that &quot;trim value&quot; is useless because the value parser skips
      whitespace anyway.
</pre><h3><a class="h" name="label_pattern" href="#label_pattern"><span></span></a><strong>Label patterns</strong></h3><pre class="code">  A label pattern is a way of expressing one or more labels in a portion of the
  source tree. They are not general regular expressions.

  They can take the following forms only:

   - Explicit (no wildcard):
       &quot;//foo/bar:baz&quot;
       &quot;:baz&quot;

   - Wildcard target names:
       &quot;//foo/bar:*&quot; (all targets in the //foo/bar/BUILD.gn file)
       &quot;:*&quot;  (all targets in the current build file)

   - Wildcard directory names (&quot;*&quot; is only supported at the end)
       &quot;*&quot;  (all targets)
       &quot;//foo/bar/*&quot;  (all targets in any subdir of //foo/bar)
       &quot;./*&quot;  (all targets in the current build file or sub dirs)

  Any of the above forms can additionally take an explicit toolchain. In this
  case, the toolchain must be fully qualified (no wildcards are supported in
  the toolchain name).

    &quot;//foo:bar(//build/toochain:mac)&quot;
        An explicit target in an explicit toolchain.

    &quot;:*(//build/toolchain/linux:32bit)&quot;
        All targets in the current build file using the 32-bit Linux toolchain.

    &quot;//foo/*(//build/toolchain:win)&quot;
        All targets in //foo and any subdirectory using the Windows
        toolchain.
</pre><h3><a class="h" name="labels" href="#labels"><span></span></a><strong>About labels</strong></h3><pre class="code">  Everything that can participate in the dependency graph (targets, configs,
  and toolchains) are identified by labels. A common label looks like:

    //base/test:test_support

  This consists of a source-root-absolute path, a colon, and a name. This means
  to look for the thing named &quot;test_support&quot; in &quot;base/test/BUILD.gn&quot;.

  You can also specify system absolute paths if necessary. Typically such
  paths would be specified via a build arg so the developer can specify where
  the component is on their system.

    /usr/local/foo:bar    (Posix)
    /C:/Program Files/MyLibs:bar   (Windows)
</pre><h4><a class="h" name="Toolchains" href="#Toolchains"><span></span></a><a class="h" name="toolchains" href="#toolchains"><span></span></a><strong>Toolchains</strong></h4><pre class="code">  A canonical label includes the label of the toolchain being used. Normally,
  the toolchain label is implicitly inherited from the current execution
  context, but you can override this to specify cross-toolchain dependencies:

    //base/test:test_support(//build/toolchain/win:msvc)

  Here GN will look for the toolchain definition called &quot;msvc&quot; in the file
  &quot;//build/toolchain/win&quot; to know how to compile this target.
</pre><h4><a class="h" name="Relative-labels" href="#Relative-labels"><span></span></a><a class="h" name="relative-labels" href="#relative-labels"><span></span></a><strong>Relative labels</strong></h4><pre class="code">  If you want to refer to something in the same buildfile, you can omit
  the path name and just start with a colon. This format is recommended for
  all same-file references.

    :base

  Labels can be specified as being relative to the current directory.
  Stylistically, we prefer to use absolute paths for all non-file-local
  references unless a build file needs to be run in different contexts (like a
  project needs to be both standalone and pulled into other projects in
  difference places in the directory hierarchy).

    source/plugin:myplugin
    ../net:url_request
</pre><h4><a class="h" name="Implicit-names" href="#Implicit-names"><span></span></a><a class="h" name="implicit-names" href="#implicit-names"><span></span></a><strong>Implicit names</strong></h4><pre class="code">  If a name is unspecified, it will inherit the directory name. Stylistically,
  we prefer to omit the colon and name when possible:

    //net  -&gt;  //net:net
    //tools/gn  -&gt;  //tools/gn:gn
</pre><h3><a class="h" name="ninja_rules" href="#ninja_rules"><span></span></a><strong>Ninja build rules</strong></h3><h4><a class="h" name="The-all-and-default-rules" href="#The-all-and-default-rules"><span></span></a><a class="h" name="the-all-and-default-rules" href="#the-all-and-default-rules"><span></span></a><strong>The &ldquo;all&rdquo; and &ldquo;default&rdquo; rules</strong></h4><pre class="code">  All generated targets (see &quot;gn help execution&quot;) will be added to an implicit
  build rule called &quot;all&quot; so &quot;ninja all&quot; will always compile everything. The
  default rule will be used by Ninja if no specific target is specified (just
  typing &quot;ninja&quot;). If there is a target named &quot;default&quot; in the root build file,
  it will be the default build rule, otherwise the implicit &quot;all&quot; rule will be
  used.
</pre><h4><a class="h" name="Phony-rules" href="#Phony-rules"><span></span></a><a class="h" name="phony-rules" href="#phony-rules"><span></span></a><strong>Phony rules</strong></h4><pre class="code">  GN generates Ninja &quot;phony&quot; rules for targets in the default toolchain.  The
  phony rules can collide with each other and with the names of generated files
  so are generated with the following priority:

    1. Actual files generated by the build always take precedence.

    2. Targets in the toplevel //BUILD.gn file.

    3. Targets in toplevel directories matching the names of the directories.
       So &quot;ninja foo&quot; can be used to compile &quot;//foo:foo&quot;. This only applies to
       the first level of directories since usually these are the most
       important (so this won&#39;t apply to &quot;//foo/bar:bar&quot;).

    4. The short names of executables if there is only one executable with that
       short name. Use &quot;ninja doom_melon&quot; to compile the
       &quot;//tools/fruit:doom_melon&quot; executable.

    5. The short names of all targets if there is only one target with that
       short name.

    6. Full label name with no leading slashes. So you can use
       &quot;ninja tools/fruit:doom_melon&quot; to build &quot;//tools/fruit:doom_melon&quot;.

    7. Labels with an implicit name part (when the short names match the
       directory). So you can use &quot;ninja foo/bar&quot; to compile &quot;//foo/bar:bar&quot;.

  These &quot;phony&quot; rules are provided only for running Ninja since this matches
  people&#39;s historical expectations for building. For consistency with the rest
  of the program, GN introspection commands accept explicit labels.

  To explicitly compile a target in a non-default toolchain, you must give
  Ninja the exact name of the output file relative to the build directory.
</pre><h3><a class="h" name="nogncheck" href="#nogncheck"><span></span></a><strong>nogncheck</strong>: Skip an include line from checking.</h3><pre class="code">  GN&#39;s header checker helps validate that the includes match the build
  dependency graph. Sometimes an include might be conditional or otherwise
  problematic, but you want to specifically allow it. In this case, it can be
  whitelisted.

  Include lines containing the substring &quot;nogncheck&quot; will be excluded from
  header checking. The most common case is a conditional include:

    #if defined(ENABLE_DOOM_MELON)
    #include &quot;tools/doom_melon/doom_melon.h&quot;  // nogncheck
    #endif

  If the build file has a conditional dependency on the corresponding target
  that matches the conditional include, everything will always link correctly:

    source_set(&quot;mytarget&quot;) {
      ...
      if (enable_doom_melon) {
        defines = [ &quot;ENABLE_DOOM_MELON&quot; ]
        deps += [ &quot;//tools/doom_melon&quot; ]
      }

  But GN&#39;s header checker does not understand preprocessor directives, won&#39;t
  know it matches the build dependencies, and will flag this include as
  incorrect when the condition is false.
</pre><h4><a class="h" name="More-information" href="#More-information"><span></span></a><a class="h" name="more-information" href="#more-information"><span></span></a><strong>More information</strong></h4><pre class="code">  The topic &quot;gn help check&quot; has general information on how checking works and
  advice on fixing problems. Targets can also opt-out of checking, see
  &quot;gn help check_includes&quot;.
</pre><h3><a class="h" name="runtime_deps" href="#runtime_deps"><span></span></a><strong>Runtime dependencies</strong></h3><pre class="code">  Runtime dependencies of a target are exposed via the &quot;runtime_deps&quot; category
  of &quot;gn desc&quot; (see &quot;gn help desc&quot;) or they can be written at build generation
  time via write_runtime_deps(), or --runtime-deps-list-file (see &quot;gn help
  --runtime-deps-list-file&quot;).

  To a first approximation, the runtime dependencies of a target are the set of
  &quot;data&quot; files, data directories, and the shared libraries from all transitive
  dependencies. Executables, shared libraries, and loadable modules are
  considered runtime dependencies of themselves.
</pre><h4><a class="h" name="Executables" href="#Executables"><span></span></a><a class="h" name="executables" href="#executables"><span></span></a><strong>Executables</strong></h4><pre class="code">  Executable targets and those executable targets&#39; transitive dependencies are
  not considered unless that executable is listed in &quot;data_deps&quot;. Otherwise, GN
  assumes that the executable (and everything it requires) is a build-time
  dependency only.
</pre><h4><a class="h" name="Actions-and-copies" href="#Actions-and-copies"><span></span></a><a class="h" name="actions-and-copies" href="#actions-and-copies"><span></span></a><strong>Actions and copies</strong></h4><pre class="code">  Action and copy targets that are listed as &quot;data_deps&quot; will have all of their
  outputs and data files considered as runtime dependencies. Action and copy
  targets that are &quot;deps&quot; or &quot;public_deps&quot; will have only their data files
  considered as runtime dependencies. These targets can list an output file in
  both the &quot;outputs&quot; and &quot;data&quot; lists to force an output file as a runtime
  dependency in all cases.

  The different rules for deps and data_deps are to express build-time (deps)
  vs. run-time (data_deps) outputs. If GN counted all build-time copy steps as
  data dependencies, there would be a lot of extra stuff, and if GN counted all
  run-time dependencies as regular deps, the build&#39;s parallelism would be
  unnecessarily constrained.

  This rule can sometimes lead to unintuitive results. For example, given the
  three targets:
    A  --[data_deps]--&gt;  B  --[deps]--&gt;  ACTION
  GN would say that A does not have runtime deps on the result of the ACTION,
  which is often correct. But the purpose of the B target might be to collect
  many actions into one logic unit, and the &quot;data&quot;-ness of A&#39;s dependency is
  lost. Solutions:

   - List the outputs of the action in it&#39;s data section (if the results of
     that action are always runtime files).
   - Have B list the action in data_deps (if the outputs of the actions are
     always runtime files).
   - Have B list the action in both deps and data deps (if the outputs might be
     used in both contexts and you don&#39;t care about unnecessary entries in the
     list of files required at runtime).
   - Split B into run-time and build-time versions with the appropriate &quot;deps&quot;
     for each.
</pre><h4><a class="h" name="Static-libraries-and-source-sets" href="#Static-libraries-and-source-sets"><span></span></a><a class="h" name="static-libraries-and-source-sets" href="#static-libraries-and-source-sets"><span></span></a><strong>Static libraries and source sets</strong></h4><pre class="code">  The results of static_library or source_set targets are not considered
  runtime dependencies since these are assumed to be intermediate targets only.
  If you need to list a static library as a runtime dependency, you can
  manually compute the .a/.lib file name for the current platform and list it
  in the &quot;data&quot; list of a target (possibly on the static library target
  itself).
</pre><h4><a class="h" name="Multiple-outputs" href="#Multiple-outputs"><span></span></a><a class="h" name="multiple-outputs" href="#multiple-outputs"><span></span></a><strong>Multiple outputs</strong></h4><pre class="code">  Linker tools can specify which of their outputs should be considered when
  computing the runtime deps by setting runtime_outputs. If this is unset on
  the tool, the default will be the first output only.
</pre><h3><a class="h" name="source_expansion" href="#source_expansion"><span></span></a><strong>How Source Expansion Works</strong></h3><pre class="code">  Source expansion is used for the action_foreach and copy target types to map
  source file names to output file names or arguments.

  To perform source expansion in the outputs, GN maps every entry in the
  sources to every entry in the outputs list, producing the cross product of
  all combinations, expanding placeholders (see below).

  Source expansion in the args works similarly, but performing the placeholder
  substitution produces a different set of arguments for each invocation of the
  script.

  If no placeholders are found, the outputs or args list will be treated as a
  static list of literal file names that do not depend on the sources.

  See &quot;gn help copy&quot; and &quot;gn help action_foreach&quot; for more on how this is
  applied.
</pre><h4><a class="h" name="Placeholders" href="#Placeholders"><span></span></a><a class="h" name="placeholders" href="#placeholders"><span></span></a><strong>Placeholders</strong></h4><pre class="code">  This section discusses only placeholders for actions. There are other
  placeholders used in the definition of tools. See &quot;gn help tool&quot; for those.

  {{source}}
      The name of the source file including directory (*). This will generally
      be used for specifying inputs to a script in the &quot;args&quot; variable.
        &quot;//foo/bar/baz.txt&quot; =&gt; &quot;../../foo/bar/baz.txt&quot;

  {{source_file_part}}
      The file part of the source including the extension.
        &quot;//foo/bar/baz.txt&quot; =&gt; &quot;baz.txt&quot;

  {{source_name_part}}
      The filename part of the source file with no directory or extension. This
      will generally be used for specifying a transformation from a source file
      to a destination file with the same name but different extension.
        &quot;//foo/bar/baz.txt&quot; =&gt; &quot;baz&quot;

  {{source_dir}}
      The directory (*) containing the source file with no trailing slash.
        &quot;//foo/bar/baz.txt&quot; =&gt; &quot;../../foo/bar&quot;

  {{source_root_relative_dir}}
      The path to the source file&#39;s directory relative to the source root, with
      no leading &quot;//&quot; or trailing slashes. If the path is system-absolute,
      (beginning in a single slash) this will just return the path with no
      trailing slash. This value will always be the same, regardless of whether
      it appears in the &quot;outputs&quot; or &quot;args&quot; section.
        &quot;//foo/bar/baz.txt&quot; =&gt; &quot;foo/bar&quot;

  {{source_gen_dir}}
      The generated file directory (*) corresponding to the source file&#39;s path.
      This will be different than the target&#39;s generated file directory if the
      source file is in a different directory than the BUILD.gn file.
        &quot;//foo/bar/baz.txt&quot; =&gt; &quot;gen/foo/bar&quot;

  {{source_out_dir}}
      The object file directory (*) corresponding to the source file&#39;s path,
      relative to the build directory. this us be different than the target&#39;s
      out directory if the source file is in a different directory than the
      build.gn file.
        &quot;//foo/bar/baz.txt&quot; =&gt; &quot;obj/foo/bar&quot;

  {{source_target_relative}}
      The path to the source file relative to the target&#39;s directory. This will
      generally be used for replicating the source directory layout in the
      output directory. This can only be used in actions and it is an error to
      use in process_file_template where there is no &quot;target&quot;.
        &quot;//foo/bar/baz.txt&quot; =&gt; &quot;baz.txt&quot;
</pre><h4><a class="h" name="Note-on-directories" href="#Note-on-directories"><span></span></a><a class="h" name="note-on-directories" href="#note-on-directories"><span></span></a><strong>(*) Note on directories</strong></h4><pre class="code">  Paths containing directories (except the source_root_relative_dir) will be
  different depending on what context the expansion is evaluated in. Generally
  it should &quot;just work&quot; but it means you can&#39;t concatenate strings containing
  these values with reasonable results.

  Details: source expansions can be used in the &quot;outputs&quot; variable, the &quot;args&quot;
  variable, and in calls to &quot;process_file_template&quot;. The &quot;args&quot; are passed to a
  script which is run from the build directory, so these directories will
  relative to the build directory for the script to find. In the other cases,
  the directories will be source- absolute (begin with a &quot;//&quot;) because the
  results of those expansions will be handled by GN internally.
</pre><h4><a class="h" name="Other-help-topics-How-Source-Expansion-Works-Examples" href="#Other-help-topics-How-Source-Expansion-Works-Examples"><span></span></a><a class="h" name="other-help-topics-how-source-expansion-works-examples" href="#other-help-topics-how-source-expansion-works-examples"><span></span></a><strong>Examples</strong></h4><pre class="code">  Non-varying outputs:
    action(&quot;hardcoded_outputs&quot;) {
      sources = [ &quot;input1.idl&quot;, &quot;input2.idl&quot; ]
      outputs = [ &quot;$target_out_dir/output1.dat&quot;,
                  &quot;$target_out_dir/output2.dat&quot; ]
    }
  The outputs in this case will be the two literal files given.

  Varying outputs:
    action_foreach(&quot;varying_outputs&quot;) {
      sources = [ &quot;input1.idl&quot;, &quot;input2.idl&quot; ]
      outputs = [ &quot;{{source_gen_dir}}/{{source_name_part}}.h&quot;,
                  &quot;{{source_gen_dir}}/{{source_name_part}}.cc&quot; ]
    }
  Performing source expansion will result in the following output names:
    //out/Debug/obj/mydirectory/input1.h
    //out/Debug/obj/mydirectory/input1.cc
    //out/Debug/obj/mydirectory/input2.h
    //out/Debug/obj/mydirectory/input2.cc
</pre><h2><a class="h" name="switches" href="#switches"><span></span></a>Command Line Switches</h2><p>**Available global switches **  Do &ldquo;gn help --the_switch_you_want_help_on&rdquo; for more. Individual commands may take command-specific switches not listed here. See the help on your specific command for more.</p><pre class="code">    *   [--args: Specifies build arguments overrides.](#--args)
    *   [--color: Force colored output.](#--color)
    *   [--dotfile: Override the name of the &quot;.gn&quot; file.](#--dotfile)
    *   [--fail-on-unused-args: Treat unused build args as fatal errors.](#--fail-on-unused-args)
    *   [--markdown: Write help output in the Markdown format.](#--markdown)
    *   [--nocolor: Force non-colored output.](#--nocolor)
    *   [-q: Quiet mode. Don&#39;t print output on success.](#-q)
    *   [--root: Explicitly specify source root.](#--root)
    *   [--runtime-deps-list-file: Save runtime dependencies for targets in file.](#--runtime-deps-list-file)
    *   [--script-executable: Set the executable used to execute scripts.](#--script-executable)
    *   [--threads: Specify number of worker threads.](#--threads)
    *   [--time: Outputs a summary of how long everything took.](#--time)
    *   [--tracelog: Writes a Chrome-compatible trace log to the given file.](#--tracelog)
    *   [-v: Verbose logging.](#-v)
    *   [--version: Prints the GN version number and exits.](#--version)
</pre></div></div></div><footer class="Site-footer"><div class="Footer"><span class="Footer-poweredBy">Powered by <a href="https://gerrit.googlesource.com/gitiles/">Gitiles</a></span><div class="Footer-links"><a class="Footer-link" href="/chromium/src/+show/master/tools/gn/docs/reference.md">source</a><a class="Footer-link" href="/chromium/src/+log/master/tools/gn/docs/reference.md">log</a><a class="Footer-link" href="/chromium/src/+blame/master/tools/gn/docs/reference.md">blame</a></div></div></footer><script>(function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){(i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o), m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)})(window,document,'script','//www.google-analytics.com/analytics.js','ga'); ga('create', 'UA-55762617-15', 'auto'); ga('send', 'pageview', {title: 'GN Reference'});</script></body></html>