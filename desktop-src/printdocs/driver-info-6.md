---
description: La estructura DRIVER \_ INFO \_ 6 contiene información del controlador de impresora.
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: DRIVER_INFO_6 estructura (Winspool.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361098"
---
# <a name="driver_info_6-structure"></a>Estructura \_ DRIVER INFO \_ 6

La **estructura DRIVER INFO \_ \_ 6** contiene información del controlador de impresora.

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

Puntero a una cadena terminada en NULL que especifica el entorno para el que se escribió el controlador (por ejemplo, Windows NT x86, Windows IA64 y Windows x64.

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

**pHelpFile**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo de ayuda del controlador de dispositivo (por ejemplo, C: \\ DRIVERS \\ Pscrptui.hlp).

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Puntero a un búfer MultiSZ que contiene una secuencia de cadenas terminadas en NULL. Cada cadena terminada en NULL del búfer contiene el nombre de un archivo del que depende el controlador. Una cadena vacía de longitud cero finaliza la secuencia de cadenas. Si **pDependentFiles** no es **NULL** y no contiene ningún nombre de archivo, apuntará a un búfer que contiene dos cadenas vacías.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica un monitor de lenguaje (por ejemplo, "monitor PJL"). Este miembro puede ser **NULL** y debe especificarse solo para impresoras que puedan comunicarse bidireccionalmente.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el tipo de datos predeterminado del trabajo de impresión (por ejemplo, "EMF").

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica nombres de controladores de impresora anteriores que son compatibles con este controlador. Por ejemplo, OldName1 \\ 0OldName2 \\ 0 \\ 0.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

Fecha del paquete de controladores, como se codifica en los archivos de controlador.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

Número de versión del controlador. Esto sale de la estructura de versión del controlador.

</dd> <dt>

**pszMfgName**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del fabricante.

</dd> <dt>

**pszOEMUrl**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica la dirección URL del fabricante.

</dd> <dt>

**pszHardwareID**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el identificador de hardware del controlador de impresora.

</dd> <dt>

**pszProvider**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el proveedor del controlador de impresora (por ejemplo, "Microsoft Windows 2000")

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las cadenas de estos miembros están contenidas en el archivo .inf que se usa para agregar el controlador.

Si llama  a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md) con *level* no igual a 6 y, a continuación, llama a [**GetPrinterDriver**](getprinterdriver.md) o [**EnumPrinterDrivers**](enumprinterdrivers.md) con Level igual a 6, la estructura DRIVER INFO **\_ \_ 6** se devuelve con **pszMfgName**, **pszOEMUrl**, **pszHardwareID y** **pszProvider** establecido en **NULL,** **dwlDriverVersion** establecido en 0 y **ftDriverDate** establecido en (0,0).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ DRIVER \_ INFO \_ 6W** (Unicode) e **\_ DRIVER INFO \_ \_ 6A** (ANSI)<br/>                             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API de Spooler de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> <dt>

[**GetPrinterDriver**](getprinterdriver.md)
</dt> </dl>

 

 




