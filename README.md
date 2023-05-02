Download Link: https://assignmentchef.com/product/solved-cpe212-project01
<br>






A          fundamental  software         engineering    skill     is         the      design,            implementation,        and      testing of         a software         component     that     must   be        integrated      into     a          larger  software         product.                      In        order  to do        this,     the      software         component     must   conform          to         a          previously      agreed upon   interface         format. As        part     of         this      assignment,    you      will      practice          this      skill     by        writing           <strong>several           functions</strong>       that will      be        integrated      into     a          larger  software         product          provided        by        the      instructor.                  Along  the way     you      will      review basic   C++     programming and      Linux  file       management  skills   required         for       successful completion     of         CPE     212.

<h1>Project01 Overview</h1>

For      this      project,           you      will      <strong><em>complete</em></strong>        the      provided        partial C++     program         by        implementing <strong><em>six functions</em></strong>       that     perform          simple image  processing      operations      on        images            stored as        10×10, two dimensional   arrays of         integers.                     The     image  processing      operations      are:

<ul>

 <li>Get Next    Image</li>

 <li>Horizontal Flip</li>

 <li>Vertical Flip</li>

 <li>Transpose</li>

 <li>Rotate 90°      Clockwise</li>

 <li>Rotate 90°      Counter          Clockwise</li>

</ul>

You      must   implement     each    of         these   operations      as        a          C++     function.                     <strong><em>Your   code    for       the      six functions       above must   appear           in        the      file      named</em></strong>            <strong>project01.cpp</strong>          <strong><em>in        order  to        compile correctly.</em></strong>                   Remember,    spelling           and      capitalization count  in         Linux/C++.

The      function          <strong>main()</strong>           has      already           been    implemented for       you      to         provide           a          common         way for       everyone        to         test      their    code.                           The     function          <strong>main()</strong>           will      scan    a          sample input   file       and      perform          the      requested       series  of         image  processing      operations      by        invoking         your functions        as        needed.

Prototypes     for       the      six       functions        are      already           provided        for       you      in         <strong>main.cpp       (do      not            modify           main.cpp       !!!).                                         </strong><strong>All       program        output            is         performed    by        the            code   in        the      </strong><strong>main.cpp</strong><strong>       file      –          do       not      include          any     output            statements    in        the      file            </strong>            <strong>project01.cpp</strong><strong><em>          </em></strong>

<strong><em>The                                           interfaces    to        each    of         these  functions       you     must   write  are      described       in          detail  on       subsequent   pages and     in        the      prototypes     listed  within </em></strong><strong><em>main.cpp</em></strong><strong><em>       </em></strong>

<h1>Step #1 – Unzipping Project Materials on blackhawk</h1>

Use      the      Chrome/Firefox/Safari         browser          to         access Canvas            and      download       the      <strong>Project01_Materials.zip</strong> file       into     your    <strong>Project01</strong>      directory.                   At        terminal         window          prompt,          use      the      unzip  utility  to uncompress   the      files.                For      example,         to         unzip  the      files     into     your    current           directory:

<strong>unzip  Project01_Materials.zip </strong>

Since   this      project            is         worth  three   points, you      have    been    given   three   input   files     to         test      your    program.

<h1>Step #2 – Create Function Stubs for the Missing Support Functions</h1>

