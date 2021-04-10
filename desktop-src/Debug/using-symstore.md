---
description: SymStore (symstore.exe) es una herramienta para crear almacenes de símbolos. Se incluye en el paquete de herramientas de depuración para Windows.
ms.assetid: fe8a96e9-e780-4e96-98ef-c5128515ee6c
title: Usar SymStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a87b5c527717d78adb9202fd1eddd54d1f44c02
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153100"
---
# <a name="using-symstore"></a><span data-ttu-id="bf566-104">Usar SymStore</span><span class="sxs-lookup"><span data-stu-id="bf566-104">Using SymStore</span></span>

<span data-ttu-id="bf566-105">SymStore (symstore.exe) es una herramienta para crear almacenes de símbolos.</span><span class="sxs-lookup"><span data-stu-id="bf566-105">SymStore (symstore.exe) is a tool for creating symbol stores.</span></span> <span data-ttu-id="bf566-106">Se incluye en el paquete de [herramientas de depuración para Windows](https://www.microsoft.com/?ref=go) .</span><span class="sxs-lookup"><span data-stu-id="bf566-106">It is included in the [Debugging Tools for Windows](https://www.microsoft.com/?ref=go) package.</span></span>

<span data-ttu-id="bf566-107">SymStore almacena los símbolos en un formato que permite al depurador buscar los símbolos según la marca de tiempo y el tamaño de la imagen (para un archivo. dbg o ejecutable), o la firma y la edad (para un archivo. pdb).</span><span class="sxs-lookup"><span data-stu-id="bf566-107">SymStore stores symbols in a format that enables the debugger to look up the symbols based on the time stamp and size of the image (for a .dbg or executable file), or signature and age (for a .pdb file).</span></span> <span data-ttu-id="bf566-108">La ventaja del almacén de símbolos con respecto al formato tradicional de almacenamiento de símbolos es que todos los símbolos se pueden almacenar o hacer referencia a ellos en el mismo servidor y recuperarlos mediante el depurador sin ningún conocimiento previo de qué producto contiene el símbolo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bf566-108">The advantage of the symbol store over the traditional symbol storage format is that all symbols can be stored or referenced on the same server and retrieved by the debugger without any prior knowledge of which product contains the corresponding symbol.</span></span>

<span data-ttu-id="bf566-109">Tenga en cuenta que no se pueden almacenar varias versiones de archivos de símbolos. pdb (por ejemplo, versiones públicas y privadas) en el mismo servidor, ya que cada una de ellas contiene la misma firma y edad.</span><span class="sxs-lookup"><span data-stu-id="bf566-109">Note that multiple versions of .pdb symbol files (for example, public and private versions) cannot be stored on the same server, because they each contain the same signature and age.</span></span>

## <a name="symstore-transactions"></a><span data-ttu-id="bf566-110">Transacciones SymStore</span><span class="sxs-lookup"><span data-stu-id="bf566-110">SymStore Transactions</span></span>

<span data-ttu-id="bf566-111">Cada llamada a SymStore se registra como una transacción.</span><span class="sxs-lookup"><span data-stu-id="bf566-111">Every call to SymStore is recorded as a transaction.</span></span> <span data-ttu-id="bf566-112">Hay dos tipos de transacciones: agregar y eliminar.</span><span class="sxs-lookup"><span data-stu-id="bf566-112">There are two types of transactions: add and delete.</span></span>

<span data-ttu-id="bf566-113">Cuando se crea el almacén de símbolos, se crea un directorio denominado "000admin" en la raíz del servidor.</span><span class="sxs-lookup"><span data-stu-id="bf566-113">When the symbol store is created, a directory, called "000admin", is created under the root of the server.</span></span> <span data-ttu-id="bf566-114">El directorio 000admin contiene un archivo para cada transacción, así como los archivos de registro Server.txt y History.txt.</span><span class="sxs-lookup"><span data-stu-id="bf566-114">The 000admin directory contains one file for each transaction, as well as the log files Server.txt and History.txt.</span></span> <span data-ttu-id="bf566-115">El archivo Server.txt contiene una lista de todas las transacciones que están actualmente en el servidor.</span><span class="sxs-lookup"><span data-stu-id="bf566-115">The Server.txt file contains a list of all transactions that are currently on the server.</span></span> <span data-ttu-id="bf566-116">El archivo de History.txt contiene un historial cronológico de todas las transacciones.</span><span class="sxs-lookup"><span data-stu-id="bf566-116">The History.txt file contains a chronological history of all transactions.</span></span>

<span data-ttu-id="bf566-117">Cada vez que SymStore almacena o quita archivos de símbolos, se crea un nuevo número de transacción.</span><span class="sxs-lookup"><span data-stu-id="bf566-117">Each time SymStore stores or removes symbol files, a new transaction number is created.</span></span> <span data-ttu-id="bf566-118">A continuación, se crea un archivo cuyo nombre es este número de transacción en 000admin.</span><span class="sxs-lookup"><span data-stu-id="bf566-118">Then, a file, whose name is this transaction number, is created in 000admin.</span></span> <span data-ttu-id="bf566-119">Este archivo contiene una lista de todos los archivos o punteros que se han agregado al almacén de símbolos durante esta transacción.</span><span class="sxs-lookup"><span data-stu-id="bf566-119">This file contains a list of all the files or pointers that have been added to the symbol store during this transaction.</span></span> <span data-ttu-id="bf566-120">Si se elimina una transacción, SymStore leerá el archivo de transacciones para determinar qué archivos y punteros debe eliminar.</span><span class="sxs-lookup"><span data-stu-id="bf566-120">If a transaction is deleted, SymStore will read through its transaction file to determine which files and pointers it should delete.</span></span>

<span data-ttu-id="bf566-121">Las opciones **Add** y **del** especifican si se va a realizar una operación de agregar o eliminar.</span><span class="sxs-lookup"><span data-stu-id="bf566-121">The **add** and **del** options specify whether an add or delete transaction is to be performed.</span></span> <span data-ttu-id="bf566-122">La inclusión de la opción **/p** con una operación de agregar especifica que se va a agregar un puntero. Si se omite la opción **/p** , se especifica que se va a agregar el archivo de símbolos real.</span><span class="sxs-lookup"><span data-stu-id="bf566-122">Including the **/p** option with an add operation specifies that a pointer is to be added; omitting the **/p** option specifies that the actual symbol file is to be added.</span></span>

<span data-ttu-id="bf566-123">También es posible crear el almacén de símbolos en dos fases independientes.</span><span class="sxs-lookup"><span data-stu-id="bf566-123">It is also possible to create the symbol store in two separate stages.</span></span> <span data-ttu-id="bf566-124">En la primera fase, se usa SymStore con la opción **/x** para crear un archivo de índice.</span><span class="sxs-lookup"><span data-stu-id="bf566-124">In the first stage, you use SymStore with the **/x** option to create an index file.</span></span> <span data-ttu-id="bf566-125">En la segunda fase, se usa SymStore con la opción **/y** para crear el almacén real de archivos o punteros a partir de la información del archivo de índice.</span><span class="sxs-lookup"><span data-stu-id="bf566-125">In the second stage, you use SymStore with the **/y** option to create the actual store of files or pointers from the information in the index file.</span></span>

<span data-ttu-id="bf566-126">Esta técnica puede ser útil por diversos motivos.</span><span class="sxs-lookup"><span data-stu-id="bf566-126">This can be a useful technique for a variety of reasons.</span></span> <span data-ttu-id="bf566-127">Por ejemplo, esto permite que el almacén de símbolos se vuelva a crear fácilmente si el almacén se pierde de algún modo, siempre y cuando el archivo de índice exista todavía.</span><span class="sxs-lookup"><span data-stu-id="bf566-127">For instance, this allows the symbol store to be easily recreated if the store is somehow lost, as long as the index file still exists.</span></span> <span data-ttu-id="bf566-128">O quizás el equipo que contiene los archivos de símbolos tiene una conexión de red lenta con el equipo en el que se creará el almacén de símbolos.</span><span class="sxs-lookup"><span data-stu-id="bf566-128">Or perhaps the computer containing the symbol files has a slow network connection to the computer on which the symbol store will be created.</span></span> <span data-ttu-id="bf566-129">En este caso, puede crear el archivo de índice en el mismo equipo que los archivos de símbolos, transferir el archivo de índice al segundo equipo y, a continuación, crear el almacén en el segundo equipo.</span><span class="sxs-lookup"><span data-stu-id="bf566-129">In this case, you can create the index file on the same machine as the symbol files, transfer the index file to the second machine, and then create the store on the second machine.</span></span>

<span data-ttu-id="bf566-130">Para obtener una lista completa de todos los parámetros de SymStore, consulte [Opciones de Command-Line de SymStore](symstore-command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="bf566-130">For a full listing of all SymStore parameters, see [SymStore Command-Line Options](symstore-command-line-options.md).</span></span>

> [!Note]  
> <span data-ttu-id="bf566-131">SymStore no admite transacciones simultáneas de varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="bf566-131">SymStore does not support simultaneous transactions from multiple users.</span></span> <span data-ttu-id="bf566-132">Se recomienda que un usuario se designe como "administrador" del almacén de símbolos y sea responsable de todas las transacciones **Add** y **del** .</span><span class="sxs-lookup"><span data-stu-id="bf566-132">It is recommended that one user be designated "administrator" of the symbol store and be responsible for all **add** and **del** transactions.</span></span>

 

## <a name="transaction-examples"></a><span data-ttu-id="bf566-133">Ejemplos de transacciones</span><span class="sxs-lookup"><span data-stu-id="bf566-133">Transaction Examples</span></span>

<span data-ttu-id="bf566-134">A continuación se muestran dos ejemplos de SymStore agregar punteros de símbolo para la compilación 3790 de Windows Server 2003 a \\ \\ sampledir \\ symsrv:</span><span class="sxs-lookup"><span data-stu-id="bf566-134">Here are two examples of SymStore adding symbol pointers for build 3790 of Windows Server 2003 to \\\\sampledir\\symsrv:</span></span>

``` syntax
symstore add /r /p /f \\BuildServer\BuildShare\3790free\symbols\*.*
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 free"
   /c "Sample add"
symstore add /r /p /f \\BuildServer\BuildShare\3790Chk\symbols\*.* 
   /s \\sampledir\symsrv /t "Windows Server 2003" /v "Build 3790 x86 checked"
   /c "Sample add"
```

<span data-ttu-id="bf566-135">En el ejemplo siguiente, SymStore agrega los archivos de símbolos reales para un proyecto de aplicación en las \\ \\ ubicaciones de largeapp de \\ AppServer \\ a \\ \\ testdir \\ symsrv:</span><span class="sxs-lookup"><span data-stu-id="bf566-135">In the following example, SymStore adds the actual symbol files for an application project in \\\\largeapp\\appserver\\bins to \\\\testdir\\symsrv:</span></span>

``` syntax
symstore add /r /f \\largeapp\appserver\bins\*.* /s \\testdir\symsrv 
   /t "Large Application" /v "Build 432" /c "Sample add"
```

<span data-ttu-id="bf566-136">Este es un ejemplo de cómo se usa un archivo de índice.</span><span class="sxs-lookup"><span data-stu-id="bf566-136">Here is an example of how an index file is used.</span></span> <span data-ttu-id="bf566-137">En primer lugar, SymStore crea un archivo de índice basado en la colección de archivos de símbolos de \\ \\ largeapp de \\ AppServer \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="bf566-137">First, SymStore creates an index file based on the collection of symbol files in \\\\largeapp\\appserver\\bins\\.</span></span> <span data-ttu-id="bf566-138">En este caso, el archivo de índice se coloca en un tercer equipo, \\ \\ \\ hubshare.</span><span class="sxs-lookup"><span data-stu-id="bf566-138">In this case, the index file is placed on a third computer, \\\\hubserver\\hubshare.</span></span> <span data-ttu-id="bf566-139">La opción **/g** se usa para especificar que el prefijo de archivo " \\ \\ largeapp \\ AppServer" podría cambiar en el futuro:</span><span class="sxs-lookup"><span data-stu-id="bf566-139">You use the **/g** option to specify that the file prefix "\\\\largeapp\\appserver" might change in the future:</span></span>

``` syntax
symstore add /r /p /g \\largeapp\appserver /f 
   \\largeapp\appserver\bins\*.* 
   /x \\hubserver\hubshare\myindex.txt
```

<span data-ttu-id="bf566-140">Ahora Supongamos que mueve todos los archivos de símbolos fuera de la máquina \\ \\ largeapp \\ AppServer y los coloca en el \\ \\ AppServer de archivo \\ .</span><span class="sxs-lookup"><span data-stu-id="bf566-140">Now suppose you move all the symbol files off of the machine \\\\largeapp\\appserver and put them on \\\\myarchive\\appserver.</span></span> <span data-ttu-id="bf566-141">A continuación, puede crear el propio almacén de símbolos desde el archivo de índice, \\ \\ \\ hubshare \\myindex.txt como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="bf566-141">You can then create the symbol store itself from the index file \\\\hubserver\\hubshare\\myindex.txt as follows:</span></span>

``` syntax
symstore add /y \\hubserver\hubshare\myindex.txt 
   /g \\myarchive\appserver /s \\sampledir\symsrv /p 
   /t "Large Application" /v "Build 432" /c "Sample Add from Index"
```

<span data-ttu-id="bf566-142">Por último, este es un ejemplo de SymStore que elimina un archivo agregado por una transacción anterior.</span><span class="sxs-lookup"><span data-stu-id="bf566-142">Finally, here is an example of SymStore deleting a file added by a previous transaction.</span></span> <span data-ttu-id="bf566-143">Vea la siguiente sección para obtener una explicación de cómo determinar el identificador de la transacción (en este caso, 0000000096).</span><span class="sxs-lookup"><span data-stu-id="bf566-143">See the following section for an explanation of how to determine the transaction ID (in this case, 0000000096).</span></span>

``` syntax
symstore del /i 0000000096 /s \\sampledir\symsrv
```

## <a name="compressed-files"></a><span data-ttu-id="bf566-144">Archivos comprimidos</span><span class="sxs-lookup"><span data-stu-id="bf566-144">Compressed Files</span></span>

<span data-ttu-id="bf566-145">SymStore se puede usar con archivos comprimidos de dos maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="bf566-145">SymStore can be used with compressed files in two different ways.</span></span>

1.  <span data-ttu-id="bf566-146">Use SymStore con la opción **/p** para almacenar punteros a los archivos de símbolos.</span><span class="sxs-lookup"><span data-stu-id="bf566-146">Use SymStore with the **/p** option to store pointers to the symbol files.</span></span> <span data-ttu-id="bf566-147">Una vez finalizado SymStore, comprima los archivos a los que hacen referencia los punteros.</span><span class="sxs-lookup"><span data-stu-id="bf566-147">After SymStore finishes, compress the files that the pointers refer to.</span></span>
2.  <span data-ttu-id="bf566-148">Use SymStore con la opción **/x** para crear un archivo de índice.</span><span class="sxs-lookup"><span data-stu-id="bf566-148">Use SymStore with the **/x** option to create an index file.</span></span> <span data-ttu-id="bf566-149">Una vez finalizado SymStore, comprima los archivos enumerados en el archivo de índice.</span><span class="sxs-lookup"><span data-stu-id="bf566-149">After SymStore finishes, compress the files listed in the index file.</span></span> <span data-ttu-id="bf566-150">A continuación, use SymStore con la opción **/y** (y, si lo desea, la opción **/p** ) para almacenar los archivos o punteros en los archivos del almacén de símbolos.</span><span class="sxs-lookup"><span data-stu-id="bf566-150">Then use SymStore with the **/y** option (and, if you wish, the **/p** option) to store the files or pointers to the files in the symbol store.</span></span> <span data-ttu-id="bf566-151">(SymStore no necesita descomprimir los archivos para realizar esta operación).</span><span class="sxs-lookup"><span data-stu-id="bf566-151">(SymStore will not need to uncompress the files to perform this operation.)</span></span>

<span data-ttu-id="bf566-152">El servidor de símbolos será responsable de descomprimir los archivos cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="bf566-152">Your symbol server will be responsible for uncompressing the files when they are needed.</span></span>

<span data-ttu-id="bf566-153">Si usa SymSrv como servidor de símbolos, se debe realizar cualquier compresión mediante la herramienta de compress.exe que se distribuye con el kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bf566-153">If you are using SymSrv as your symbol server, any compression should be done using the compress.exe tool that is distributed with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bf566-154">Los archivos comprimidos deben tener un carácter de subrayado como último carácter en sus extensiones de archivo (por ejemplo, Module1. PD \_ o Module2. dB \_ ).</span><span class="sxs-lookup"><span data-stu-id="bf566-154">Compressed files should have an underscore as the last character in their file extensions (for example, module1.pd\_ or module2.db\_).</span></span> <span data-ttu-id="bf566-155">Para obtener más información, consulte [uso de SymSrv](using-symsrv.md).</span><span class="sxs-lookup"><span data-stu-id="bf566-155">For details, see [Using SymSrv](using-symsrv.md).</span></span>

## <a name="the-servertxt-and-historytxt-files"></a><span data-ttu-id="bf566-156">Archivos de server.txt y history.txt</span><span class="sxs-lookup"><span data-stu-id="bf566-156">The server.txt and history.txt Files</span></span>

<span data-ttu-id="bf566-157">Cuando se agrega una transacción, se agregan varios elementos de información a server.txt y history.txt para la capacidad de búsqueda futura.</span><span class="sxs-lookup"><span data-stu-id="bf566-157">When a transaction is added, several items of information are added to server.txt and history.txt for future lookup capability.</span></span> <span data-ttu-id="bf566-158">A continuación se muestra un ejemplo de una línea en server.txt y history.txt para una transacción de adición:</span><span class="sxs-lookup"><span data-stu-id="bf566-158">The following is an example of a line in server.txt and history.txt for an add transaction:</span></span>

``` syntax
0000000096,add,ptr,10/09/99,00:08:32,Windows XP,x86 fre 1.156c-RTM-2,Added from \\mybuilds\symbols,
```

<span data-ttu-id="bf566-159">Se trata de una línea separada por comas.</span><span class="sxs-lookup"><span data-stu-id="bf566-159">This is a comma-separated line.</span></span> <span data-ttu-id="bf566-160">Los campos se definen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="bf566-160">The fields are defined as follows.</span></span>



| <span data-ttu-id="bf566-161">Campo</span><span class="sxs-lookup"><span data-stu-id="bf566-161">Field</span></span>      | <span data-ttu-id="bf566-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf566-162">Description</span></span>                                                                         |
|------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bf566-163">0000000096</span><span class="sxs-lookup"><span data-stu-id="bf566-163">0000000096</span></span> | <span data-ttu-id="bf566-164">Número de ID. de transacción, tal y como lo creó SymStore.</span><span class="sxs-lookup"><span data-stu-id="bf566-164">Transaction ID number, as created by SymStore.</span></span>                                      |
| <span data-ttu-id="bf566-165">add</span><span class="sxs-lookup"><span data-stu-id="bf566-165">add</span></span>        | <span data-ttu-id="bf566-166">Tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="bf566-166">Type of transaction.</span></span> <span data-ttu-id="bf566-167">Este campo puede ser **Add** o **del**.</span><span class="sxs-lookup"><span data-stu-id="bf566-167">This field can be either **add** or **del**.</span></span>                   |
| <span data-ttu-id="bf566-168">ptr</span><span class="sxs-lookup"><span data-stu-id="bf566-168">ptr</span></span>        | <span data-ttu-id="bf566-169">Indica si se agregaron archivos o punteros.</span><span class="sxs-lookup"><span data-stu-id="bf566-169">Whether files or pointers were added.</span></span> <span data-ttu-id="bf566-170">Este campo puede ser **archivo** o **ptr**.</span><span class="sxs-lookup"><span data-stu-id="bf566-170">This field can be either **file** or **ptr**.</span></span> |
| <span data-ttu-id="bf566-171">10/09/99</span><span class="sxs-lookup"><span data-stu-id="bf566-171">10/09/99</span></span>   | <span data-ttu-id="bf566-172">Fecha en que se produjo la transacción.</span><span class="sxs-lookup"><span data-stu-id="bf566-172">Date when transaction occurred.</span></span>                                                     |
| <span data-ttu-id="bf566-173">00:08:32</span><span class="sxs-lookup"><span data-stu-id="bf566-173">00:08:32</span></span>   | <span data-ttu-id="bf566-174">Hora de inicio de la transacción.</span><span class="sxs-lookup"><span data-stu-id="bf566-174">Time when transaction started.</span></span>                                                      |
| <span data-ttu-id="bf566-175">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf566-175">Windows XP</span></span> | <span data-ttu-id="bf566-176">Producto.</span><span class="sxs-lookup"><span data-stu-id="bf566-176">Product.</span></span>                                                                            |
| <span data-ttu-id="bf566-177">"fre" x86</span><span class="sxs-lookup"><span data-stu-id="bf566-177">x86 fre</span></span>    | <span data-ttu-id="bf566-178">Versión (opcional).</span><span class="sxs-lookup"><span data-stu-id="bf566-178">Version (optional).</span></span>                                                                 |
| <span data-ttu-id="bf566-179">Agregado desde</span><span class="sxs-lookup"><span data-stu-id="bf566-179">Added from</span></span> | <span data-ttu-id="bf566-180">Comentario (opcional)</span><span class="sxs-lookup"><span data-stu-id="bf566-180">Comment (optional)</span></span>                                                                  |
| <span data-ttu-id="bf566-181">No utilizado</span><span class="sxs-lookup"><span data-stu-id="bf566-181">Unused</span></span>     | <span data-ttu-id="bf566-182">(Reservado para su uso posterior).</span><span class="sxs-lookup"><span data-stu-id="bf566-182">(Reserved for later use.)</span></span>                                                           |



 

<span data-ttu-id="bf566-183">A continuación se muestran algunas líneas de ejemplo del archivo de transacción 0000000096.</span><span class="sxs-lookup"><span data-stu-id="bf566-183">Here are some sample lines from the transaction file 0000000096.</span></span> <span data-ttu-id="bf566-184">Cada línea registra el directorio y la ubicación del archivo o puntero que se agregó al directorio.</span><span class="sxs-lookup"><span data-stu-id="bf566-184">Each line records the directory and the location of the file or pointer that was added to the directory.</span></span>

``` syntax
canon800.dbg\35d9fd51b000,\\mybuilds\symbols\sp4\dll\canon800.dbg
canonlbp.dbg\35d9fd521c000,\\mybuilds\symbols\sp4\dll\canonlbp.dbg
certadm.dbg\352bf2f48000,\\mybuilds\symbols\sp4\dll\certadm.dbg
certcli.dbg\352bf2f1b000,\\mybuilds\symbols\sp4\dll\certcli.dbg
certcrpt.dbg\352bf04911000,\\mybuilds\symbols\sp4\dll\certcrpt.dbg
certenc.dbg\352bf2f7f000,\\mybuilds\symbols\sp4\dll\certenc.dbg
```

<span data-ttu-id="bf566-185">Si utiliza una transacción **del** para deshacer las transacciones **agregadas** originales, estas líneas se quitarán de server.txt y se agregará la siguiente línea a history.txt:</span><span class="sxs-lookup"><span data-stu-id="bf566-185">If you use a **del** transaction to undo the original **add** transactions, these lines will be removed from server.txt, and the following line will be added to history.txt:</span></span>

``` syntax
0000000105,del,0000000096
```

<span data-ttu-id="bf566-186">Los campos de la transacción de eliminación se definen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="bf566-186">The fields for the delete transaction are defined as follows.</span></span>



| <span data-ttu-id="bf566-187">Campo</span><span class="sxs-lookup"><span data-stu-id="bf566-187">Field</span></span>      | <span data-ttu-id="bf566-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf566-188">Description</span></span>                                                       |
|------------|-------------------------------------------------------------------|
| <span data-ttu-id="bf566-189">0000000105</span><span class="sxs-lookup"><span data-stu-id="bf566-189">0000000105</span></span> | <span data-ttu-id="bf566-190">Número de ID. de transacción, tal y como lo creó SymStore.</span><span class="sxs-lookup"><span data-stu-id="bf566-190">Transaction ID number, as created by SymStore.</span></span>                    |
| <span data-ttu-id="bf566-191">del</span><span class="sxs-lookup"><span data-stu-id="bf566-191">del</span></span>        | <span data-ttu-id="bf566-192">Tipo de transacción.</span><span class="sxs-lookup"><span data-stu-id="bf566-192">Type of transaction.</span></span> <span data-ttu-id="bf566-193">Este campo puede ser **Add** o **del**.</span><span class="sxs-lookup"><span data-stu-id="bf566-193">This field can be either **add** or **del**.</span></span> |
| <span data-ttu-id="bf566-194">0000000096</span><span class="sxs-lookup"><span data-stu-id="bf566-194">0000000096</span></span> | <span data-ttu-id="bf566-195">Transacción que se eliminó.</span><span class="sxs-lookup"><span data-stu-id="bf566-195">Transaction that was deleted.</span></span>                                     |



 

## <a name="symbol-storage-format"></a><span data-ttu-id="bf566-196">Formato de almacenamiento de símbolos</span><span class="sxs-lookup"><span data-stu-id="bf566-196">Symbol Storage Format</span></span>

<span data-ttu-id="bf566-197">SymStore usa el sistema de archivos como una base de datos.</span><span class="sxs-lookup"><span data-stu-id="bf566-197">SymStore uses the file system itself as a database.</span></span> <span data-ttu-id="bf566-198">Crea un árbol grande de directorios, con nombres de directorio basados en elementos como marcas de tiempo de archivo de símbolos, firmas, edad y otros datos.</span><span class="sxs-lookup"><span data-stu-id="bf566-198">It creates a large tree of directories, with directory names based on such things as the symbol file time stamps, signatures, age, and other data.</span></span>

<span data-ttu-id="bf566-199">Por ejemplo, después de que se hayan agregado al servidor varios archivos ACPI. dbg distintos, los directorios podrían tener el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="bf566-199">For example, after several different acpi.dbg files have been added to the server, the directories could look like this:</span></span>

``` syntax
Directory of \\mybuilds\symsrv\acpi.dbg
10/06/1999  05:46p      <DIR>          .
10/06/1999  05:46p      <DIR>          ..
10/04/1999  01:54p      <DIR>          37cdb03962040
10/04/1999  01:49p      <DIR>          37cdb04027740
10/04/1999  12:56p      <DIR>          37e3eb1c62060
10/04/1999  12:51p      <DIR>          37e3ebcc27760
10/04/1999  12:45p      <DIR>          37ed151662060
10/04/1999  12:39p      <DIR>          37ed15dd27760
10/04/1999  11:33a      <DIR>          37f03ce962020
10/04/1999  11:21a      <DIR>          37f03cf7277c0
10/06/1999  05:38p      <DIR>          37fa7f00277e0
10/06/1999  05:46p      <DIR>          37fa7f01620a0
```

<span data-ttu-id="bf566-200">En este ejemplo, la ruta de acceso de búsqueda del archivo de símbolos ACPI. dbg podría tener un aspecto similar al siguiente: \\ \\ \\ symsrv \\ ACPI. dbg \\ 37cdb03962040.</span><span class="sxs-lookup"><span data-stu-id="bf566-200">In this example, the lookup path for the acpi.dbg symbol file might look something like this: \\\\mybuilds\\symsrv\\acpi.dbg\\37cdb03962040.</span></span>

<span data-ttu-id="bf566-201">Pueden existir tres archivos dentro del directorio de búsqueda:</span><span class="sxs-lookup"><span data-stu-id="bf566-201">Three files may exist inside the lookup directory:</span></span>

1.  <span data-ttu-id="bf566-202">Si se almacenó el archivo, entonces ACPI. dbg existirá allí.</span><span class="sxs-lookup"><span data-stu-id="bf566-202">If the file was stored, then acpi.dbg will exist there.</span></span>
2.  <span data-ttu-id="bf566-203">Si se almacenó un puntero, se creará un archivo denominado File. PTR que contendrá la ruta de acceso al archivo de símbolos real.</span><span class="sxs-lookup"><span data-stu-id="bf566-203">If a pointer was stored, then a file called file.ptr will exist and contain the path to the actual symbol file.</span></span>
3.  <span data-ttu-id="bf566-204">Un archivo denominado refs. PTR, que contiene una lista de todas las ubicaciones actuales de ACPI. dbg con esta marca de tiempo y el tamaño de la imagen que se han agregado actualmente al almacén de símbolos.</span><span class="sxs-lookup"><span data-stu-id="bf566-204">A file called refs.ptr, which contains a list of all the current locations for acpi.dbg with this timestamp and image size that are currently added to the symbol store.</span></span>

<span data-ttu-id="bf566-205">Al mostrar la lista de directorios de \\ \\ \\ symsrvs, \\ ACPI. dbg \\ 37cdb03962040 ofrece lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bf566-205">Displaying the directory listing of \\\\mybuilds\\symsrv\\acpi.dbg\\37cdb03962040 gives the following:</span></span>

``` syntax
10/04/1999  01:54p                  52 file.ptr
10/04/1999  01:54p                  67 refs.ptr
```

<span data-ttu-id="bf566-206">El archivo File. PTR contiene la cadena de texto " \\ \\ albuilds \\ Symbols \\ x86 \\ 2128. chk \\ Symbols \\ Sys \\ ACPI. dbg".</span><span class="sxs-lookup"><span data-stu-id="bf566-206">The file file.ptr contains the text string "\\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg".</span></span> <span data-ttu-id="bf566-207">Puesto que no hay ningún archivo llamado ACPI. dbg en este directorio, el depurador intentará encontrar el archivo en \\ \\ símbolos de \\ generación \\ x86 \\ 2128. chk \\ Symbols \\ Sys \\ ACPI. dbg.</span><span class="sxs-lookup"><span data-stu-id="bf566-207">Since there is no file called acpi.dbg in this directory, the debugger will try to find the file at \\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg.</span></span>

<span data-ttu-id="bf566-208">El contenido de refs. PTR solo se usa en SymStore, no en el depurador.</span><span class="sxs-lookup"><span data-stu-id="bf566-208">The contents of refs.ptr are used only by SymStore, not the debugger.</span></span> <span data-ttu-id="bf566-209">Este archivo contiene un registro de todas las transacciones que han tenido lugar en este directorio.</span><span class="sxs-lookup"><span data-stu-id="bf566-209">This file contains a record of all transactions that have taken place in this directory.</span></span> <span data-ttu-id="bf566-210">Una línea de ejemplo de refs. PTR podría ser:</span><span class="sxs-lookup"><span data-stu-id="bf566-210">A sample line from refs.ptr might be:</span></span>

``` syntax
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\sys\acpi.dbg
```

<span data-ttu-id="bf566-211">Esto muestra que se ha agregado un puntero a los \\ \\ símbolos de generación de \\ símbolos \\ x86 \\ 2128. chk \\ \\ Sys \\ ACPI. dbg con la transacción "0000000026".</span><span class="sxs-lookup"><span data-stu-id="bf566-211">This shows that a pointer to \\\\mybuilds\\symbols\\x86\\2128.chk\\symbols\\sys\\acpi.dbg was added with transaction "0000000026".</span></span>

<span data-ttu-id="bf566-212">Algunos archivos de símbolos permanecen constantes a través de varios productos o compilaciones o un producto determinado.</span><span class="sxs-lookup"><span data-stu-id="bf566-212">Some symbol files stay constant through various products or builds or a particular product.</span></span> <span data-ttu-id="bf566-213">Un ejemplo de esto es el archivo Msvcrt. pdb.</span><span class="sxs-lookup"><span data-stu-id="bf566-213">One example of this is the file msvcrt.pdb.</span></span> <span data-ttu-id="bf566-214">Al hacer un directorio de \\ \\ \\ symsrv \\ msvcrt. pdb, se muestra que solo se han agregado dos versiones de msvcrt. pdb al servidor de símbolos:</span><span class="sxs-lookup"><span data-stu-id="bf566-214">Doing a directory of \\\\mybuilds\\symsrv\\msvcrt.pdb shows that only two versions of msvcrt.pdb have been added to the symbols server:</span></span>

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb
10/06/1999  05:37p      <DIR>          .
10/06/1999  05:37p      <DIR>          ..
10/04/1999  11:19a      <DIR>          37a8f40e2
10/06/1999  05:37p      <DIR>          37f2c2272
```

<span data-ttu-id="bf566-215">Sin embargo, al hacer un directorio de \\ \\ \\ symsrv \\ msvcrt. pdb \\ 37a8f40e2, se muestra que refs. PTR tiene varios punteros.</span><span class="sxs-lookup"><span data-stu-id="bf566-215">However, doing a directory of \\\\mybuilds\\symsrv\\msvcrt.pdb\\37a8f40e2 shows that refs.ptr has several pointers in it.</span></span>

``` syntax
Directory of \\mybuilds\symsrv\msvcrt.pdb\37a8f40e2
10/05/1999  02:50p              54     file.ptr
10/05/1999  02:50p           2,039     refs.ptr
```

<span data-ttu-id="bf566-216">El contenido de \\ \\ \\ symsrv \\ msvcrt. pdb \\ 37a8f40e2 \\ refs. PTR es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="bf566-216">The contents of \\\\mybuilds\\symsrv\\msvcrt.pdb\\37a8f40e2\\refs.ptr are the following:</span></span>

``` syntax
0000000001,ptr,\\mybuilds\symbols\x86\2137\symbols\dll\msvcrt.pdb
0000000002,ptr,\\mybuilds\symbols\x86\2137.chk\symbols\dll\msvcrt.pdb
0000000003,ptr,\\mybuilds\symbols\x86\2138\symbols\dll\msvcrt.pdb
0000000004,ptr,\\mybuilds\symbols\x86\2138.chk\symbols\dll\msvcrt.pdb
0000000005,ptr,\\mybuilds\symbols\x86\2139\symbols\dll\msvcrt.pdb
0000000006,ptr,\\mybuilds\symbols\x86\2139.chk\symbols\dll\msvcrt.pdb
0000000007,ptr,\\mybuilds\symbols\x86\2140\symbols\dll\msvcrt.pdb
0000000008,ptr,\\mybuilds\symbols\x86\2140.chk\symbols\dll\msvcrt.pdb
0000000009,ptr,\\mybuilds\symbols\x86\2136\symbols\dll\msvcrt.pdb
0000000010,ptr,\\mybuilds\symbols\x86\2136.chk\symbols\dll\msvcrt.pdb
0000000011,ptr,\\mybuilds\symbols\x86\2135\symbols\dll\msvcrt.pdb
0000000012,ptr,\\mybuilds\symbols\x86\2135.chk\symbols\dll\msvcrt.pdb
0000000013,ptr,\\mybuilds\symbols\x86\2134\symbols\dll\msvcrt.pdb
0000000014,ptr,\\mybuilds\symbols\x86\2134.chk\symbols\dll\msvcrt.pdb
0000000015,ptr,\\mybuilds\symbols\x86\2133\symbols\dll\msvcrt.pdb
0000000016,ptr,\\mybuilds\symbols\x86\2133.chk\symbols\dll\msvcrt.pdb
0000000017,ptr,\\mybuilds\symbols\x86\2132\symbols\dll\msvcrt.pdb
0000000018,ptr,\\mybuilds\symbols\x86\2132.chk\symbols\dll\msvcrt.pdb
0000000019,ptr,\\mybuilds\symbols\x86\2131\symbols\dll\msvcrt.pdb
0000000020,ptr,\\mybuilds\symbols\x86\2131.chk\symbols\dll\msvcrt.pdb
0000000021,ptr,\\mybuilds\symbols\x86\2130\symbols\dll\msvcrt.pdb
0000000022,ptr,\\mybuilds\symbols\x86\2130.chk\symbols\dll\msvcrt.pdb
0000000023,ptr,\\mybuilds\symbols\x86\2129\symbols\dll\msvcrt.pdb
0000000024,ptr,\\mybuilds\symbols\x86\2129.chk\symbols\dll\msvcrt.pdb
0000000025,ptr,\\mybuilds\symbols\x86\2128\symbols\dll\msvcrt.pdb
0000000026,ptr,\\mybuilds\symbols\x86\2128.chk\symbols\dll\msvcrt.pdb
0000000027,ptr,\\mybuilds\symbols\x86\2141\symbols\dll\msvcrt.pdb
0000000028,ptr,\\mybuilds\symbols\x86\2141.chk\symbols\dll\msvcrt.pdb
0000000029,ptr,\\mybuilds\symbols\x86\2142\symbols\dll\msvcrt.pdb
0000000030,ptr,\\mybuilds\symbols\x86\2142.chk\symbols\dll\msvcrt.pdb
```

<span data-ttu-id="bf566-217">Esto muestra que se ha usado el mismo archivo Msvcrt. pdb para varias compilaciones de símbolos almacenados en las \\ \\ \\ symsrv.</span><span class="sxs-lookup"><span data-stu-id="bf566-217">This shows that the same msvcrt.pdb was used for multiple builds of symbols stored on \\\\mybuilds\\symsrv.</span></span>

<span data-ttu-id="bf566-218">A continuación se muestra un ejemplo de un directorio que contiene una combinación de adiciones de archivos y punteros:</span><span class="sxs-lookup"><span data-stu-id="bf566-218">Here is an example of a directory that contains a mixture of file and pointer additions:</span></span>

``` syntax
Directory of E:\symsrv\dbghelp.dbg\38039ff439000
10/12/1999  01:54p         141,232     dbghelp.dbg
10/13/1999  04:57p              49     file.ptr
10/13/1999  04:57p             306     refs.ptr
```

<span data-ttu-id="bf566-219">En este caso, refs. PTR tiene el siguiente contenido:</span><span class="sxs-lookup"><span data-stu-id="bf566-219">In this case, refs.ptr has the following contents:</span></span>

``` syntax
0000000043,file,e:\binaries\symbols\retail\dll\dbghelp.dbg
0000000044,file,f:\binaries\symbols\retail\dll\dbghelp.dbg
0000000045,file,g:\binaries\symbols\retail\dll\dbghelp.dbg
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

<span data-ttu-id="bf566-220">Por lo tanto, las transacciones 43, 44 y 45 agregaron el mismo archivo al servidor y las transacciones 46 y 47 punteros agregados.</span><span class="sxs-lookup"><span data-stu-id="bf566-220">Thus, transactions 43, 44, and 45 added the same file to the server, and transactions 46 and 47 added pointers.</span></span> <span data-ttu-id="bf566-221">Si se eliminan las transacciones 43, 44 y 45, el archivo DbgHelp. dbg se eliminará del directorio.</span><span class="sxs-lookup"><span data-stu-id="bf566-221">If transactions 43, 44, and 45 are deleted, then the file dbghelp.dbg will be deleted from the directory.</span></span> <span data-ttu-id="bf566-222">El directorio tendrá el siguiente contenido:</span><span class="sxs-lookup"><span data-stu-id="bf566-222">The directory will then have the following contents:</span></span>

``` syntax
Directory of e:\symsrv\dbghelp.dbg\38039ff439000
10/13/1999  05:01p                   49 file.ptr
10/13/1999  05:01p                 130 refs.ptr
```

<span data-ttu-id="bf566-223">Ahora File. PTR contiene " \\ \\ sampledir2 \\ bin \\ \\ Retail \\ dll \\ DbgHelp. dbg" y refs. PTR contiene</span><span class="sxs-lookup"><span data-stu-id="bf566-223">Now file.ptr contains "\\\\sampledir2\\bin\\symbols\\retail\\dll\\dbghelp.dbg", and refs.ptr contains</span></span>

``` syntax
0000000046,ptr,\\sampledir\bin\symbols\retail\dll\dbghelp.dbg
0000000047,ptr,\\sampledir2\bin\symbols\retail\dll\dbghelp.dbg
```

<span data-ttu-id="bf566-224">Siempre que la última entrada en refs. PTR sea un puntero, el archivo File. PTR existirá y contendrá la ruta de acceso al archivo asociado.</span><span class="sxs-lookup"><span data-stu-id="bf566-224">Whenever the final entry in refs.ptr is a pointer, the file file.ptr will exist and contain the path to the associated file.</span></span> <span data-ttu-id="bf566-225">Siempre que la última entrada en refs. PTR sea un archivo, no existirá ningún archivo. PTR en este directorio.</span><span class="sxs-lookup"><span data-stu-id="bf566-225">Whenever the final entry in refs.ptr is a file, no file.ptr will exist in this directory.</span></span> <span data-ttu-id="bf566-226">Por lo tanto, cualquier operación de eliminación que quite la entrada final en refs. PTR puede dar lugar a que se cree, elimine o cambie File. PTR.</span><span class="sxs-lookup"><span data-stu-id="bf566-226">Therefore, any delete operation that removes the final entry in refs.ptr may result in file.ptr being created, deleted, or changed.</span></span>

 

 



