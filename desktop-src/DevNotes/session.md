---
description: La estructura de la sesión contiene información sobre la sesión actual.
ms.assetid: e04571f9-eeb7-4612-8cb2-05aca7b5df06
title: Estructura de la sesión
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9e1f356020df681e00f43c7a47ac16048764c0ab
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806902"
---
# <a name="session-structure"></a><span data-ttu-id="b527b-103">Estructura de la sesión</span><span class="sxs-lookup"><span data-stu-id="b527b-103">SESSION structure</span></span>

<span data-ttu-id="b527b-104">\[Esta estructura contiene información necesaria solo cuando se usan las funciones **DeleteExtractedFiles** y **Extract** , que no se admiten.</span><span class="sxs-lookup"><span data-stu-id="b527b-104">\[This structure contains information required only when using the **DeleteExtractedFiles** and **Extract** functions, which are not supported.</span></span> <span data-ttu-id="b527b-105">Esta documentación se proporciona solo con fines informativos.\]</span><span class="sxs-lookup"><span data-stu-id="b527b-105">This documentation is provided for informational purposes only.\]</span></span>

<span data-ttu-id="b527b-106">La estructura de la **sesión** contiene información sobre la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="b527b-106">The **SESSION** structure contains information about the current session.</span></span>

## <a name="syntax"></a><span data-ttu-id="b527b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b527b-107">Syntax</span></span>


```C++
typedef struct {
  ACTION    act;
  HFILELIST hflist;
  BOOL      fAllCabinets;
  BOOL      fOverwrite;
  BOOL      fNoLineFeed;
  BOOL      fSelfExtract;
  long      cbSelfExtractSize;
  long      cbSelfExtractSize;
  int       ahfSelf[cMAX_CAB_FILE_OPEN];
  int       cErrors;
  HFDI      hfdi;
  ERF       erf;
  long      cFiles;
  long      cbTotalBytes;
  PERROR    perr;
  SPILLERR  se;
  long      cbSpill;
  char      achSelf[cbFILE_NAME_MAX];
  char      achMsg[cbMAX_LINE*2];
  char      achLine;
  char      achLocation;
  char      achFile;
  char      achDest;
  char      achCabPath;
  BOOL      fContinuationCabinet;
  BOOL      fShowReserveInfo;
  BOOL      fNextCabCalled;
  CABINET   acab[2];
  char      achZap[cbFILE_NAME_MAX];
  char      achCabinetFile[cbFILE_NAME_MAX];
  int       cArgv;
  char      **pArgv;
  int       fDestructive;
  USHORT    iCurrentFolder;
} SESSION, *PSESSION;
```



## <a name="members"></a><span data-ttu-id="b527b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b527b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b527b-109">**LEDs**</span><span class="sxs-lookup"><span data-stu-id="b527b-109">**act**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-110">la acción que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="b527b-110">The action to perform.</span></span> <span data-ttu-id="b527b-111">Este miembro puede ser uno de los valores del siguiente tipo enumerado.</span><span class="sxs-lookup"><span data-stu-id="b527b-111">This member can be one of the values from the following enumerated type.</span></span>

``` syntax
typedef enum {
    actBAD,         // Invalid action
    actHELP,        // Show help
    actDEFAULT,     // Perform default action based on command line arguments
    actDIRECTORY,   // Force display of cabinet directory
    actEXTRACT,     // Force file extraction
    actCOPY,        // Do single file-to-file copy
} ACTION;  
```

</dd> <dt>

<span data-ttu-id="b527b-112">**hflist**</span><span class="sxs-lookup"><span data-stu-id="b527b-112">**hflist**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-113">Identificador de una lista de archivos especificados en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="b527b-113">The handle to a list of files specified on the command line.</span></span> <span data-ttu-id="b527b-114">Este tipo de texto se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b527b-114">This datatype is declared as follows:</span></span>

`typedef void *HFILELIST;`

</dd> <dt>

