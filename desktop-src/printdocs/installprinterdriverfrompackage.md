---
description: Instala un controlador de impresora desde un paquete de controladores que se encuentra en el almacén de controladores del servidor de impresión.
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: Función InstallPrinterDriverFromPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallPrinterDriverFromPackage
- InstallPrinterDriverFromPackageA
- InstallPrinterDriverFromPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f817f5e73537f6a71d8236ad9532acdf02a53552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279026"
---
# <a name="installprinterdriverfrompackage-function"></a>InstallPrinterDriverFromPackage función)

Instala un controlador de impresora desde un paquete de controladores que se encuentra en el almacén de controladores del servidor de impresión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InstallPrinterDriverFromPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszDriverName,
  _In_ LPCTSTR pszEnvironment,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszServer* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica el nombre del servidor de impresión. **Null** significa el equipo local.

</dd> <dt>

*pszInfPath* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica la ruta de acceso del almacén de controladores al archivo. inf del controlador de impresión. **Null** significa que el controlador está en un archivo INF que se incluye con Windows.

</dd> <dt>

*pszDriverName* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica el nombre del controlador.

</dd> <dt>

*pszEnvironment* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica la arquitectura del procesador (por ejemplo, Windows NT x86). Puede ser **null**.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Solo puede ser 0 o IPDFP \_ copiar \_ todos los \_ archivos. Un valor de 0 significa que el controlador de impresora debe agregarse y se deben copiar todos los archivos del directorio de controladores de impresora que sean más recientes que los archivos correspondientes actualmente en uso. Un valor de IPDFP \_ copiar \_ todos \_ los archivos significa que se debe agregar el controlador de impresora y todos los archivos del directorio de controladores de impresora. Las marcas de tiempo de archivo se omiten cuando *dwFlags* tiene un valor de IPDFP \_ copiar \_ todos \_ los archivos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es S \_ OK; de lo contrario, **HRESULT** contendrá un código de error.

Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

El almacén de controladores suele ser% WINDIR% \\ inf o% WINDIR% \\ system32 \\ DriverStore \\ FileRepository.

**InstallPrinterDriverFromPackage** también instala otros archivos en el paquete, como perfiles de color y procesadores de impresión.

Los usuarios deben tener derechos de administración de impresoras para instalar en un equipo remoto o en el equipo local cuando el usuario inicia sesión con Terminal Services.

Solo los paquetes firmados se pueden instalar en un equipo remoto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nombres Unicode y ANSI<br/>   | **InstallPrinterDriverFromPackageW** (Unicode) y **InstallPrinterDriverFromPackageA** (ANSI)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

