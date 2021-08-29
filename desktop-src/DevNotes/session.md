---
description: La estructura SESSION contiene información sobre la sesión actual.
ms.assetid: e04571f9-eeb7-4612-8cb2-05aca7b5df06
title: Estructura SESSION
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
ms.openlocfilehash: db283c735e87fb88b489c3ad8367b37ab867c9627fffa7b6052706e0d260b54e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075955"
---
# <a name="session-structure"></a>Estructura SESSION

\[Esta estructura contiene información necesaria solo cuando se usan las **funciones DeleteExtractedFiles** y **Extract,** que no se admiten. Esta documentación solo se proporciona con fines informativos.\]

La **estructura SESSION** contiene información sobre la sesión actual.

## <a name="syntax"></a>Sintaxis


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



## <a name="members"></a>Miembros

<dl> <dt>

**act**
</dt> <dd>

la acción que se va a realizar. Este miembro puede ser uno de los valores del siguiente tipo enumerado.

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

**list**
</dt> <dd>

Identificador de una lista de archivos especificados en la línea de comandos. Este tipo de datos se declara como sigue:

`typedef void *HFILELIST;`

</dd> <dt>

**fAllCabinets**
</dt> <dd>

Marca que indica si se debe procesar más de un archivo de archivador. Si este valor es **TRUE,** se procesan los archivadores de continuación.

</dd> <dt>

**fOverwrite**
</dt> <dd>

Marca que indica si se deben sobrescribir los archivos existentes. Si este valor es **TRUE,** se sobrescriben los archivos existentes.

</dd> <dt>

**fNoLineFeed**
</dt> <dd>

Marca que indica si la última `printf` llamada tiene los caracteres de nueva línea ( `\n` ). Si este valor es **TRUE,** la última `printf` llamada no ingregó los caracteres de nueva línea.

</dd> <dt>

**fSelfExtract**
</dt> <dd>

Marca que indica si un gabinete se extrae de forma autoextrayendo. Si este valor es **TRUE,** el gabinete se extrae de forma autoextraída.

</dd> <dt>

**cbSelfExtractSize**
</dt> <dd>

Longitud del archivo ejecutable (.exe) de un gabinete autoextraíble.

</dd> <dt>

**cbSelfExtractSize**
</dt> <dd>

Longitud de la parte cab de un gabinete autoextrayendo.

</dd> <dt>

**ahfSelf**
</dt> <dd>

El archivo controla el archivador.

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

**cErrors**
</dt> <dd>

Recuento de errores detectados durante la sesión de extracción.

</dd> <dt>

**ydi**
</dt> <dd>

Identificador del contexto de FDI. Este tipo de datos se declara como sigue:

`typedef void FAR *HFDI; `

</dd> <dt>

**Erf**
</dt> <dd>

Estructura de errores de FDI. Consulte [**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).

</dd> <dt>

**cFiles**
</dt> <dd>

Recuento de archivos procesados.

</dd> <dt>

**cbTotalBytes**
</dt> <dd>

Número total de bytes extraídos.

</dd> <dt>

**perr**
</dt> <dd>

El paso a través de FDI.

</dd> <dt>

**se**
</dt> <dd>

Error del archivo de desbordamiento. Este miembro puede ser uno de los valores del siguiente tipo enumerado.

``` syntax
typedef enum {
    seNONE,                     // No error
    seNOT_ENOUGH_MEMORY,        // Not enough RAM
    seCANNOT_CREATE,            // Cannot create spill file
    seNOT_ENOUGH_SPACE,         // Not enough space for spill file
} SPILLERR;
```

</dd> <dt>

**cbSpill**
</dt> <dd>

Tamaño del archivo de desbordamiento solicitado.

</dd> <dt>

**achSelf**
</dt> <dd>

Nombre del archivo ejecutable (.exe).

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**achMsg**
</dt> <dd>

Búfer de formato de mensaje.

`#define cbMAX_LINE          256`

</dd> <dt>

**achLine**
</dt> <dd>

Búfer de formato de línea.

</dd> <dt>

**achLocation**
</dt> <dd>

el directorio de salida.

</dd> <dt>

**achFile**
</dt> <dd>

Nombre de archivo actual que se va a extraer.

</dd> <dt>

**achDest**
</dt> <dd>

Nombre de archivo de destino forzado.

</dd> <dt>

**achCabPath**
</dt> <dd>

Ruta de acceso que se debe buscar para un archivo de archivador.

</dd> <dt>

**fContinuationCabinet**
</dt> <dd>

Marca que indica si el gabinete actual es el primero procesado. Si se establece **en TRUE,** no es el primer gabinete procesado.

</dd> <dt>

**fShowReserveInfo**
</dt> <dd>

Marca que indica si se debe proporcionar información de reserva. Si se establece **en TRUE,** la información estará disponible.

</dd> <dt>

**fNextCabCalled**
</dt> <dd>

Este miembro proporciona una manera de determinar cuál de las entradas **de acab** usar si se están procesando todos los archivos de un conjunto de archivadores (**fAllCabinet** se establece en **TRUE).**

</dd> <dt>

**acab**
</dt> <dd>

Las dos últimas entradas del conjunto de gabinetes. Esta estructura se define de la siguiente manera:

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

**achZap**
</dt> <dd>

Prefijo que se quitará del nombre de archivo.

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**achCabinetFile**
</dt> <dd>

Archivo de archivador actual.

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**cArgv**
</dt> <dd>

Argc autoextraía predeterminado.

</dd> <dt>

**pArgv**
</dt> <dd>

Puntero a un puntero al argumento predeterminado autoextrayendo \[ \] .

</dd> <dt>

**fDestructive**
</dt> <dd>

Marca que minimiza el espacio en disco necesario cuando se establece en **TRUE.**

</dd> <dt>

**iCurrentFolder**
</dt> <dd>

Si **fDestructive** se establece en **TRUE,** extraiga solo la carpeta actual.

</dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeleteExtractedFiles**](deleteextractedfiles.md)
</dt> <dt>

[**Extracto**](extract.md)
</dt> </dl>

 

 
