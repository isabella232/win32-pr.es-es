---
description: Recupera la ruta de acceso al paquete de controladores de impresora especificado en un servidor de impresión.
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: Función GetPrinterDriverPackagePath (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverPackagePath
- GetPrinterDriverPackagePathA
- GetPrinterDriverPackagePathW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5058d57a0275019c5e603673d260c9969cc0b5d5641dea15e09ffe242addff10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600805"
---
# <a name="getprinterdriverpackagepath-function"></a>Función GetPrinterDriverPackagePath

Recupera la ruta de acceso al paquete de controladores de impresora especificado en un servidor de impresión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPrinterDriverPackagePath(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszEnvironment,
  _In_    LPCTSTR pszLanguage,
  _In_    LPCTSTR pszPackageID,
  _Inout_ LPTSTR  pszDriverPackageCab,
  _In_    DWORD   cchDriverPackageCab,
  _Out_   LPDWORD pcchRequiredSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszServer* \[ En\]
</dt> <dd>

Puntero a una cadena constante terminada en NULL que especifica el nombre del servidor de impresión. Use **NULL** para el equipo local.

</dd> <dt>

*pszEnvironment* \[ En\]
</dt> <dd>

Puntero a una cadena constante terminada en NULL que especifica la arquitectura del procesador (por ejemplo, Windows NT x86). Puede ser **NULL.**

</dd> <dt>

*pszLanguage* \[ En\]
</dt> <dd>

Puntero a una cadena constante terminada en NULL que especifica el [Interfaz de usuario multilingüe](/windows/desktop/Intl/mui-resource-management) idioma del controlador que se va a instalar. Puede ser **NULL.**

</dd> <dt>

*pszPackageID* \[ En\]
</dt> <dd>

Puntero a una cadena constante terminada en NULL que especifica el identificador del paquete de controladores.

</dd> <dt>

*pszDriverPackageCab* \[ in, out\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica la ruta de acceso al archivo de archivador para el paquete de controladores. Puede ser **NULL.** Vea la sección Comentarios.

</dd> <dt>

*cchDriverPackageCab* \[ En\]
</dt> <dd>

Tamaño, en caracteres, del *búfer pszDriverPackageCab.* Puede ser **NULL.**

</dd> <dt>

*pcchRequiredSize* \[ out\]
</dt> <dd>

Puntero al tamaño necesario del búfer *pszDriverPackageCab.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es S OK; de \_ lo **contrario, HRESULT** contendrá un código de error.

Para obtener más información sobre los códigos de error COM, vea [Control de errores.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Para obtener un valor para *cchDriverPackageCab*, llame a la función **con NULL** como el valor de *pszDriverPackageCab*. Use el valor devuelto en *pcchRequiredSize* como valor de *cchDriverPackageCab* y llame a la función de nuevo.

*PszPackageID* normalmente se obtiene de una llamada a [**GetCorePrinterDrivers.**](getcoreprinterdrivers.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nombres Unicode y ANSI<br/>   | **GetPrinterDriverPackagePathW** (Unicode) y **GetPrinterDriverPackagePathA** (ANSI)<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

