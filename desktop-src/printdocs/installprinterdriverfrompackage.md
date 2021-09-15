---
description: Instala un controlador de impresora desde un paquete de controladores que se encuentra en el almacén de controladores de servidores de impresión.
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: Función InstallPrinterDriverFromPackage (Winspool.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568641"
---
# <a name="installprinterdriverfrompackage-function"></a>Función InstallPrinterDriverFromPackage

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

*pszServer* \[ En\]
</dt> <dd>

Puntero a una cadena constante terminada en NULL que especifica el nombre del servidor de impresión. **NULL significa** el equipo local.

</dd> <dt>

*pszInfPath* \[ En\]
</dt> <dd>

Puntero a una cadena constante terminada en NULL que especifica la ruta de acceso del almacén de controladores al archivo .inf del controlador de impresión. **NULL** significa que el controlador está en un archivo inf que se incluye con Windows.

</dd> <dt>

*pszDriverName* \[ En\]
</dt> <dd>

Puntero a una cadena constante terminada en NULL que especifica el nombre del controlador.

</dd> <dt>

*pszEnvironment* \[ En\]
</dt> <dd>

Puntero a una cadena constante terminada en NULL que especifica la arquitectura del procesador (por ejemplo, Windows NT x86). Puede ser **NULL.**

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Solo puede ser 0 o IPDFP \_ COPY \_ ALL \_ FILES. Un valor de 0 significa que se debe agregar el controlador de impresora y se deben copiar todos los archivos del directorio del controlador de impresora que sean más recientes que los archivos correspondientes actualmente en uso. Un valor de IPDFP COPY ALL FILES significa que se debe agregar el controlador de impresora y todos los archivos del directorio del controlador \_ \_ de \_ impresora. Las marcas de tiempo de archivo se omiten *cuando dwFlags* tiene un valor de IPDFP \_ COPY ALL \_ \_ FILES.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es S \_ OK; de lo contrario, **HRESULT** contendrá un código de error.

Para obtener más información sobre los códigos de error COM, vea [Control de errores.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

El almacén de controladores suele ser %windir% inf o \\ %windir% \\ System32 \\ DriverStore \\ FileRepository.

**InstallPrinterDriverFromPackage** también instala otros archivos en el paquete, como perfiles de color y procesadores de impresión.

Los usuarios deben tener derechos de administración de impresoras para instalar en un equipo remoto o en el equipo local cuando el usuario haya iniciado sesión con Terminal Services.

Solo se pueden instalar paquetes firmados en un equipo remoto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nombres Unicode y ANSI<br/>   | **InstallPrinterDriverFromPackageW** (Unicode) e **InstallPrinterDriverFromPackageA** (ANSI)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

