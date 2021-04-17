---
description: Más información acerca de los archivos del motor de almacenamiento extensible
title: Archivos del motor de almacenamiento extensible
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: c27bb0104c5923496c5dd7962ef4a9bacdc90af4
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717453"
---
# <a name="extensible-storage-engine-files"></a><span data-ttu-id="bb4de-103">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="bb4de-103">Extensible Storage Engine Files</span></span>


<span data-ttu-id="bb4de-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bb4de-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-files"></a><span data-ttu-id="bb4de-105">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="bb4de-105">Extensible Storage Engine Files</span></span>

<span data-ttu-id="bb4de-106">El motor de almacenamiento extensible usa los siguientes tipos de archivos:</span><span class="sxs-lookup"><span data-stu-id="bb4de-106">The Extensible Storage Engine uses the following types of files:</span></span>

- [<span data-ttu-id="bb4de-107">Archivos de registro de transacciones</span><span class="sxs-lookup"><span data-stu-id="bb4de-107">Transaction Log Files</span></span>](#transaction-log-files)

- [<span data-ttu-id="bb4de-108">Archivos de registro de transacciones temporales</span><span class="sxs-lookup"><span data-stu-id="bb4de-108">Temporary Transaction Log Files</span></span>](#temporary-transaction-log-files)

- [<span data-ttu-id="bb4de-109">Archivos de registro de transacciones reservados</span><span class="sxs-lookup"><span data-stu-id="bb4de-109">Reserved Transaction Log Files</span></span>](#reserved-transaction-log-files)

- [<span data-ttu-id="bb4de-110">Archivos de puntos de control</span><span class="sxs-lookup"><span data-stu-id="bb4de-110">Checkpoint Files</span></span>](#checkpoint-files)

- [<span data-ttu-id="bb4de-111">Archivos de la base de datos</span><span class="sxs-lookup"><span data-stu-id="bb4de-111">Database Files</span></span>](#database-files)

- [<span data-ttu-id="bb4de-112">Bases de datos temporales</span><span class="sxs-lookup"><span data-stu-id="bb4de-112">Temporary Databases</span></span>](#temporary-databases)

- [<span data-ttu-id="bb4de-113">Vaciar archivos de asignación</span><span class="sxs-lookup"><span data-stu-id="bb4de-113">Flush Map Files</span></span>](#flush-map-files)

<span data-ttu-id="bb4de-114">Esta tabla contiene información general de los nombres de los archivos de datos administrados por ESE.</span><span class="sxs-lookup"><span data-stu-id="bb4de-114">This table contains an overview of the data file names that are managed by ESE.</span></span> <span data-ttu-id="bb4de-115">En Windows Vista y versiones posteriores, el valor JET_paramLegacyNames afecta a los nombres de archivo que se usan.</span><span class="sxs-lookup"><span data-stu-id="bb4de-115">For Windows Vista and later, the JET_paramLegacyNames setting impacts the file names that are used.</span></span>

<table xmlns="https://www.w3.org/1999/xhtml">
  <tr>
    <th>
      <p><span data-ttu-id="bb4de-116">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bb4de-116">Operating System</span></span></p>
    </th>
    <th>
      <p><span data-ttu-id="bb4de-117">Windows Server 2003 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="bb4de-117">Windows Server 2003 and earlier</span></span><br /><br /></p>
    </th>
    <th colspan="2">
      <p></p>
      <p><span data-ttu-id="bb4de-118">Windows Vista y versiones posteriores (cliente)</span><span class="sxs-lookup"><span data-stu-id="bb4de-118">Windows Vista and later (client)</span></span> <br />
<span data-ttu-id="bb4de-119">Windows Server 2008 y versiones posteriores (servidor)</span><span class="sxs-lookup"><span data-stu-id="bb4de-119">Windows Server 2008 and later (server)</span></span>
</p>
    </th>
    <th>
      <p><span data-ttu-id="bb4de-120">Actualización de aniversario de Windows 10 y versiones posteriores (cliente)</span><span class="sxs-lookup"><span data-stu-id="bb4de-120">Windows 10 Anniversary Update and later (client)</span></span> <br />
<span data-ttu-id="bb4de-121">Windows Server 2016 y versiones posteriores (servidor)</span><span class="sxs-lookup"><span data-stu-id="bb4de-121">Windows Server 2016 and later (server)</span></span>
</p>
    </th>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="bb4de-122">
        <strong>JET_paramLegacyNames configuración</strong>
      </span><span class="sxs-lookup"><span data-stu-id="bb4de-122">
        <strong>JET_paramLegacyNames setting</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-123">
        <strong>N/A</strong>
      </span><span class="sxs-lookup"><span data-stu-id="bb4de-123">
        <strong>N/A</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-124">
        <strong>Ninguna</strong>
      </span><span class="sxs-lookup"><span data-stu-id="bb4de-124">
        <strong>None</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-125">
        <strong>JET_bitESE98FileNames</strong>
      </span><span class="sxs-lookup"><span data-stu-id="bb4de-125">
        <strong>JET_bitESE98FileNames</strong>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-126">
        <strong>Igual que Windows Vista/servidor 2008</strong>
      </span><span class="sxs-lookup"><span data-stu-id="bb4de-126">
        <strong>Same as Windows Vista/Server 2008</strong>
      </span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="bb4de-127">Registro actual</span><span class="sxs-lookup"><span data-stu-id="bb4de-127">Current Log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-128">&lt;INST &gt; . log</span><span class="sxs-lookup"><span data-stu-id="bb4de-128">&lt;inst&gt;.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-129">&lt;INST &gt; . JTX</span><span class="sxs-lookup"><span data-stu-id="bb4de-129">&lt;inst&gt;.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-130">&lt;INST &gt; . log</span><span class="sxs-lookup"><span data-stu-id="bb4de-130">&lt;inst&gt;.log</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="bb4de-131">Registro previo a la inicialización</span><span class="sxs-lookup"><span data-stu-id="bb4de-131">Pre-Init Log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-132">&lt;INST &gt; . log tmp</span><span class="sxs-lookup"><span data-stu-id="bb4de-132">&lt;inst&gt;tmp.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-133">&lt;INST &gt; tmp. JTX</span><span class="sxs-lookup"><span data-stu-id="bb4de-133">&lt;inst&gt;tmp.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-134">&lt;INST &gt; . log tmp</span><span class="sxs-lookup"><span data-stu-id="bb4de-134">&lt;inst&gt;tmp.log</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="bb4de-135">Registros girados</span><span class="sxs-lookup"><span data-stu-id="bb4de-135">Rotated Logs</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-136">&lt;INST &gt; . log</span><span class="sxs-lookup"><span data-stu-id="bb4de-136">&lt;inst&gt;XXXXX.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-137">&lt;INST &gt; . JTX después de FFFFF cambie a &lt; inst &gt; xxxxxxxx. JTX</span><span class="sxs-lookup"><span data-stu-id="bb4de-137">&lt;inst&gt;XXXXX.jtx after FFFFF switch to &lt;inst&gt;XXXXXXXX.jtx</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-138">&lt;Inst. &gt; log después de FFFFF cambie a &lt; inst &gt; xxxxxxxx. log.</span><span class="sxs-lookup"><span data-stu-id="bb4de-138">&lt;inst&gt;XXXXX.log after FFFFF switch to &lt;inst&gt;XXXXXXXX.log.</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="bb4de-139">
        <a href="gg294069(v=exchg.10).md">Archivos de punto de comprobación</a>
      </span><span class="sxs-lookup"><span data-stu-id="bb4de-139">
        <a href="gg294069(v=exchg.10).md">Checkpoint Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-140">&lt;INST &gt; . chk</span><span class="sxs-lookup"><span data-stu-id="bb4de-140">&lt;inst&gt;.chk</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-141">&lt;INST &gt; . JCP</span><span class="sxs-lookup"><span data-stu-id="bb4de-141">&lt;inst&gt;.jcp</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-142">&lt;INST &gt; . chk</span><span class="sxs-lookup"><span data-stu-id="bb4de-142">&lt;inst&gt;.chk</span></span></p>
    </td>
    <td rowspan="2"></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="bb4de-143">
        <a href="gg294069(v=exchg.10).md">Bases de datos temporales</a>
      </span><span class="sxs-lookup"><span data-stu-id="bb4de-143">
        <a href="gg294069(v=exchg.10).md">Temporary Databases</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-144">&lt;Temp. edb del nombre de archivo de la base de archivos temporal &gt; : tmp. edb</span><span class="sxs-lookup"><span data-stu-id="bb4de-144">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-145">&lt;Temp. edb del nombre de archivo de la base de archivos temporal &gt; : tmp. edb</span><span class="sxs-lookup"><span data-stu-id="bb4de-145">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-146">&lt;Temp. edb del nombre de archivo de la base de archivos temporal &gt; : tmp. edb</span><span class="sxs-lookup"><span data-stu-id="bb4de-146">&lt;temp db file name&gt; Default: tmp.edb</span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="bb4de-147">
        <a href="gg294069(v=exchg.10).md">Archivos de registro de transacciones reservados</a>
      </span><span class="sxs-lookup"><span data-stu-id="bb4de-147">
        <a href="gg294069(v=exchg.10).md">Reserved Transaction Log Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-148">res1. log &amp; Res2. log</span><span class="sxs-lookup"><span data-stu-id="bb4de-148">res1.log &amp; res2.log</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-149">&lt;INST &gt; RESXXXXX. JRS</span><span class="sxs-lookup"><span data-stu-id="bb4de-149">&lt;inst&gt;RESXXXXX.jrs</span></span></p>
    </td>
    <td colspan="2">
      <p><span data-ttu-id="bb4de-150">&lt;INST &gt; RESXXXXX. JRS</span><span class="sxs-lookup"><span data-stu-id="bb4de-150">&lt;inst&gt;RESXXXXX.jrs</span></span></p>
    </td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="bb4de-151">
        <a href="gg294069(v=exchg.10).md">Archivos de base de datos</a>
      </span><span class="sxs-lookup"><span data-stu-id="bb4de-151">
        <a href="gg294069(v=exchg.10).md">Database Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-152">&lt;nombre de archivo de base de archivos&gt;</span><span class="sxs-lookup"><span data-stu-id="bb4de-152">&lt;db file name&gt;</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-153">&lt;nombre de archivo de base de archivos&gt;</span><span class="sxs-lookup"><span data-stu-id="bb4de-153">&lt;db file name&gt;</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-154">&lt;nombre de archivo de base de archivos&gt;</span><span class="sxs-lookup"><span data-stu-id="bb4de-154">&lt;db file name&gt;</span></span></p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p><span data-ttu-id="bb4de-155">
        <a href="gg294069(v=exchg.10).md">Vaciar archivos de asignación</a>
      </span><span class="sxs-lookup"><span data-stu-id="bb4de-155">
        <a href="gg294069(v=exchg.10).md">Flush Map Files</a>
      </span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-156">N/D</span><span class="sxs-lookup"><span data-stu-id="bb4de-156">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-157">N/D</span><span class="sxs-lookup"><span data-stu-id="bb4de-157">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-158">N/D</span><span class="sxs-lookup"><span data-stu-id="bb4de-158">N/A</span></span></p>
    </td>
    <td>
      <p><span data-ttu-id="bb4de-159">&lt;nombre de archivo de base de archivo sin extensión &gt; . JFM</span><span class="sxs-lookup"><span data-stu-id="bb4de-159">&lt;db file name without extension&gt;.jfm</span></span></p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a><span data-ttu-id="bb4de-160">Archivos de registro de transacciones</span><span class="sxs-lookup"><span data-stu-id="bb4de-160">Transaction Log Files</span></span>

<span data-ttu-id="bb4de-161">Los archivos de registro de transacciones contienen operaciones en archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="bb4de-161">Transaction log files contain operations on database files.</span></span> <span data-ttu-id="bb4de-162">Contienen información suficiente para poner una base de datos a un estado coherente lógicamente después de una terminación de proceso inesperada o un cierre del sistema.</span><span class="sxs-lookup"><span data-stu-id="bb4de-162">They contain enough information to bring a database to a logically consistent state after an unexpected process termination or system shutdown.</span></span>

<span data-ttu-id="bb4de-163">Los nombres de los archivos de registro dependen de un nombre base de tres letras, que se puede establecer con [JET_paramBaseName](./transaction-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bb4de-163">The names of the log files are dependent on a three-letter base name, which can be set with [JET_paramBaseName](./transaction-log-parameters.md).</span></span> <span data-ttu-id="bb4de-164">En los ejemplos siguientes se usa un nombre base de "edb", ya que es el nombre base predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bb4de-164">The examples below use a base name of "edb", because that is the default base name.</span></span> <span data-ttu-id="bb4de-165">La extensión de los archivos de registro de transacciones será. log o. JTX, dependiendo de si el JET_bitESE98FileNames se establece en el parámetro JET_paramLegacyFileNames.</span><span class="sxs-lookup"><span data-stu-id="bb4de-165">The extension for the transaction log files will be either .log or .jtx depending upon whether the JET_bitESE98FileNames is set in the JET_paramLegacyFileNames parameter.</span></span> <span data-ttu-id="bb4de-166">Para obtener más información, vea [parámetros del sistema del motor de almacenamiento extensible](./extensible-storage-engine-system-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bb4de-166">For more information, see [Extensible Storage Engine System Parameters](./extensible-storage-engine-system-parameters.md).</span></span>

<span data-ttu-id="bb4de-167">Los archivos de registro de transacciones se denominan \<base\> \<generation-number\> . log, comenzando por 1.</span><span class="sxs-lookup"><span data-stu-id="bb4de-167">Transaction log files are named \<base\>\<generation-number\>.log, beginning with 1.</span></span> <span data-ttu-id="bb4de-168">El número de generación de registro está en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="bb4de-168">The log generation number is in hexadecimal format.</span></span> <span data-ttu-id="bb4de-169">Por ejemplo, edb00001. log es el primer registro y edb000ff. log es el registro 255th.</span><span class="sxs-lookup"><span data-stu-id="bb4de-169">For example, edb00001.log is the first log, and edb000ff.log is the 255th log.</span></span> <span data-ttu-id="bb4de-170">Los archivos de registro tienen cinco dígitos hexadecimales en el nombre del archivo de registro, hasta el archivo de registro 1048576th, momento en el que los archivos de registro empiezan a denominarse en un formato 11,3 (por ejemplo, edb00100000. log).</span><span class="sxs-lookup"><span data-stu-id="bb4de-170">The log files have five hexadecimal digits in the log file name, until the 1048576th log file, at which point the log files start being named in an 11.3 format (for example, edb00100000.log).</span></span> <span data-ttu-id="bb4de-171">\<base\>. log siempre es el archivo de registro que se está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="bb4de-171">\<base\>.log is always the log file that is currently being used.</span></span> <span data-ttu-id="bb4de-172">Si el motor de base de datos no está activo, la generación de edb. log puede identificarse con el siguiente comando: **esentutl.exe-ml EDB. log**.</span><span class="sxs-lookup"><span data-stu-id="bb4de-172">If the database engine is not active, the generation of edb.log can be identified using the following command: **esentutl.exe -ml edb.log**.</span></span>

<span data-ttu-id="bb4de-173">Aunque los archivos de registro de transacciones tienen el. Extensión de registro asociada normalmente a archivos de texto, los archivos de registro de transacciones están en formato binario y nunca deben ser editados por un usuario. Las operaciones de base de datos se escriben primero en el registro.</span><span class="sxs-lookup"><span data-stu-id="bb4de-173">Although transaction log files have the .LOG extension commonly associated with text files, transaction log files are in a binary format and should never be edited by a user.Database operations are written to the log first.</span></span> <span data-ttu-id="bb4de-174">Los datos se pueden escribir más adelante en el archivo de base de datos. posiblemente de inmediato, posiblemente más tarde.</span><span class="sxs-lookup"><span data-stu-id="bb4de-174">The data can be written to the database file later; possibly immediately, potentially much later.</span></span> <span data-ttu-id="bb4de-175">En caso de que se produzca un proceso inesperado o una terminación del sistema, las operaciones seguirán presentes en los archivos de registro y se pueden revertir las transacciones incompletas.</span><span class="sxs-lookup"><span data-stu-id="bb4de-175">In the event of unexpected process or system termination, the operations are still present in the log files, and incomplete transactions can be rolled back.</span></span> <span data-ttu-id="bb4de-176">La acción de reproducir archivos de registro de transacciones se denomina *recuperación de software* y se realiza automáticamente cuando se llama a [JetInit](./jetinit-function.md) o [JetInit2](./jetinit2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="bb4de-176">The act of replaying transaction log files is called *soft recovery*, and it is done automatically when [JetInit](./jetinit-function.md) or [JetInit2](./jetinit2-function.md) is called.</span></span> <span data-ttu-id="bb4de-177">La recuperación de software también puede realizarse manualmente con la opción "-r" del programa Esentutl.exe.</span><span class="sxs-lookup"><span data-stu-id="bb4de-177">Soft recovery can also be performed manually with the "-r" option of the Esentutl.exe program.</span></span> <span data-ttu-id="bb4de-178">La acción de reproducir archivos de registro de transacciones en una base de datos restaurada a partir de una copia de seguridad se denomina *recuperación de hardware*.</span><span class="sxs-lookup"><span data-stu-id="bb4de-178">The act of replaying transaction log files on a database that is restored from a backup is called *hard recovery*.</span></span>

<span data-ttu-id="bb4de-179">Los archivos de registro tienen un tamaño fijo, personalizable con [JET_paramLogFileSize](./transaction-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bb4de-179">Log files are of a fixed size, customizable with [JET_paramLogFileSize](./transaction-log-parameters.md).</span></span> <span data-ttu-id="bb4de-180">Cuando se rellena el archivo de registro actual (es decir, EDB. log), se le cambia el nombre a \<base\> \<generation-number\> . log y se necesita un nuevo archivo de registro de transacciones en la secuencia del registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="bb4de-180">When the current log file (that is, edb.log) gets filled, it gets renamed to \<base\>\<generation-number\>.log, and a new transaction log file is needed in the transaction log stream.</span></span>

<span data-ttu-id="bb4de-181">Cada instancia de base de datos tiene asociada una única secuencia de archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="bb4de-181">Each database instance has a single log file sequence associated with it.</span></span> <span data-ttu-id="bb4de-182">Windows XP presentó [JetCreateInstance](./jetcreateinstance-function.md), lo que permite usar varias secuencias de archivos de registro de transacciones en un único proceso.</span><span class="sxs-lookup"><span data-stu-id="bb4de-182">Windows XP introduced [JetCreateInstance](./jetcreateinstance-function.md), allowing multiple transaction log file sequences to be used by a single process.</span></span> <span data-ttu-id="bb4de-183">Sin embargo, no pueden existir varias secuencias de archivo de registro de transacciones en el mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="bb4de-183">Multiple transaction log file sequences cannot exist in the same directory, however.</span></span>

<span data-ttu-id="bb4de-184">Los archivos de registro de transacciones nunca deben manipularse, cambiarse de nombre, moverse o eliminarse de forma manual, ya que pueden producirse daños en los datos.</span><span class="sxs-lookup"><span data-stu-id="bb4de-184">Transaction log files should almost never be manually manipulated, renamed, moved, or deleted because data corruption can result.</span></span>

<span data-ttu-id="bb4de-185">El motor de base de datos eliminará los archivos de registro de transacciones durante una copia de seguridad completa (vea [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)), o durante las operaciones normales, si está habilitado el registro circular.</span><span class="sxs-lookup"><span data-stu-id="bb4de-185">Transaction log files will be deleted by the database engine during a full backup (see [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)), or during normal operations, if circular logging is enabled.</span></span>

<span data-ttu-id="bb4de-186">Una vez que se llena un archivo de registro de transacciones, el motor de base de datos debe crear un nuevo archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="bb4de-186">After a transaction log file is filled up, the database engine needs to create a new log file.</span></span> <span data-ttu-id="bb4de-187">El registro circular es un medio por el que el motor de base de datos puede limpiar automáticamente los archivos de registro cuando ya no son necesarios para la recuperación tras bloqueo.</span><span class="sxs-lookup"><span data-stu-id="bb4de-187">Circular logging is a means by which log files can be automatically cleaned up by the database engine when they are no longer required for crash recovery.</span></span> <span data-ttu-id="bb4de-188">Este proceso es una alternativa a la eliminación de archivos de registro como un producto de la realización de una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="bb4de-188">This process is an alternative to removing log files as a by-product of performing a backup.</span></span> <span data-ttu-id="bb4de-189">El registro circular se puede controlar con el parámetro del sistema [JET_paramCircularLog](./transaction-log-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="bb4de-189">Circular logging can be controlled with the [JET_paramCircularLog](./transaction-log-parameters.md) system parameter.</span></span> <span data-ttu-id="bb4de-190">Los archivos de registro de transacciones no se deben eliminar con ningún otro método.</span><span class="sxs-lookup"><span data-stu-id="bb4de-190">Transaction log files should not be deleted using any other method.</span></span>

### <a name="temporary-transaction-log-files"></a><span data-ttu-id="bb4de-191">Archivos de registro de transacciones temporales</span><span class="sxs-lookup"><span data-stu-id="bb4de-191">Temporary Transaction Log Files</span></span>

<span data-ttu-id="bb4de-192">Cuando se llena EDB. log, ESE debe crear un nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="bb4de-192">When edb.log fills up, ESE needs to create a new file.</span></span> <span data-ttu-id="bb4de-193">El nuevo archivo de transacción de registro se conoce como archivo de registro de transacciones temporal antes de que lo use ESE.</span><span class="sxs-lookup"><span data-stu-id="bb4de-193">The new log transaction file is known as a temporary transaction log file prior to its use by ESE.</span></span>

<span data-ttu-id="bb4de-194">Mientras se crea un nuevo archivo de registro y su tamaño se extiende, se denominará \<base\> tmp. log.</span><span class="sxs-lookup"><span data-stu-id="bb4de-194">While a new log file is created and its size extended, it will be called \<base\>tmp.log.</span></span> <span data-ttu-id="bb4de-195">La creación de un nuevo archivo puede ser una operación potencialmente costosa, por lo que ESE creará el siguiente archivo de registro de forma proactiva como una tarea en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="bb4de-195">Creating a new file can be a potentially costly operation, so ESE will create the next log file proactively as a background task.</span></span>

<span data-ttu-id="bb4de-196">Dado que el archivo de registro de transacciones temporal se crea en previsión de necesidad de un nuevo archivo de registro de transacciones, no contiene ninguna información útil.</span><span class="sxs-lookup"><span data-stu-id="bb4de-196">Because the temporary transaction log file is created in anticipation of need for a new transaction log file, it does not contain any useful information.</span></span>

### <a name="reserved-transaction-log-files"></a><span data-ttu-id="bb4de-197">Archivos de registro de transacciones reservados</span><span class="sxs-lookup"><span data-stu-id="bb4de-197">Reserved Transaction Log Files</span></span>

<span data-ttu-id="bb4de-198">Los archivos de registro de transacciones reservados se crean cuando el motor comienza a permitir que se registren operaciones importantes para obtener un cierre correcto.</span><span class="sxs-lookup"><span data-stu-id="bb4de-198">The reserved transaction log files are created when the engine starts to allow important operations to be logged to get a clean shutdown.</span></span>

<span data-ttu-id="bb4de-199">**Windows Vista:** En Windows Vista y versiones posteriores, los archivos de registro de transacciones reservados se denominan \<base\> RESXXXXX. JRS.</span><span class="sxs-lookup"><span data-stu-id="bb4de-199">**Windows Vista:** In Windows Vista and later, the Reserved Transaction Log Files are named \<base\>RESXXXXX.jrs.</span></span>

<span data-ttu-id="bb4de-200">**Windows Server 2003:** En Windows Server 2003 y versiones anteriores, los archivos de registro de transacciones reservados se denominan res1. log y Res2. log.</span><span class="sxs-lookup"><span data-stu-id="bb4de-200">**Windows Server 2003:** In Windows Server 2003 and earlier, The Reserved Transaction Log Files are named res1.log and res2.log.</span></span>

<span data-ttu-id="bb4de-201">Cuando el motor de base de datos se queda sin espacio en disco, no puede crear un nuevo archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="bb4de-201">When the database engine runs out of disk space it cannot create a new log file.</span></span> <span data-ttu-id="bb4de-202">Lo más seguro es cerrar sin problemas, pero es necesario registrar algunas operaciones (como las operaciones de reversión).</span><span class="sxs-lookup"><span data-stu-id="bb4de-202">The safest thing to do is to shut down cleanly, but some operations (such as rollback operations) must still be logged.</span></span> <span data-ttu-id="bb4de-203">La mayoría de las operaciones de base de datos producirán errores durante esta fase.</span><span class="sxs-lookup"><span data-stu-id="bb4de-203">Most database operations will fail during this stage.</span></span>

<span data-ttu-id="bb4de-204">Dado que los archivos de registro de transacciones reservados se crean en previsión de necesidad de archivos de registro de transacciones en un escenario fuera de disco, no contienen ninguna información útil.</span><span class="sxs-lookup"><span data-stu-id="bb4de-204">Because the reserved transaction log files are created in anticipation of need for transaction log files in an out-of-disk scenario, they do not contain any useful information.</span></span>

### <a name="checkpoint-files"></a><span data-ttu-id="bb4de-205">punto de comprobación, archivos</span><span class="sxs-lookup"><span data-stu-id="bb4de-205">Checkpoint Files</span></span>

<span data-ttu-id="bb4de-206">El archivo de punto de comprobación almacena el punto de control para una secuencia de archivo de registro de transacciones determinada.</span><span class="sxs-lookup"><span data-stu-id="bb4de-206">The checkpoint file stores the checkpoint for a particular transaction log file sequence.</span></span> <span data-ttu-id="bb4de-207">El archivo de punto de comprobación se denomina \<base\> . chk o \<base\> . JCP, dependiendo de si el JET_bitESE98FileNames se establece en el parámetro JET_paramLegacyFileNames y [JET_paramSystemPath](./transaction-log-parameters.md)proporciona su ubicación.</span><span class="sxs-lookup"><span data-stu-id="bb4de-207">The checkpoint file is named \<base\>.chk or \<base\>.jcp, depending upon whether the JET_bitESE98FileNames is set in the JET_paramLegacyFileNames parameter, and its location is given by [JET_paramSystemPath](./transaction-log-parameters.md).</span></span>

<span data-ttu-id="bb4de-208">Las operaciones de base de datos se escriben primero en los archivos de registro y, a continuación, se almacenan en la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="bb4de-208">Database operations are first written to the log files and then cached in memory.</span></span> <span data-ttu-id="bb4de-209">En algún momento posterior, las operaciones se escriben en el archivo de base de datos, pero por razones de rendimiento, el orden en el que se escriben las operaciones en el archivo de base de datos podría no coincidir con el orden en el que se registraron originalmente.</span><span class="sxs-lookup"><span data-stu-id="bb4de-209">At some later point, the operations get written to the database file, but for performance reasons, the order in which operations are written to the database file might not match the order in which they were originally logged.</span></span> <span data-ttu-id="bb4de-210">Las operaciones escritas en el archivo de registro de transacciones estarán en uno de estos dos Estados:</span><span class="sxs-lookup"><span data-stu-id="bb4de-210">Operations written to the transaction log file will be in one of two states:</span></span>

  - <span data-ttu-id="bb4de-211">Se escriben en el archivo de registro de transacciones y en el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="bb4de-211">Written to the transaction log file and the database file.</span></span>

  - <span data-ttu-id="bb4de-212">Se escribe en el archivo de registro de transacciones y aún no se ha escrito en el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="bb4de-212">Written to the transaction log file and not yet written to the database file.</span></span>

<span data-ttu-id="bb4de-213">Muchas operaciones de base de datos se pueden almacenar en un único archivo de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="bb4de-213">Many database operations can be stored in a single transaction log file.</span></span> <span data-ttu-id="bb4de-214">Un archivo de registro determinado puede estar formado por los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="bb4de-214">A given log file can consist of the following items:</span></span>

  - <span data-ttu-id="bb4de-215">Todas las operaciones escritas en el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="bb4de-215">All operations written to the database file.</span></span>

  - <span data-ttu-id="bb4de-216">No se han escrito operaciones en el archivo de base de datos</span><span class="sxs-lookup"><span data-stu-id="bb4de-216">No operations written to the database file</span></span>

  - <span data-ttu-id="bb4de-217">Combinación de operaciones escritas en el archivo de base de datos y operaciones que todavía no se han escrito en el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="bb4de-217">A mix of operations written to the database file and operations not yet written to the database file.</span></span>

<span data-ttu-id="bb4de-218">El punto de control hace referencia al punto en el tiempo en la secuencia del registro de transacciones, donde todas las operaciones anteriores al punto de control se han escrito en el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="bb4de-218">The checkpoint refers to the point in time in the transaction log stream where all operations prior to the checkpoint have been written to the database file.</span></span> <span data-ttu-id="bb4de-219">No hay ninguna garantía sobre las operaciones que se producen después del punto de control; algunos pueden estar en memoria y otros pueden escribirse en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="bb4de-219">There is no guarantee about the operations that occur after the checkpoint; some might be in memory, and some might be written to the database.</span></span>

<span data-ttu-id="bb4de-220">Dado que todas las operaciones en los archivos de registro antes del punto de control se representan en el archivo de base de datos, solo se necesitan los archivos de registro de transacciones después del punto de control para que la recuperación de software Ponga una base de datos determinada en un estado limpio.</span><span class="sxs-lookup"><span data-stu-id="bb4de-220">Since all the operations in the log files prior to the checkpoint are represented in the database file, only the transaction log files after the checkpoint are needed for soft recovery to bring a particular database into a clean state.</span></span>

### <a name="database-files"></a><span data-ttu-id="bb4de-221">Archivos de la base de datos</span><span class="sxs-lookup"><span data-stu-id="bb4de-221">Database Files</span></span>

<span data-ttu-id="bb4de-222">El archivo de base de datos contiene el esquema de todas las tablas de la base de datos, los registros de todas las tablas de la base de datos y los índices de las tablas.</span><span class="sxs-lookup"><span data-stu-id="bb4de-222">The database file contains the schema for all of the tables in the database, the records for all of the tables in the database, and the indexes over the tables.</span></span> <span data-ttu-id="bb4de-223">Su ubicación se proporciona con [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md)o [JetAttachDatabase2](./jetattachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="bb4de-223">Its location is given using [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md), or [JetAttachDatabase2](./jetattachdatabase2-function.md).</span></span>

<span data-ttu-id="bb4de-224">Una base de datos se cierra correctamente solo después de una llamada correcta a [JetTerm](./jetterm-function.md) o [JetTerm2](./jetterm2-function.md).</span><span class="sxs-lookup"><span data-stu-id="bb4de-224">A database is cleanly shut down only after a successful call to [JetTerm](./jetterm-function.md) or [JetTerm2](./jetterm2-function.md).</span></span>

<span data-ttu-id="bb4de-225">El programa Esentutl.exe puede detectar si una base de datos se cierra correctamente con la opción "-MH".</span><span class="sxs-lookup"><span data-stu-id="bb4de-225">The Esentutl.exe program can detect whether a database is shut down cleanly with the "-mh" option.</span></span> <span data-ttu-id="bb4de-226">Por ejemplo, "esentutl.exe-AG sample. edb" leerá el encabezado de la base de datos de una base de datos denominada sample. edb e imprimirá el estado de sample. edb.</span><span class="sxs-lookup"><span data-stu-id="bb4de-226">For example, "esentutl.exe -mh sample.edb" will read the database header of a database named sample.edb, and print out the state of sample.edb.</span></span> <span data-ttu-id="bb4de-227">Puede imprimir "estado: cierre correcto" o "estado: cierre con errores".</span><span class="sxs-lookup"><span data-stu-id="bb4de-227">It may print out "State: Clean Shutdown" or "State: Dirty Shutdown".</span></span>

<span data-ttu-id="bb4de-228">Una base de datos que no se ha cerrado correctamente se encuentra en un estado de cierre con errores.</span><span class="sxs-lookup"><span data-stu-id="bb4de-228">A database that has not been cleanly shut down is in a dirty shutdown state.</span></span> <span data-ttu-id="bb4de-229">Antes de Windows XP, este estado se llamaba *incoherente*.</span><span class="sxs-lookup"><span data-stu-id="bb4de-229">Prior to Windows XP, this state was called *inconsistent*.</span></span> <span data-ttu-id="bb4de-230">Una base de datos desfasada (incoherente) se puede trasladar a un estado limpio con recuperación de software.</span><span class="sxs-lookup"><span data-stu-id="bb4de-230">A dirty (inconsistent) database can be brought to a clean state with soft recovery.</span></span> <span data-ttu-id="bb4de-231">Una base de datos dañada no es lo mismo que una base de datos desfasada ("incoherente").</span><span class="sxs-lookup"><span data-stu-id="bb4de-231">A corrupt database is not the same as a dirty ("inconsistent") database.</span></span>

<span data-ttu-id="bb4de-232">Una base de datos dañada hace referencia a un daño físico o lógico, y no se puede corregir con la recuperación de software.</span><span class="sxs-lookup"><span data-stu-id="bb4de-232">A corrupt database refers to a physical or logical corruption, and cannot be fixed with soft recovery.</span></span> <span data-ttu-id="bb4de-233">Los daños físicos pueden ser volteo de bits, que se capturan con frecuencia en las sumas de comprobación de las páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="bb4de-233">Physical corruptions can be bit flips, which will frequently be caught by the checksums on the database pages.</span></span> <span data-ttu-id="bb4de-234">Una suma de comprobación con errores en un archivo de base de datos se manifiesta como un error de JET_errReadVerifyFailure.</span><span class="sxs-lookup"><span data-stu-id="bb4de-234">A failed checksum in a database file manifests itself as a JET_errReadVerifyFailure error.</span></span>

<span data-ttu-id="bb4de-235">Solo las bases de datos que se cierran correctamente pueden moverse o cambiarse de nombre con seguridad.</span><span class="sxs-lookup"><span data-stu-id="bb4de-235">Only cleanly shut down databases can be safely moved around or renamed.</span></span> <span data-ttu-id="bb4de-236">Si una base de datos no se ha cerrado correctamente, no se puede cambiar o cambiar de nombre automáticamente.</span><span class="sxs-lookup"><span data-stu-id="bb4de-236">If a database was not cleanly shut down, it cannot be automatically safely moved or renamed.</span></span>

<span data-ttu-id="bb4de-237">Varias bases de datos se pueden asociar a una sola secuencia de archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="bb4de-237">Multiple databases can be associated with a single transaction log file sequence.</span></span>

### <a name="temporary-databases"></a><span data-ttu-id="bb4de-238">Bases de datos temporales</span><span class="sxs-lookup"><span data-stu-id="bb4de-238">Temporary Databases</span></span>

<span data-ttu-id="bb4de-239">La base de datos temporal se usa como una memoria auxiliar para temptables y también se usa al crear índices.</span><span class="sxs-lookup"><span data-stu-id="bb4de-239">The temporary database is used as a backing store for temptables and it is also used when creating indices.</span></span>

<span data-ttu-id="bb4de-240">El nombre y la ubicación se configuran con [JET_paramTempPath](./temporary-database-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="bb4de-240">The name and location is configured with [JET_paramTempPath](./temporary-database-parameters.md).</span></span>

<span data-ttu-id="bb4de-241">Temptables se crean con [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span><span class="sxs-lookup"><span data-stu-id="bb4de-241">Temptables are created with [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md).</span></span> <span data-ttu-id="bb4de-242">También se crean mediante algunas llamadas API y se usan para devolver información de esquema (por ejemplo, [JetGetIndexInfo](./jetgetindexinfo-function.md)).</span><span class="sxs-lookup"><span data-stu-id="bb4de-242">They are also created by some API calls and used to return schema information (such as [JetGetIndexInfo](./jetgetindexinfo-function.md)).</span></span>

## <a name="flush-map-files"></a><span data-ttu-id="bb4de-243">Vaciar archivos de asignación</span><span class="sxs-lookup"><span data-stu-id="bb4de-243">Flush Map Files</span></span>

<span data-ttu-id="bb4de-244">A partir de la actualización de aniversario (cliente) de Windows 10 y Windows Server 2016 (servidor), ESE agregó un nivel adicional de protección contra las escrituras perdidas (o vaciados perdidos) 1, lo que permite detectar eventos initialization2 de este tipo.</span><span class="sxs-lookup"><span data-stu-id="bb4de-244">Starting with the Windows 10 Anniversary Update (client) and Windows Server 2016 (server), ESE added an additional level of protection against lost writes (or lost flushes) 1, allowing it to detect such events cross-process re-initialization2.</span></span> <span data-ttu-id="bb4de-245">Esta característica requiere la persistencia de metadatos en un archivo independiente denominado archivo de "mapa de vaciado".</span><span class="sxs-lookup"><span data-stu-id="bb4de-245">This feature requires persisting metadata to a separate file called a "flush map" file.</span></span>

<span data-ttu-id="bb4de-246">Se crea un archivo de mapa de vaciado para cada archivo de base de datos y se encuentra en el mismo directorio.</span><span class="sxs-lookup"><span data-stu-id="bb4de-246">One flush map file is created for each database file, and is located in the same directory.</span></span> <span data-ttu-id="bb4de-247">El archivo se denomina de forma similar al archivo de base de datos, pero con una extensión diferente.</span><span class="sxs-lookup"><span data-stu-id="bb4de-247">The file is named similarly to the database file, but with a different extension.</span></span> <span data-ttu-id="bb4de-248">Por ejemplo, si la aplicación cliente crea una base de datos con la ruta de acceso completa C: mi \\ Director \\ MyDabatase. edb, su archivo de mapa de vaciado correspondiente es C: mi \\ Director \\ MyDabatase. JFM.</span><span class="sxs-lookup"><span data-stu-id="bb4de-248">For example, if the client application creates a database with the full path C:\\MyDirectory\\MyDabatase.edb, its corresponding flush map file is C:\\MyDirectory\\MyDabatase.jfm.</span></span>

<span data-ttu-id="bb4de-249">Esta mejora presenta dos requisitos para el nombre de los archivos de base de datos:</span><span class="sxs-lookup"><span data-stu-id="bb4de-249">This enhancement introduces two requirements for how database files must be named:</span></span>

  - <span data-ttu-id="bb4de-250">Dos bases de datos del mismo directorio no deben tener el mismo nombre de archivo con extensiones diferentes.</span><span class="sxs-lookup"><span data-stu-id="bb4de-250">Two databases in the same directory must not have the same filename with different extensions.</span></span> <span data-ttu-id="bb4de-251">Por ejemplo: C: \\ \\ MyDabatase. db1 y c: mi \\ Director \\ MyDabatase. DB2.</span><span class="sxs-lookup"><span data-stu-id="bb4de-251">For example: C:\\MyDirectory\\MyDabatase.db1 and C:\\MyDirectory\\MyDabatase.db2.</span></span>

  - <span data-ttu-id="bb4de-252">2\.</span><span class="sxs-lookup"><span data-stu-id="bb4de-252">2\.</span></span> <span data-ttu-id="bb4de-253">Una base de datos no debe tener una extensión. JFM.</span><span class="sxs-lookup"><span data-stu-id="bb4de-253">A database must not have a .jfm extension.</span></span>

<span data-ttu-id="bb4de-254">Al copiar o trasladar un archivo de base de datos manualmente, su archivo de mapa de vaciado correspondiente también debe copiarse o moverse al mismo directorio de destino, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="bb4de-254">When you manually copy or move a database file, its corresponding flush map file should also be, respectively, copied or moved to the same destination directory.</span></span> <span data-ttu-id="bb4de-255">Si no hay un archivo de mapa de vaciado en el momento de una nueva base de datos adjunta (a través de [JetAttachDatabase](./jetattachdatabase-function.md), se creará un nuevo y se volverá a rellenar a petición a medida que las páginas se leen en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="bb4de-255">If a flush map file is not present at the time of a new database attachment (via [JetAttachDatabase](./jetattachdatabase-function.md), a new one will be created and re-populated on-demand as pages are read in from the database.</span></span> <span data-ttu-id="bb4de-256">ESE controla la combinación de archivos de mapa de bits y de base de datos no coincidentes, y obliga a que se elimine el mapa de vaciado no coincidente y se vuelva a crear desde cero.</span><span class="sxs-lookup"><span data-stu-id="bb4de-256">Mixing mismatching database and flush map files is handled by ESE, and forces the mismatched flush map to be deleted and re-created from scratch.</span></span>

<span data-ttu-id="bb4de-257">El tamaño de un archivo de mapa de vaciado es directamente proporcional a su archivo de base de datos asociado y aproximadamente igual a (todos los tamaños en bytes, el resultado se debe redondear al siguiente múltiplo de 8.192):</span><span class="sxs-lookup"><span data-stu-id="bb4de-257">The size of a flush map file is directly proportional to its associated database file and approximately equal to (all sizes in bytes, result must be rounded up to the next multiple of 8,192):</span></span>

`8,192 + ((<database file size> / <database page size>) / 4)`

<span data-ttu-id="bb4de-258">Por ejemplo: para una base de datos de 1,5 GB con un tamaño de página de 32 KB, el tamaño aproximado del mapa de vaciado es 24.576 bytes (o 24KB).</span><span class="sxs-lookup"><span data-stu-id="bb4de-258">For example: for a 1.5GB database using a 32KB page size, the approximate size of the flush map is 24,576 bytes (or 24KB).</span></span>

<span data-ttu-id="bb4de-259">El archivo de mapa de vaciado debe actualizarse a medida que se vacíen las páginas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="bb4de-259">The flush map file needs to be refreshed as database pages are flushed.</span></span> <span data-ttu-id="bb4de-260">Si el registro transaccional está habilitado (por ejemplo, [JET_paramRecovery](./transaction-log-parameters.md) establecido en "ON", el valor predeterminado), la actualización del mapa de vaciado se realiza a medida que la aplicación cliente realiza modificaciones en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="bb4de-260">If transactional logging is enabled (for example, [JET_paramRecovery](./transaction-log-parameters.md) set to "on", the default), refreshing the flush map is performed as the client application makes modifications to the database.</span></span> <span data-ttu-id="bb4de-261">En promedio, todo el mapa de vaciado se escribe en el medio no volátil una vez por cada 20% de [JET_paramCheckpointDepthMax](./database-cache-parameters.md) (en bytes) de los registros transaccionales generados.</span><span class="sxs-lookup"><span data-stu-id="bb4de-261">On average, the entire flush map is written to the non-volatile media once for every 20% of [JET_paramCheckpointDepthMax](./database-cache-parameters.md) -worth (in bytes) of transactional logs generated.</span></span> <span data-ttu-id="bb4de-262">El número de operaciones de escritura depende de cómo se distribuyan las modificaciones en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="bb4de-262">The number of write operations depends on how distributed throughout the database the modifications are.</span></span> <span data-ttu-id="bb4de-263">Pero, a lo sumo, aproximadamente (todos los tamaños en bytes):</span><span class="sxs-lookup"><span data-stu-id="bb4de-263">But it is at most, approximately (all sizes in bytes):</span></span>

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

<span data-ttu-id="bb4de-264">Si el registro transaccional está deshabilitado (por ejemplo, [JET_paramRecovery](./transaction-log-parameters.md) establecido en "OFF"), el mapa de vaciado se actualiza solo una vez cuando la base de datos se separa explícitamente (a través de [JetDetachDatabase](./jetdetachdatabase-function.md), o bien se desasocia implícitamente al terminar la instancia de ese asociada (a través de cualquiera de las funciones [JetTerm](./jetterm-function.md) , siempre y cuando no se pase [JET_bitTermDirty](./jetterm2-function.md) ).</span><span class="sxs-lookup"><span data-stu-id="bb4de-264">If transactional logging is disabled (for example, [JET_paramRecovery](./transaction-log-parameters.md) set to "off"), the flush map gets refreshed only once when the database is explicitly detached cleanly (via [JetDetachDatabase](./jetdetachdatabase-function.md), or implicitly detached cleanly by terminating its associated ESE instance (via any of the [JetTerm](./jetterm-function.md) functions, as long as [JET_bitTermDirty](./jetterm2-function.md) is not passed).</span></span>

<span data-ttu-id="bb4de-265">1 una escritura perdida (o vaciado perdido) se define como una operación de escritura que se devuelve correctamente desde el sistema operativo al motor de base de datos de ESE, pero los datos reales nunca se conservan en el archivo de base de datos en los medios no volátiles.</span><span class="sxs-lookup"><span data-stu-id="bb4de-265">1 A lost write (or lost flush) is defined as a write operation that returns successfully from the operating system to the ESE database engine but the actual data never gets persisted to the database file in the non-volatile media.</span></span> <span data-ttu-id="bb4de-266">Normalmente se debe a una pila de almacenamiento mal configurada o mal configurada (software o hardware).</span><span class="sxs-lookup"><span data-stu-id="bb4de-266">It is usually caused by a malfunctioning or misconfigured storage stack (software or hardware).</span></span> <span data-ttu-id="bb4de-267">Las aplicaciones cliente pueden recibir un error de [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) de las funciones de ese que requieren leer datos de la base de datos si los datos se encuentran en una región que ha sufrido un evento de escritura perdido.</span><span class="sxs-lookup"><span data-stu-id="bb4de-267">Client applications may receive a [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) error from ESE functions that require reading data from the database if the data is located in a region that underwent a lost write event.</span></span>

<span data-ttu-id="bb4de-268">2 la capacidad de detectar escrituras perdidas dentro de la duración de un proceso ha estado presente desde Windows 8 (cliente) y Windows Server 2012 (servidor).</span><span class="sxs-lookup"><span data-stu-id="bb4de-268">2 The ability to detect lost writes within a process's lifetime has been present since Windows 8 (client) and Windows Server 2012 (server).</span></span>
