---
description: Contiene información del controlador de impresora.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: DRIVER_INFO_8 estructura (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_8
- _DRIVER_INFO_8A
- _DRIVER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 753b05b9d59bb98742d5c49102b604cc0a499a4dcdc6c624489d261400279297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234844"
---
# <a name="driver_info_8-structure"></a>Estructura \_ DRIVER INFO \_ 8

Contiene información del controlador de impresora.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DRIVER_INFO_8 {
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
  LPTSTR    pszPrintProcessor;
  LPTSTR    pszVendorSetup;
  LPTSTR    pszzColorProfiles;
  LPTSTR    pszInfPath;
  DWORD     dwPrinterDriverAttributes;
  LPTSTR    pszzCoreDriverDependencies;
  FILETIME  ftMinInboxDriverVerDate;
  DWORDLONG dwlMinInboxDriverVerVersion;
} DRIVER_INFO_8, *PDRIVER_INFO_8, *LPDRIVER_INFO_8;
```



## <a name="members"></a>Miembros

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

Puntero a una cadena terminada en NULL que especifica el entorno para el que se escribió el controlador (por ejemplo, Windows x86, Windows IA64 y Windows x64.

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

Puntero a un búfer MultiSZ que contiene una secuencia de cadenas terminadas en NULL. Cada cadena terminada en NULL del búfer contiene el nombre de un archivo del que depende el controlador. La secuencia de cadenas finaliza con una cadena vacía de longitud cero. Si **pDependentFiles** no es **NULL** y no contiene ningún nombre de archivo, apuntará a un búfer que contiene dos cadenas vacías.

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

Número de versión del controlador. Esto procede de la estructura de versión del controlador.

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

Puntero a una cadena terminada en NULL que especifica el identificador de hardware para el controlador de impresora.

</dd> <dt>

**pszProvider**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el proveedor del controlador de impresora (por ejemplo, "Microsoft Windows 2000").

</dd> <dt>

**pszPrintProcessor**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el procesador de impresión (por ejemplo, "WinPrint").

</dd> <dt>

**pszVendorSetup**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el archivo DLL y el punto de entrada del programa de instalación del controlador del proveedor.

</dd> <dt>

**pszzColorProfiles**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica los perfiles de color asociados al controlador.

</dd> <dt>

**pszInfPath**
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica la ruta de acceso al archivo .inf del controlador en el almacén de controladores. (Vea Comentarios). Debe ser **NULL si** driver INFO 8 se pasa a \_ \_ [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx.**](addprinterdriverex.md)

</dd> <dt>

**dwPrinterDriverAttributes**
</dt> <dd>

Marcas de atributos para los controladores de impresora. Debe ser 0 si driver INFO 8 se pasa a \_ \_ [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md). De lo contrario, puede ser cualquier combinación de las marcas siguientes:



| Nombre y valor de marca                                                         | Significado                                                                                                                                                                                                                                                                                                                                             | So mínimo                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| CONTROLADOR DE \_ IMPRESORA QUE TIENE EN CUENTA EL \_ \_ PAQUETE<br/> 0x00000001<br/>        | El controlador de impresora forma parte de un paquete de controladores.                                                                                                                                                                                                                                                                                                     | Windows Vista                                          |
| XPS \_ DEL \_ CONTROLADOR DE IMPRESORA<br/> 0x00000002<br/>                   | El controlador de impresora admite el formato XPS de Microsoft descrito en [XML Paper Specification: Información](/previous-versions/windows/hardware/design/dn641615(v=vs.85))general y también en Comportamiento del producto, sección [<27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).                        | Windows 8<br/> Windows Server 2012<br/>    |
| ESPACIO AISLADO \_ DEL CONTROLADOR DE IMPRESORA \_ \_ HABILITADO<br/> 0x00000004<br/>      | El controlador de impresora es compatible con el [aislamiento del controlador de impresora](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24). Para obtener más información, vea [Comportamiento del producto, sección <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43). | Windows 7<br/> Windows Server 2008 R2<br/> |
| PRINTER \_ DRIVER \_ CLASS<br/> 0x00000008<br/>                 | El controlador de impresora es un [controlador de impresora de clase](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                       | Windows 8<br/> Windows Server 2012<br/>    |
| CONTROLADOR \_ DE IMPRESORA \_ DERIVADO<br/> 0x00000010<br/>               | El controlador de impresora es [un controlador de impresora derivado.](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)                                                                                                                                                                                   | Windows 8<br/> Windows Server 2012<br/>    |
| CONTROLADOR \_ DE IMPRESORA NO \_ \_ COMPARTIBLE<br/> 0x00000020<br/>        | Las impresoras que usan este controlador de impresora no se pueden compartir.                                                                                                                                                                                                                                                                                                | Windows 8<br/> Windows Server 2012<br/>    |
| FAX DE \_ CATEGORÍA DEL CONTROLADOR DE \_ \_ IMPRESORA<br/> 0x00000040<br/>         | El controlador de impresora está pensado para su uso con [impresoras de fax.](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)                                                                                                                                                                                    | Windows 8<br/> Windows Server 2012<br/>    |
| ARCHIVO DE \_ CATEGORÍA DEL CONTROLADOR DE \_ \_ IMPRESORA<br/> 0x00000080<br/>        | El controlador de impresora está pensado para su uso con [impresoras de archivos](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                  | Windows 8<br/> Windows Server 2012<br/>    |
| CATEGORÍA \_ DEL CONTROLADOR DE IMPRESORA \_ \_ VIRTUAL<br/> 0x00000100<br/>     | El controlador de impresora está pensado para su uso con [impresoras virtuales.](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24)                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| SERVICIO DE \_ CATEGORÍA DE CONTROLADOR DE \_ \_ IMPRESORA<br/> 0x00000200<br/>     | El controlador de impresora está pensado para su uso con [impresoras de servicio](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| SE REQUIERE \_ EL \_ RESTABLECIMIENTO \_ DE SOFTWARE DEL CONTROLADOR \_ DE IMPRESORA<br/> 0x00000400<br/> | Las impresoras que usan este controlador de impresora deben seguir las instrucciones descritas en la definición de la clase de dispositivo USB. Para obtener más información, vea [Comportamiento del producto, sección <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)                                                                      | Windows 8<br/> Windows Server 2012<br/>    |



 

</dd> <dt>

**pszzCoreDriverDependencies**
</dt> <dd>

Puntero a una cadena múltiple terminada en NULL que especifica todos los controladores de impresora principales de los que depende el controlador. Debe ser **NULL si** driver INFO **\_ \_ 8** se pasa a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx.**](addprinterdriverex.md)

</dd> <dt>

**ftMinInboxDriverVerDate**
</dt> <dd>

La fecha más temprana permitida de todos los controladores incluidos con Windows y de los que depende este controlador.

</dd> <dt>

**dwlMinInboxDriverVerVersion**
</dt> <dd>

La versión más antigua permitida de todos los controladores incluidos con Windows y de los que depende este controlador.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las cadenas de estos miembros están contenidas en el archivo .inf que se usa para agregar el controlador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ DRIVER \_ INFO \_ 8W** (Unicode) e **\_ DRIVER INFO \_ \_ 8A** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del colador de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 

