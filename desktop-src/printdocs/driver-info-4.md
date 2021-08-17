---
description: La estructura DRIVER \_ INFO \_ 4 contiene información del controlador de impresora.
ms.assetid: 63000de6-74e7-4427-98d7-7bbd2dd61080
title: DRIVER_INFO_4 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_4
- _DRIVER_INFO_4A
- _DRIVER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d42f74ce58c126130bd28820283c0b4262d3e3ce6b05106ae9ff74bc280ae234
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119353935"
---
# <a name="driver_info_4-structure"></a>Driver \_ INFO \_ 4 (estructura)

La **estructura DRIVER INFO \_ \_ 4** contiene información del controlador de impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DRIVER_INFO_4 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  LPTSTR pHelpFile;
  LPTSTR pDependentFiles;
  LPTSTR pMonitorName;
  LPTSTR pDefaultDataType;
  LPTSTR pszzPreviousNames;
} DRIVER_INFO_4, *PDRIVER_INFO_4;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cVersion**
</dt> <dd>

Versión del sistema operativo para la que se escribió el controlador. El valor admitido es 3.

</dd> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del controlador (por ejemplo, "QMS 810").

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

Puntero a una cadena terminada en NULL que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene los datos del controlador (por ejemplo, C: \\ DRIVERS \\ Qms810.ppd).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para la biblioteca de vínculos dinámicos de configuración del controlador de dispositivo (por ejemplo, C: \\ CONTROLADORES \\Pscrptui.dll).

</dd> <dt>

**pHelpFile**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo de ayuda del controlador de dispositivo.

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Puntero a un búfer MultiSZ que contiene una secuencia de cadenas terminadas en NULL. Cada cadena terminada en NULL en el búfer contiene el nombre de un archivo del que depende el controlador. La secuencia de cadenas finaliza con una cadena vacía de longitud cero. Si **pDependentFiles** no es **NULL** y no contiene ningún nombre de archivo, apuntará a un búfer que contiene dos cadenas vacías.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica un monitor de lenguaje (por ejemplo, monitor de PJL). Este miembro puede ser **NULL** y debe especificarse solo para impresoras que puedan comunicarse bidireccionalmente.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el tipo de datos predeterminado del trabajo de impresión (por ejemplo, EMF).

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica nombres de controladores de impresora anteriores que son compatibles con este controlador. Por ejemplo, OldName1 \\ 0OldName2 \\ 0 \\ 0.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ DRIVER \_ INFO \_ 4W** (Unicode) e **\_ DRIVER INFO \_ \_ 4A** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de LA API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




