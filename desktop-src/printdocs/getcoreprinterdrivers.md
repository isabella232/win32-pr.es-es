---
description: Recupera el GUID, la versión y la fecha de los controladores de impresora principales especificados y la ruta de acceso a sus paquetes.
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
title: Función GetCorePrinterDrivers (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCorePrinterDrivers
- GetCorePrinterDriversA
- GetCorePrinterDriversW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 7cca2a8d96b521cb18013afae7dbab571fe02544273ec4943706f829ec841e45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949175"
---
# <a name="getcoreprinterdrivers-function"></a>Función GetCorePrinterDrivers

Recupera el GUID, la versión y la fecha de los controladores de impresora principales especificados y la ruta de acceso a sus paquetes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCorePrinterDrivers(
  _In_  LPCTSTR              pszServer,
  _In_  LPCTSTR              pszEnvironment,
  _In_  LPCTSTR              pszzCoreDriverDependencies,
  _In_  DWORD                cCorePrinterDrivers,
  _Out_ PCORE_PRINTER_DRIVER pCorePrinterDrivers
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

*pszzCoreDriverDependencies* \[ En\]
</dt> <dd>

Puntero a una cadena múltiple terminada en NULL que especifica los GUID de los controladores de impresora principales.

</dd> <dt>

*cCorePrinterDrivers* \[ En\]
</dt> <dd>

Número de cadenas de *pszzCoreDriverDependencies.*

</dd> <dt>

*pCorePrinterDrivers* \[ out\]
</dt> <dd>

Puntero a una matriz de una o varias estructuras [**CORE \_ PRINTER \_ DRIVER.**](core-printer-driver.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es S OK; de \_ lo **contrario, HRESULT** contendrá un código de error.

Para obtener más información sobre los códigos de error COM, vea [Control de errores.](../com/error-handling-in-com.md)

## <a name="remarks"></a>Comentarios

Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nombres Unicode y ANSI<br/>   | **GetCorePrinterDriversW** (Unicode) y **GetCorePrinterDriversA** (ANSI)<br/>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

