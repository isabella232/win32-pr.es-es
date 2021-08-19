---
description: La función CorePrinterDriverInstalled informa de si está instalado un controlador de impresora principal con un GUID, una fecha y una versión especificados.
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: Función CorePrinterDriverInstalled (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 014b9932046ab6d66b64794bbe042f43a390f9f6a4b6183d36a6338eca434526
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719775"
---
# <a name="coreprinterdriverinstalled-function"></a>Función CorePrinterDriverInstalled

La **función CorePrinterDriverInstalled** informa de si está instalado un controlador de impresora principal con un GUID, una fecha y una versión especificados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
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

*CoreDriverGUID* \[ En\]
</dt> <dd>

GUID del controlador de impresora principal.

</dd> <dt>

*ftDriverDate* \[ En\]
</dt> <dd>

Fecha del controlador de impresora principal.

</dd> <dt>

*dwlDriverVersion* \[ En\]
</dt> <dd>

La versión del controlador de impresora principal.

</dd> <dt>

*pbDriverInstalled* \[ out\]
</dt> <dd>

Puntero a **TRUE si** el controlador, o una versión más reciente, está instalado; en caso contrario, **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es S \_ OK; de lo contrario, **HRESULT** contendrá un código de error.

Para obtener más información sobre los códigos de error COM, vea [Control de errores.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nombres Unicode y ANSI<br/>   | **CorePrinterDriverInstalledW** (Unicode) y **CorePrinterDriverInstalledA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