Open   a          Linux  terminal         window          and      navigate         to         the      directory        containing      the      <strong>Project01</strong> materials        downloaded   from    Canvas            (you    should be        there   already           if          you      just      completed      Step    #1 above).

Use      the      following        command       to         create the      file       <strong>project01.cpp          </strong>by        typing the      following        at         the Linux  prompt.                      Linux  is         case     sensitive         so        pay      attention        to         upper  versus lower  case     letters. <strong>gedit               project01.cpp                      &amp;         </strong>

This     command       starts  the      <strong>gedit</strong>   text     editor  running          as        a          background    process           (          <strong>&amp;</strong>         ).          With    the      editor  running          in         the      background,   you      may     use      the      same   terminal         window          to compile          and      test      your    program.                    Place   function          stubs   for       the      functions        listed   above  in the      file       <strong>project01.cpp          </strong>and      save    the      file.




In         the      terminal         window,         compile          your    program         by        typing the      word   <strong>make</strong>  at         the      prompt and      press   the      Enter   key.                 If         you      see      error   messages,       use      the      text     editor  to         make   corrections to         the      function          stubs   and      switch back    to         the      terminal         window          to         type    <strong>make</strong>  again   to recompile       your    program.                    Once   your    program         compiles,        you      may     execute           it          by        typing:                                                             <strong>./project01   inputfilename</strong><strong>       </strong>

Now    that     your    program         compiles         and      executes         using   function          stubs,  you      may     implement     and      test your    solution          function          by        function.                     Start    with    the      functions        associated      with    opening          files and      loading           data.

<strong>Running the Sample Solution on blackhawk [shows the desired output for specified input file] </strong><strong><em>The    best     description    of what   your    code    should            do        is         the      Sample           Solution         for       the      project.</em></strong>

Run     the      sample            solution          by        typing the      following        at         <strong>blackhawk</strong>    terminal         window          command prompt           where <strong>inputfilename</strong>     is         the      name   of         one      of         the      provided        input   files     (for     example, p01input1.txt).

<strong>/home/work/cpe212/project01/p01   inputfilename </strong>

è<strong>                    Your   current          working         directory       must   contain          the      input  files    for       this     to        work. </strong>ç<strong>        </strong>

<h1>Running the Preview Script on blackhawk [analyzes outputs for all provided input files]</h1>

Run     the      preview          script  by        typing the      following        in         a          <strong>blackhawk</strong>    terminal         window          command prompt

<strong>/home/work/cpe212data/project01/preview01.bash         </strong>

This     script  will      run      both    the      <strong>Sample           Solution</strong>         AND    your    <strong>project01</strong>      executable      program         on        the complete        set       of         input   files,    and      it          compares       the      outputs           of         the      two     programs       line      by line      to         identify           errors in         your    program’s      outputs.                      Make   sure    that     the      output of         your program         exactly            matches          the      output of         the      Sample           Solution.

<ul>

 <li><strong><em>To use      the      preview          script, your    executable     must   be        on       </em></strong><strong><em>blackhawk</em></strong><strong><em>    </em></strong></li>

 <li><strong><em>The sample           input  files     must   be        in        your    current          working         directory       BEFORE          you execute          the      preview          script!!!          </em></strong></li>

</ul>

<h1>Project01 Hints</h1>

Use      the      function          prototypes     appearing       in         <strong>main.cpp</strong>       to         create a          file       named <strong>project01.cpp</strong>          that contains          empty function          definitions.                 Be        sure    that     you      can      successfully    use      <strong><em>make</em></strong>  to         compile this      skeleton         solution          before adding any      additional       code.

The      <strong>GetNextImage</strong>          function          is         critical –          <strong>if         this     function         does   not      work, then    your   project will     fail      every  test</strong>.                Make   sure    that     <strong>GetNextImage</strong>          works before continuing      with    any      other   functions.

After    <strong>GetNextImage</strong>,         implement     the      simplest         operations      <strong>FlipHorizontal,        FlipVertical, </strong>and<strong>      Transpose</strong>     <strong><em>one at        a          time</em></strong>,   testing each    with    the      appropriate    input   file.                  Rotations        may     be        implemented by combinations of         the      three   simplest         operations.

struct Record   // Structured data type for storing one line of image data from file

{     int digit;                          // Digit read from file     int image[MAXROWS][MAXCOLS];        // Pixel data read from file };

<strong>Project 01 Function Specifications </strong>void GetNextImage(ifstream&amp; datastream, int counters[], Record&amp; data)

// Reads digit and image data from datastream object storing values in data parameter

// Updates histogram counters to reflect specific digit input from file

// Note: Correct operation of this function is critical!!  If one cannot correctly //       load images into the array from the file, then one cannot test the  //       image processing operations and your code will fail every test!




void Transpose(int image[MAXROWS][MAXCOLS]);

// Transpose() – must flip the image across the primary diagonal row = column as // with a matrix transpose

// Parameter image is a two-dimensional array of integers representing the image




void FlipHorizontal(int image[MAXROWS][MAXCOLS]);

// FlipHorizontal() – must flip the image horizontally.  For example,

// column zero exchanged with column N-1, column one exchanged with column N-2, etc.

// Parameter image is a two-dimensional array of integers representing the image




void FlipVertical(int image[MAXROWS][MAXCOLS]);

// FlipVertical() – must flip the image Vertically.  For example,

// row zero exchanged with row N-1, row one exchanged with row N-2, etc.

// Parameter image is a two-dimensional array of integers representing the image

void RotateCW(int image[MAXROWS][MAXCOLS]);

// RotateCW() – must rotate the image 90 degrees clockwise.

// Parameter image is a two-dimensional array of integers representing the image

void RotateCCW(int image[MAXROWS][MAXCOLS]);

// RotateCCW() – must rotate the image 90 degrees counter clockwise.

// Parameter image is a two-dimensional array of integers representing the image <strong>Hint:                       Rotations      may    be        achieved        by combining    the      other  operations.   </strong>

<h1>Project01 Sample Input File  (p01input1.txt)</h1>




<table width="713">

 <tbody>

  <tr>

   <td colspan="4" width="336"><strong>#          p01input1.txt           —         Test    of            Transpose     Image </strong></td>

   <td rowspan="2" width="48"><strong>            </strong></td>

   <td rowspan="2" width="48"><strong>            </strong></td>

   <td rowspan="2" width="281">ç<strong>        #          designates    a            comment</strong><strong>       </strong></td>

  </tr>

  <tr>

   <td width="192"><strong>            </strong></td>

   <td width="48"> </td>

   <td width="48"> </td>

   <td width="48"> </td>

  </tr>

  <tr>

   <td width="192"><strong>[                                                          smalldata.csv                                                </strong><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="281">ç<strong>        Open  specified       image data            file</strong><strong>      </strong></td>

  </tr>

  <tr>

   <td width="192"><strong>#                             Draw                                Bars                                                        </strong><strong>b                      1          </strong><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="281">ç<strong>        b          designates    drawbar            command</strong><strong>      </strong></td>

  </tr>

  <tr>

   <td width="192"><strong>#          Print   Original            Image p          </strong><strong>            </strong><strong>#          Draw            Bars            b                      1          </strong><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="281">ç<strong>        p          designates    print            image command</strong><strong>      </strong></td>

  </tr>

  <tr>

   <td width="192"><strong>#          Test    Transpose            Image t           </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="48"><strong>            </strong></td>

   <td width="281">ç<strong>        t           designates    transpose            command</strong><strong>      </strong></td>

  </tr>

 </tbody>

</table>

<strong>            </strong>

<strong>#          Print   Image p          </strong>

<strong>            </strong>

<strong>#          Close  file      </strong>

<strong>]                                   </strong>

<strong>            </strong>

<h1>One Line from Data File  (smalldata.csv)     (first integer is digit depicted by pixels – 24×24 array)</h1>

<strong>            </strong>

<strong>7</strong><strong>,</strong><strong>0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,</strong>

<strong>0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,</strong>

<strong>0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,</strong>

<strong>0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,84,185,159,151,60,36,0,</strong>

<strong>0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,222,254,254,254,254,241,198,198,198,198,198,198,198,19</strong>

<strong>8,170,52,0,0,0,0,0,0,0,0,0,0,0,0,67,114,72,114,163,227,254,225,254,254,254,250,229,254,254,140</strong>

<strong>,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,17,66,14,67,67,67,59,21,236,254,106,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0, 0,0,0,0,0,0,0,0,83,253,209,18,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,22,233,255,83,0,0,0,0,0,0,0</strong>

<strong>,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,129,254,238,44,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,59,249,2</strong>

<strong>54,62,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,133,254,187,5,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0</strong>

<strong>,0,0,0,0,9,205,248,58,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,126,254,182,0,0,0,0,0,0,0,0,0,0,0,</strong>

<strong>0,0,0,0,0,0,0,0,0,0,0,0,0,75,251,240,57,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,19,221,254,166,0, 0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,3,203,254,219,35,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,</strong>

<strong>0,38,254,254,77,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,31,224,254,115,1,0,0,0,0,0,0,0,0,0,0,0,0,</strong>

<strong>0,0,0,0,0,0,0,0,0,0,0,133,254,254,52,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,61,242,254,254,52,0</strong>

<strong>,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,121,254,254,219,40,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0</strong>

<strong>,0,0,121,254,207,18,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0</strong><strong>     </strong>