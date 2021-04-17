---
description: La estructura de la información de controlador \_ \_ 2 identifica un controlador de impresora, el número de versión del controlador, el entorno para el que se escribió el controlador, el nombre del archivo en el que está almacenado el controlador, etc.
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
title: Estructura de DRIVER_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_2
- _DRIVER_INFO_2A
- _DRIVER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: a88caf5aa10828b81dccefbe8118b3a57aebce97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716028"
---
# <a name="driver_info_2-structure"></a>Estructura de la información de controlador \_ \_ 2

La estructura de la **información de controlador \_ \_ 2** identifica un controlador de impresora, el número de versión del controlador, el entorno para el que se escribió el controlador, el nombre del archivo en el que está almacenado el controlador, etc.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DRIVER_INFO_2 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
} DRIVER_INFO_2, *PDRIVER_INFO_2;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cVersion**
</dt> <dd>

Versión del sistema operativo para el que se escribió el controlador. El valor admitido es 3.

</dd> <dt>

**pName**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el nombre del controlador (por ejemplo, "QMS 810").

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el entorno para el que se escribió el controlador (por ejemplo, Windows x86, Windows IA64 y Windows x64).

</dd> <dt>

**pDriverPath**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene el controlador de dispositivo (por ejemplo, "c: \\ drivers \\pscript.dll").

</dd> <dt>

**pDataFile**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene los datos del controlador (por ejemplo, "c: \\ drivers \\ Qms810. PPD").

</dd> <dt>

**pConfigFile**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para Configuration. dll del controlador de dispositivo (por ejemplo, "c: \\ drivers \\Pscrptui.dll").

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ Información del controlador \_ \_ 2W** (Unicode) y la **\_ información del controlador \_ \_ 2A** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