<span data-ttu-id="b527b-115">**fAllCabinets**</span><span class="sxs-lookup"><span data-stu-id="b527b-115">**fAllCabinets**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-116">Marca que indica si se debe procesar más de un archivo contenedor.</span><span class="sxs-lookup"><span data-stu-id="b527b-116">A flag that indicates whether more than one cabinet file should be processed.</span></span> <span data-ttu-id="b527b-117">Si este valor es **true**, se procesan los archivadores de continuación.</span><span class="sxs-lookup"><span data-stu-id="b527b-117">If this value is **TRUE**, continuation cabinets are processed.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-118">**fOverwrite**</span><span class="sxs-lookup"><span data-stu-id="b527b-118">**fOverwrite**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-119">Marca que indica si se deben sobrescribir los archivos existentes.</span><span class="sxs-lookup"><span data-stu-id="b527b-119">A flag that indicates whether existing files should be overwritten.</span></span> <span data-ttu-id="b527b-120">Si este valor es **true**, se sobrescriben los archivos existentes.</span><span class="sxs-lookup"><span data-stu-id="b527b-120">If this value is **TRUE**, existing files are overwritten.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-121">**fNoLineFeed**</span><span class="sxs-lookup"><span data-stu-id="b527b-121">**fNoLineFeed**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-122">Marca que indica si la última `printf` llamada tiene los caracteres de nueva línea ( `\n` ).</span><span class="sxs-lookup"><span data-stu-id="b527b-122">A flag that indicates whether the last `printf` call has the newline (`\n`) characters.</span></span> <span data-ttu-id="b527b-123">Si este valor es **true**, la última `printf` llamada no incluía los caracteres de nueva línea.</span><span class="sxs-lookup"><span data-stu-id="b527b-123">If this value is **TRUE**, the last `printf` call did not include the newline characters.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-124">**fSelfExtract**</span><span class="sxs-lookup"><span data-stu-id="b527b-124">**fSelfExtract**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-125">Marca que indica si un archivo. cab se está autoextraíble.</span><span class="sxs-lookup"><span data-stu-id="b527b-125">A flag that indicates whether a cabinet is self extracting.</span></span> <span data-ttu-id="b527b-126">Si este valor es **true**, el archivo. cab se extrae automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b527b-126">If this value is **TRUE**, the cabinet is self extracting.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-127">**cbSelfExtractSize**</span><span class="sxs-lookup"><span data-stu-id="b527b-127">**cbSelfExtractSize**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-128">La longitud de la parte ejecutable (. exe) de un archivo. cab autoextraíble.</span><span class="sxs-lookup"><span data-stu-id="b527b-128">The length of the executable (.exe) portion of a self-extracting cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-129">**cbSelfExtractSize**</span><span class="sxs-lookup"><span data-stu-id="b527b-129">**cbSelfExtractSize**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-130">La longitud de la parte del archivo. CAB de un archivo. CAB autoextraíble.</span><span class="sxs-lookup"><span data-stu-id="b527b-130">The length of the CAB portion of a self-extracting cabinet.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-131">**ahfSelf**</span><span class="sxs-lookup"><span data-stu-id="b527b-131">**ahfSelf**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-132">Identificadores de archivos del archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="b527b-132">The file handles to the cabinet.</span></span>

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

<span data-ttu-id="b527b-133">**cErrors**</span><span class="sxs-lookup"><span data-stu-id="b527b-133">**cErrors**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-134">Recuento de errores encontrados durante la sesión de extracción.</span><span class="sxs-lookup"><span data-stu-id="b527b-134">The count of errors encountered during the extraction session.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-135">**hfdi**</span><span class="sxs-lookup"><span data-stu-id="b527b-135">**hfdi**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-136">Identificador del contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="b527b-136">A handle to the FDI context.</span></span> <span data-ttu-id="b527b-137">Este tipo de texto se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b527b-137">This datatype is declared as follows:</span></span>

`typedef void FAR *HFDI; `

</dd> <dt>

<span data-ttu-id="b527b-138">**Fun**</span><span class="sxs-lookup"><span data-stu-id="b527b-138">**erf**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-139">La estructura de error FDI.</span><span class="sxs-lookup"><span data-stu-id="b527b-139">The FDI error structure.</span></span> <span data-ttu-id="b527b-140">Vea [**Fun**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).</span><span class="sxs-lookup"><span data-stu-id="b527b-140">See [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).</span></span>

</dd> <dt>

