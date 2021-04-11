---
description: Contiene información del controlador de impresora.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: Estructura de DRIVER_INFO_8 (winspool. h)
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
ms.openlocfilehash: 3cc174fdc8617a8ff59afc5a12740eaba715114f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361417"
---
# <a name="driver_info_8-structure"></a>Estructura de información de controlador \_ \_ 8

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

Versión del sistema operativo para el que se escribió el controlador. El valor admitido es 3.

</dd> <dt>

**pName**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el nombre del controlador (por ejemplo, QMS 810).

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntero a una cadena terminada en null que especifica el entorno para el que se escribió el controlador (por ejemplo, Windows x86, Windows IA64 y Windows x64).

</dd> <dt>

**pDriverPath**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene el controlador de dispositivo (por ejemplo, C: \\ DRIVERS \\Pscript.dll).

</dd> <dt>

**pDataFile**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo que contiene los datos del controlador (por ejemplo, C: \\ drivers \\ Qms810. PPD).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para la biblioteca de vínculos dinámicos de configuración del controlador del dispositivo (por ejemplo, C: \\ DRIVERS \\Pscrptui.dll).

</dd> <dt>

**pHelpFile**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica un nombre de archivo o una ruta de acceso completa y un nombre de archivo para el archivo de ayuda del controlador del dispositivo (por ejemplo, C: \\ drivers \\ Pscrptui. hlp).

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

Número de versión del controlador. Procede de la estructura de la versión del controlador.

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

Un puntero a una cadena terminada en null que especifica el proveedor del controlador de impresora (por ejemplo, "Microsoft Windows 2000").

</dd> <dt>

**pszPrintProcessor**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el procesador de impresión (por ejemplo, "WinPrint").

</dd> <dt>

**pszVendorSetup**
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el punto de entrada y la DLL de instalación del controlador del proveedor.

</dd> <dt>

**pszzColorProfiles**
</dt> <dd>

Puntero a una cadena terminada en null que especifica los perfiles de color asociados al controlador.

</dd> <dt>

**pszInfPath**
</dt> <dd>

Puntero a una cadena terminada en null que especifica la ruta de acceso al archivo. inf del controlador en el almacén de controladores. (Vea la sección comentarios). Debe ser **null** si la información del \_ controlador \_ 8 se pasa a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md).

</dd> <dt>

**dwPrinterDriverAttributes**
</dt> <dd>

Marcas de atributo para controladores de impresora. Debe ser 0 si la información del \_ controlador \_ 8 se pasa a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md). De lo contrario, puede ser cualquier combinación de las marcas siguientes:



| Nombre/valor de marca                                                         | Significado                                                                                                                                                                                                                                                                                                                                             | SO mínimo                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| paquete de controlador de impresora \_ \_ \_ compatible<br/> 0x00000001<br/>        | El controlador de impresora forma parte de un paquete de controladores.                                                                                                                                                                                                                                                                                                     | Windows Vista                                          |
| controlador de impresora \_ \_ XPS<br/> 0x00000002<br/>                   | El controlador de impresora admite el formato XPS de Microsoft que se describe en la [especificación de XML Paper: información general](/previous-versions/windows/hardware/design/dn641615(v=vs.85))y también en el [comportamiento del producto, sección <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).                        | Windows 8<br/> Windows Server 2012<br/>    |
| \_ \_ espacio aislado habilitado del controlador de impresora \_<br/> 0x00000004<br/>      | El controlador de impresora es compatible con el [aislamiento de controladores de impresora](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24). Para obtener más información, vea el tema sobre el [comportamiento del producto, la sección <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43). | Windows 7<br/> Windows Server 2008 R2<br/> |
| \_clase de controlador de impresora \_<br/> 0x00000008<br/>                 | El controlador de impresora es un [controlador de impresora de clase](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                       | Windows 8<br/> Windows Server 2012<br/>    |
| controlador de impresora \_ \_ derivado<br/> 0x00000010<br/>               | El controlador de impresora es un [controlador de impresora derivado](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                   | Windows 8<br/> Windows Server 2012<br/>    |
| controlador de impresora \_ \_ no \_ compartible<br/> 0x00000020<br/>        | Las impresoras que usan este controlador de impresora no se pueden compartir.                                                                                                                                                                                                                                                                                                | Windows 8<br/> Windows Server 2012<br/>    |
| \_fax de \_ categoría de controlador de impresora \_<br/> 0x00000040<br/>         | El controlador de impresora está diseñado para su uso con [impresoras de fax](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                    | Windows 8<br/> Windows Server 2012<br/>    |
| \_archivo de \_ categoría del controlador de impresora \_<br/> 0x00000080<br/>        | El controlador de impresora está pensado para su uso con [impresoras de archivos](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                  | Windows 8<br/> Windows Server 2012<br/>    |
| Categoría de controlador de impresora \_ \_ \_ virtual<br/> 0x00000100<br/>     | El controlador de impresora está pensado para su uso con [impresoras virtuales](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| \_servicio de \_ categoría de controlador de impresora \_<br/> 0x00000200<br/>     | El controlador de impresora está pensado para su uso con [impresoras de servicio](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| se \_ \_ \_ requiere restablecimiento parcial del controlador de impresora \_<br/> 0x00000400<br/> | Las impresoras que usan este controlador de impresora deben seguir las instrucciones descritas en la definición de clase de dispositivo USB. Para obtener más información, vea el tema sobre el [comportamiento del producto, la sección <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)                                                                      | Windows 8<br/> Windows Server 2012<br/>    |



 

</dd> <dt>

**pszzCoreDriverDependencies**
</dt> <dd>

Puntero a una cadena múltiple terminada en null que especifica todos los controladores de impresora principales de los que depende el controlador. Debe ser **null** si la **información del \_ controlador \_ 8** se pasa a [**AddPrinterDriver**](addprinterdriver.md) o [**AddPrinterDriverEx**](addprinterdriverex.md).

</dd> <dt>

**ftMinInboxDriverVerDate**
</dt> <dd>

La fecha más temprana permitida de los controladores incluidos en Windows y de los que depende este controlador.

</dd> <dt>

**dwlMinInboxDriverVerVersion**
</dt> <dd>

La versión más temprana permitida de los controladores que se incluyen con Windows y de los que depende este controlador.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las cadenas de estos miembros se encuentran en el archivo. inf que se utiliza para agregar el controlador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **\_ Información del controlador \_ \_ 8W** (Unicode) y la **\_ información del controlador \_ \_ 8A** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 

