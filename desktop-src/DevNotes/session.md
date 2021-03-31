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
# <a name="session-structure"></a>Estructura de la sesión

\[Esta estructura contiene información necesaria solo cuando se usan las funciones **DeleteExtractedFiles** y **Extract** , que no se admiten. Esta documentación se proporciona solo con fines informativos.\]

La estructura de la **sesión** contiene información sobre la sesión actual.

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

**LEDs**
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

**hflist**
</dt> <dd>

Identificador de una lista de archivos especificados en la línea de comandos. Este tipo de texto se declara de la siguiente manera:

`typedef void *HFILELIST;`

</dd> <dt>

**fAllCabinets**
</dt> <dd>

Marca que indica si se debe procesar más de un archivo contenedor. Si este valor es **true**, se procesan los archivadores de continuación.

</dd> <dt>

**fOverwrite**
</dt> <dd>

Marca que indica si se deben sobrescribir los archivos existentes. Si este valor es **true**, se sobrescriben los archivos existentes.

</dd> <dt>

**fNoLineFeed**
</dt> <dd>

Marca que indica si la última `printf` llamada tiene los caracteres de nueva línea ( `\n` ). Si este valor es **true**, la última `printf` llamada no incluía los caracteres de nueva línea.

</dd> <dt>

**fSelfExtract**
</dt> <dd>

Marca que indica si un archivo. cab se está autoextraíble. Si este valor es **true**, el archivo. cab se extrae automáticamente.

</dd> <dt>

**cbSelfExtractSize**
</dt> <dd>

La longitud de la parte ejecutable (. exe) de un archivo. cab autoextraíble.

</dd> <dt>

**cbSelfExtractSize**
</dt> <dd>

La longitud de la parte del archivo. CAB de un archivo. CAB autoextraíble.

</dd> <dt>

**ahfSelf**
</dt> <dd>

Identificadores de archivos del archivo. cab.

`#define cMAX_CAB_FILE_OPEN    2 `

</dd> <dt>

**cErrors**
</dt> <dd>

Recuento de errores encontrados durante la sesión de extracción.

</dd> <dt>

**hfdi**
</dt> <dd>

Identificador del contexto FDI. Este tipo de texto se declara de la siguiente manera:

`typedef void FAR *HFDI; `

</dd> <dt>

**Fun**
</dt> <dd>

La estructura de error FDI. Vea [**Fun**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf).

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

**x300**
</dt> <dd>

Error de archivo de derrame. Este miembro puede ser uno de los valores del siguiente tipo enumerado.

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

Tamaño del archivo de derrame solicitado.

</dd> <dt>

**achSelf**
</dt> <dd>

Nombre del archivo ejecutable (. exe).

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**achMsg**
</dt> <dd>

Búfer de formato del mensaje.

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

Ruta de acceso en la que se va a buscar un archivo. cab.

</dd> <dt>

**fContinuationCabinet**
</dt> <dd>

Marca que indica si el archivo. cab actual es el primero que se procesa. Si se establece en **true**, no se procesa el primer contenedor.

</dd> <dt>

**fShowReserveInfo**
</dt> <dd>

Marca que indica si se debe proporcionar la información de reserva. Si se establece en **true**, la información estará disponible.

</dd> <dt>

**fNextCabCalled**
</dt> <dd>

Este miembro proporciona una manera de determinar cuál de las entradas de **Acab** se va a usar si se procesan todos los archivos de un conjunto de contenedores (**fAllCabinet** se establece en **true**).

</dd> <dt>

**acab**
</dt> <dd>

Las dos últimas entradas del conjunto de contenedores. Esta estructura se define de la siguiente manera:

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

El prefijo que se va a quitar del nombre de archivo.

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**achCabinetFile**
</dt> <dd>

Archivo. cab actual.

`#define cbFILE_NAME_MAX     256`

</dd> <dt>

**cArgv**
</dt> <dd>

Argc predeterminado de extracción automática.

</dd> <dt>

**pArgv**
</dt> <dd>

Un puntero a un puntero a los argv de extracción automática predeterminados \[ \] .

</dd> <dt>

**fDestructive**
</dt> <dd>

Marca que reduce el espacio en disco necesario cuando se establece en **true**.

</dd> <dt>

**iCurrentFolder**
</dt> <dd>

Si **fDestructive** está establecido en **true**, extraiga solo la carpeta actual.

</dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[**DeleteExtractedFiles**](deleteextractedfiles.md)
</dt> <dt>

[**Extracción**](extract.md)
</dt> </dl>

 

 