<span data-ttu-id="b527b-141">**cFiles**</span><span class="sxs-lookup"><span data-stu-id="b527b-141">**cFiles**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-142">Recuento de archivos procesados.</span><span class="sxs-lookup"><span data-stu-id="b527b-142">The count of files processed.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-143">**cbTotalBytes**</span><span class="sxs-lookup"><span data-stu-id="b527b-143">**cbTotalBytes**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-144">Número total de bytes extraídos.</span><span class="sxs-lookup"><span data-stu-id="b527b-144">The total number of bytes extracted.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-145">**perr**</span><span class="sxs-lookup"><span data-stu-id="b527b-145">**perr**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-146">El paso a través de FDI.</span><span class="sxs-lookup"><span data-stu-id="b527b-146">The pass through FDI.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-147">**x300**</span><span class="sxs-lookup"><span data-stu-id="b527b-147">**se**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-148">Error de archivo de derrame.</span><span class="sxs-lookup"><span data-stu-id="b527b-148">The spill file error.</span></span> <span data-ttu-id="b527b-149">Este miembro puede ser uno de los valores del siguiente tipo enumerado.</span><span class="sxs-lookup"><span data-stu-id="b527b-149">This member can be one of the values from the following enumerated type.</span></span>

``` syntax
typedef enum {
    seNONE,                     // No error
    seNOT_ENOUGH_MEMORY,        // Not enough RAM
    seCANNOT_CREATE,            // Cannot create spill file
    seNOT_ENOUGH_SPACE,         // Not enough space for spill file
} SPILLERR;
```

</dd> <dt>

<span data-ttu-id="b527b-150">**cbSpill**</span><span class="sxs-lookup"><span data-stu-id="b527b-150">**cbSpill**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-151">Tamaño del archivo de derrame solicitado.</span><span class="sxs-lookup"><span data-stu-id="b527b-151">The size of the spill file requested.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-152">**achSelf**</span><span class="sxs-lookup"><span data-stu-id="b527b-152">**achSelf**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-153">Nombre del archivo ejecutable (. exe).</span><span class="sxs-lookup"><span data-stu-id="b527b-153">The name of the executable (.exe) file.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="b527b-154">**achMsg**</span><span class="sxs-lookup"><span data-stu-id="b527b-154">**achMsg**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-155">Búfer de formato del mensaje.</span><span class="sxs-lookup"><span data-stu-id="b527b-155">The message formatting buffer.</span></span>

`#define cbMAX_LINE          256`

</dd> <dt>

<span data-ttu-id="b527b-156">**achLine**</span><span class="sxs-lookup"><span data-stu-id="b527b-156">**achLine**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-157">Búfer de formato de línea.</span><span class="sxs-lookup"><span data-stu-id="b527b-157">The line formatting buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-158">**achLocation**</span><span class="sxs-lookup"><span data-stu-id="b527b-158">**achLocation**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-159">el directorio de salida.</span><span class="sxs-lookup"><span data-stu-id="b527b-159">The output directory.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-160">**achFile**</span><span class="sxs-lookup"><span data-stu-id="b527b-160">**achFile**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-161">Nombre de archivo actual que se va a extraer.</span><span class="sxs-lookup"><span data-stu-id="b527b-161">The current file name being extracted.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-162">**achDest**</span><span class="sxs-lookup"><span data-stu-id="b527b-162">**achDest**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-163">Nombre de archivo de destino forzado.</span><span class="sxs-lookup"><span data-stu-id="b527b-163">The forced destination file name.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-164">**achCabPath**</span><span class="sxs-lookup"><span data-stu-id="b527b-164">**achCabPath**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-165">Ruta de acceso en la que se va a buscar un archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="b527b-165">The path to look at for a cabinet file.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-166">**fContinuationCabinet**</span><span class="sxs-lookup"><span data-stu-id="b527b-166">**fContinuationCabinet**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-167">Marca que indica si el archivo. cab actual es el primero que se procesa.</span><span class="sxs-lookup"><span data-stu-id="b527b-167">A flag that indicates whether the current cabinet is the first one processed.</span></span> <span data-ttu-id="b527b-168">Si se establece en **true**, no se procesa el primer contenedor.</span><span class="sxs-lookup"><span data-stu-id="b527b-168">If set to **TRUE**, it is not the first cabinet processed.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-169">**fShowReserveInfo**</span><span class="sxs-lookup"><span data-stu-id="b527b-169">**fShowReserveInfo**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-170">Marca que indica si se debe proporcionar la información de reserva.</span><span class="sxs-lookup"><span data-stu-id="b527b-170">A flag that indicates whether reserve information should be provided.</span></span> <span data-ttu-id="b527b-171">Si se establece en **true**, la información estará disponible.</span><span class="sxs-lookup"><span data-stu-id="b527b-171">If set to **TRUE**, the information is made available.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-172">**fNextCabCalled**</span><span class="sxs-lookup"><span data-stu-id="b527b-172">**fNextCabCalled**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-173">Este miembro proporciona una manera de determinar cuál de las entradas de **Acab** se va a usar si se procesan todos los archivos de un conjunto de contenedores (**fAllCabinet** se establece en **true**).</span><span class="sxs-lookup"><span data-stu-id="b527b-173">This member provides a way to determine which of the **acab** entries to use if we are processing all files in a cabinet set (**fAllCabinet** is set to **TRUE**).</span></span>

