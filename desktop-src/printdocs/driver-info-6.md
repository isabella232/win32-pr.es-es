---
description: La estructura de la información del controlador \_ \_ 6 contiene información sobre el controlador de impresora.
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: Estructura de DRIVER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_6
- _DRIVER_INFO_6A
- _DRIVER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20edef2aca2c6948984f5195b16711b78112354a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697131"
---
# <a name="driver_info_6-structure"></a>Estructura de información de controlador \_ \_ 6

La estructura de la **información del controlador \_ \_ 6** contiene información sobre el controlador de impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DRIVER_INFO_6 {
  DWORD     cVersion;
  LPTSTR    pName;
  LPTSTR    pEnvironment;
  LPTSTR    pDriverPath;
  LPTSTR    pDataFile;
  LPTSTR    pConfigFile;
  LPTSTR    pHelpFile;
  LPTSTR    pDependentFiles;
  LPTSTR    pMonitorName;
  LPTSTR    pDefaultDataType;
  LPTSTR    pszzPreviousNames;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  LPTSTR    pszMfgName;
  LPTSTR    pszOEMUrl;
  LPTSTR    pszHardwareID;
  LPTSTR    pszProvider;
} DRIVER_INFO_6, *PDRIVER_INFO_6, *LPDRIVER_INFO_6;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cVersion**
</dt> <dd>

Versión del sistema operativo para el que se escribió el controlador. El valor admitido es 3.

</dd> <dt>

**pName**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del controlador (por ejemplo, QMS 810).

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el entorno para el que se escribió el controlador (por ejemplo, Windows NT x86, Windows IA64 y Windows x64).

</dd> <dt>

**pDriverPath**
</dt> <dd>

Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene el controlador de dispositivo (por ejemplo, C: \\ DRIVERS \\Pscript.dll).

</dd> <dt>

**pDataFile**
</dt> <dd>

Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene los datos del controlador (por ejemplo, C: \\ drivers \\ Qms810. PPD).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para la biblioteca de vínculos dinámicos de configuración del controlador del dispositivo (por ejemplo, C: \\ DRIVERS \\Pscrptui.dll).

</dd> <dt>

**pHelpFile**
</dt> <dd>

Puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo de ayuda del controlador del dispositivo (por ejemplo, C: \\ drivers \\ Pscrptui. hlp).

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Un puntero a un búfer MultiSZ que contiene una secuencia de cadenas terminadas en NULL. Cada cadena terminada en NULL del búfer contiene el nombre de un archivo del que depende el controlador. La secuencia de cadenas termina en una cadena vacía de longitud cero. Si **pDependentFiles** no es **null** y no contiene ningún nombre de archivo, apuntará a un búfer que contenga dos cadenas vacías.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica un monitor de idioma (por ejemplo, "monitor PJL"). Este miembro puede ser **null** y debe especificarse solo para impresoras capaces de comunicación bidireccional.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el tipo de datos predeterminado del trabajo de impresión (por ejemplo, "EMF").

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

Puntero a una cadena terminada en null que especifica los nombres de controladores de impresora anteriores que son compatibles con este controlador. Por ejemplo, OldName1 \\ 0OldName2 \\ 0 \\ 0.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

La fecha del paquete de controladores, como se codifica en los archivos del controlador.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

Número de versión del controlador. Esto sale de la estructura de la versión del controlador.

</dd> <dt>

**pszMfgName**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del fabricante.

</dd> <dt>

**pszOEMUrl**
</dt> <dd>

Puntero a una cadena terminada en null que especifica la dirección URL del fabricante.

</dd> <dt>

**pszHardwareID**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el identificador de hardware para el controlador de impresora.

</dd> <dt>

**pszProvider**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el proveedor del controlador de impresora (por ejemplo, "Microsoft Windows 2000")

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las cadenas de estos miembros se encuentran en el archivo. inf que se utiliza para agregar el controlador.

Si llama a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md) con un *nivel* distinto de 6 y, a continuación, llama a [**GetPrinterDriver**](getprinterdriver.md) o [**EnumPrinterDrivers**](enumprinterdrivers.md) con un *nivel* igual a 6, la estructura de la **información del controlador \_ \_ 6** se devuelve con **pszMfgName**, **pszOEMUrl**, **pszHardwareID** y **pszProvider** establecidos en **null**, **dwlDriverVersion** establecido en 0 y **ftDriverDate** establecido en (0,0).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ Información del controlador \_ \_ 6W** (Unicode) y la **\_ información del controlador \_ \_ 6A** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




