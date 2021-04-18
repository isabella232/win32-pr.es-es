---
description: Recupera la ruta de acceso al paquete de controladores de impresora especificado en un servidor de impresión.
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: Función GetPrinterDriverPackagePath (winspool. h)
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
ms.openlocfilehash: ea355782df6cce7910f92a46af3cde320536106e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707229"
---
# <a name="getprinterdriverpackagepath-function"></a>GetPrinterDriverPackagePath función)

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

*pszServer* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica el nombre del servidor de impresión. Use **null** para el equipo local.

</dd> <dt>

*pszEnvironment* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica la arquitectura del procesador (por ejemplo, Windows NT x86). Puede ser **null**.

</dd> <dt>

*pszLanguage* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica el idioma de la [interfaz de usuario multilingüe](/windows/desktop/Intl/mui-resource-management) para el controlador que se va a instalar. Puede ser **null**.

</dd> <dt>

*pszPackageID* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica el identificador del paquete de controladores.

</dd> <dt>

*pszDriverPackageCab* \[ in, out\]
</dt> <dd>

Un puntero a una cadena terminada en null que especifica la ruta de acceso al archivo. cab para el paquete de controladores. Puede ser **null**. Vea la sección Comentarios.

</dd> <dt>

*cchDriverPackageCab* \[ de\]
</dt> <dd>

Tamaño, en caracteres, del búfer *pszDriverPackageCab* . Puede ser **null**.

</dd> <dt>

*pcchRequiredSize* \[ enuncia\]
</dt> <dd>

Puntero al tamaño requerido del búfer de *pszDriverPackageCab* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es S \_ OK; de lo contrario, **HRESULT** contendrá un código de error.

Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Para obtener un valor para *cchDriverPackageCab*, llame a la función con **null** como el valor de *pszDriverPackageCab*. Use el valor devuelto en *pcchRequiredSize* como el valor de *cchDriverPackageCab* y vuelva a llamar a la función.

El *pszPackageID* se suele obtener de una llamada a [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nombres Unicode y ANSI<br/>   | **GetPrinterDriverPackagePathW** (Unicode) y **GetPrinterDriverPackagePathA** (ANSI)<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