</dd> <dt>

<span data-ttu-id="b527b-174">**acab**</span><span class="sxs-lookup"><span data-stu-id="b527b-174">**acab**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-175">Las dos últimas entradas del conjunto de contenedores.</span><span class="sxs-lookup"><span data-stu-id="b527b-175">The last two entries in the cabinet set.</span></span> <span data-ttu-id="b527b-176">Esta estructura se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b527b-176">This structure is defined as follows:</span></span>

``` syntax
typedef struct {
    char    achCabPath[cbFILE_NAME_MAX];     // Cabinet file path
    char    achCabFilename[cbFILE_NAME_MAX]; // Cabinet file name.ext
    char    achDiskName[cbFILE_NAME_MAX];    // User readable disk label
    USHORT  setID;
    USHORT  iCabinet;
} CABINET;
typedef CABINET *PCABINET;
```

</dd> <dt>

<span data-ttu-id="b527b-177">**achZap**</span><span class="sxs-lookup"><span data-stu-id="b527b-177">**achZap**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-178">El prefijo que se va a quitar del nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="b527b-178">The prefix to strip from the file name.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="b527b-179">**achCabinetFile**</span><span class="sxs-lookup"><span data-stu-id="b527b-179">**achCabinetFile**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-180">Archivo. cab actual.</span><span class="sxs-lookup"><span data-stu-id="b527b-180">The current cabinet file.</span></span>

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

<span data-ttu-id="b527b-181">**cArgv**</span><span class="sxs-lookup"><span data-stu-id="b527b-181">**cArgv**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-182">Argc predeterminado de extracción automática.</span><span class="sxs-lookup"><span data-stu-id="b527b-182">The default self-extracting argc.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-183">**pArgv**</span><span class="sxs-lookup"><span data-stu-id="b527b-183">**pArgv**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-184">Un puntero a un puntero a los argv de extracción automática predeterminados \[ \] .</span><span class="sxs-lookup"><span data-stu-id="b527b-184">A pointer to a pointer to the default self-extracting argv\[\].</span></span>

</dd> <dt>

<span data-ttu-id="b527b-185">**fDestructive**</span><span class="sxs-lookup"><span data-stu-id="b527b-185">**fDestructive**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-186">Marca que reduce el espacio en disco necesario cuando se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="b527b-186">A flag that minimizes the disk space needed when set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="b527b-187">**iCurrentFolder**</span><span class="sxs-lookup"><span data-stu-id="b527b-187">**iCurrentFolder**</span></span>
</dt> <dd>

<span data-ttu-id="b527b-188">Si **fDestructive** está establecido en **true**, extraiga solo la carpeta actual.</span><span class="sxs-lookup"><span data-stu-id="b527b-188">If **fDestructive** is set to **TRUE**, extract only the current folder.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="b527b-189">Vea también</span><span class="sxs-lookup"><span data-stu-id="b527b-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b527b-190">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="b527b-190">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
</dt> <dt>

[<span data-ttu-id="b527b-191">**Extracción**</span><span class="sxs-lookup"><span data-stu-id="b527b-191">**Extract**</span></span>](extract.md)
</dt> </dl>

 

 
