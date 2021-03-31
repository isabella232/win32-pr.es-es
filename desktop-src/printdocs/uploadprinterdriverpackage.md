---
description: Carga un controlador de impresora en el almacén de controladores de los servidores de impresión para que se pueda instalar llamando a InstallPrinterDriverFromPackage.
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: Función UploadPrinterDriverPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UploadPrinterDriverPackage
- UploadPrinterDriverPackageA
- UploadPrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f616c4f731d3a416806f499a513f48466263f441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278643"
---
# <a name="uploadprinterdriverpackage-function"></a>UploadPrinterDriverPackage función)

Carga un controlador de impresora en el almacén de controladores del servidor de impresión para que se pueda instalar llamando a [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UploadPrinterDriverPackage(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszInfPath,
  _In_    LPCTSTR pszEnvironment,
  _In_    DWORD   dwFlags,
  _In_    HWND    hwnd,
  _Out_   LPTSTR  pszDestInfPath,
  _Inout_ PULONG  pcchDestInfPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszServer* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica el nombre del servidor de impresión. Use **null** si el servidor es el equipo local.

</dd> <dt>

*pszInfPath* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica la ruta de acceso de origen al archivo. inf del controlador.

</dd> <dt>

*pszEnvironment* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica la arquitectura de procesador del servidor (por ejemplo, Windows NT x86). Puede ser **null**.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Puede ser cualquiera de los siguientes valores:



| Value                                                                                                                                                                                     | Significado                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <dt>**UPDP_SILENT_UPLOAD**</dt> </dl>             | La interfaz de usuario no se mostrará durante la carga.<br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <dt>**UPDP_UPLOAD_ALWAYS**</dt> </dl>             | Los archivos se cargarán incluso si el paquete ya está en el almacén de controladores del servidor.<br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <dt>**UPDP_CHECK_DRIVERSTORE**</dt> </dl> | El almacén de controladores del servidor se comprobará antes de la carga para ver si el paquete ya está allí. Este valor se omite si se establece UPDP_UPLOAD_ALWAYS.<br/> |



 

</dd> <dt>

*hWnd* \[ de\]
</dt> <dd>

Identificador de la interfaz de usuario que se va a copiar.

</dd> <dt>

*pszDestInfPath* \[ enuncia\]
</dt> <dd>

Un puntero a la ruta de acceso de destino, en el almacén de controladores, donde se copió el archivo. inf del controlador.

</dd> <dt>

*pcchDestInfPath* \[ in, out\]
</dt> <dd>

En la entrada, especifica el tamaño, en caracteres, del búfer de *pszDestInfPath* . En la salida, recibe el tamaño, en caracteres, de la cadena de ruta de acceso, incluido el carácter nulo de terminación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es S_OK; de lo contrario, **HRESULT** contendrá un código de error.

Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

El almacén de controladores suele ser% WINDIR% \\ inf o% WINDIR% \\ system32 \\ DriverStore \\ FileRepository.

Solo se puede cargar un paquete a la vez. Si un paquete depende de otros, debe cargarse por separado.

Solo se pueden cargar paquetes de controladores firmados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nombres Unicode y ANSI<br/>   | **UploadPrinterDriverPackageW** (Unicode) y **UploadPrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

