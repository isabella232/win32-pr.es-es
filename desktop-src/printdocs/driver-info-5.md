---
description: La estructura DRIVER \_ INFO \_ 5 contiene información del controlador de impresora.
ms.assetid: 6fb63a9f-5227-46a3-97dc-8de1968e9d63
title: DRIVER_INFO_5 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_5
- _DRIVER_INFO_5A
- _DRIVER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 11281e69b70b2d87d354138a6313c8bca6673944
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358964"
---
# <a name="driver_info_5-structure"></a>Estructura \_ DRIVER INFO \_ 5

La **estructura DRIVER INFO \_ \_ 5** contiene información del controlador de impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DRIVER_INFO_5 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  DWORD  dwDriverAttributes;
  DWORD  dwConfigVersion;
  DWORD  dwDriverVersion;
} DRIVER_INFO_5, *PDRIVER_INFO_5;
```



## <a name="members"></a>Members

<dl> <dt>

**cVersion**
</dt> <dd>

Versión del sistema operativo para la que se escribió el controlador. El valor admitido es 3.

</dd> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del controlador (por ejemplo, QMS 810).

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el entorno para el que se escribió el controlador (por ejemplo, Windows x86, Windows IA64 y Windows x64).

</dd> <dt>

**pDriverPath**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene el controlador de dispositivo (por ejemplo, C: \\ CONTROLADORES \\Pscript.dll).

</dd> <dt>

**pDataFile**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene datos de controlador (por ejemplo, C: \\ DRIVERS \\ Qms810.ppd).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para la biblioteca de vínculos dinámicos de configuración del controlador de dispositivo (por ejemplo, C: \\ CONTROLADORES \\Pscrptui.dll).

</dd> <dt>

**dwDriverAttributes**
</dt> <dd>

Atributos de controlador, como UMPD/KMPD.

</dd> <dt>

**dwConfigVersion**
</dt> <dd>

Número de veces que el archivo de configuración de este controlador se ha actualizado o degradado desde el último reinicio del administrador de trabajos de cola.

</dd> <dt>

**dwDriverVersion**
</dt> <dd>

Número de veces que el archivo de controlador para este controlador se ha actualizado o degradado desde el último reinicio del administrador de trabajos de cola.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ DRIVER \_ INFO \_ 5W** (Unicode) e **\_ DRIVER INFO \_ \_ 5A** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




