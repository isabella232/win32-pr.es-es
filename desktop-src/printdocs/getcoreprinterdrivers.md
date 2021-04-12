---
description: Recupera el GUID, la versión y la fecha de los controladores de impresora principales especificados y la ruta de acceso a sus paquetes.
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
title: Función GetCorePrinterDrivers (winspool. h)
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
ms.openlocfilehash: 5bdebc3f4b716a21c56c9ec756ff56c02765d1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360656"
---
# <a name="getcoreprinterdrivers-function"></a>GetCorePrinterDrivers función)

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

*pszServer* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica el nombre del servidor de impresión. Use **null** para el equipo local.

</dd> <dt>

*pszEnvironment* \[ de\]
</dt> <dd>

Puntero a una cadena constante terminada en null que especifica la arquitectura del procesador (por ejemplo, Windows NT x86). Puede ser **null**.

</dd> <dt>

*pszzCoreDriverDependencies* \[ de\]
</dt> <dd>

Puntero a una cadena múltiple terminada en null que especifica los GUID de los controladores de impresora principales.

</dd> <dt>

*cCorePrinterDrivers* \[ de\]
</dt> <dd>

Número de cadenas de *pszzCoreDriverDependencies*.

</dd> <dt>

*pCorePrinterDrivers* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de una o varias estructuras [**principales \_ del \_ controlador de impresora**](core-printer-driver.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la operación se realiza correctamente, el valor devuelto es S \_ OK; de lo contrario, **HRESULT** contendrá un código de error.

Para obtener más información sobre los códigos de error COM, vea [control de errores](../com/error-handling-in-com.md).

## <a name="remarks"></a>Observaciones

Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nombres Unicode y ANSI<br/>   | **GetCorePrinterDriversW** (Unicode) y **GetCorePrinterDriversA** (ANSI)<br/>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> </dl>

 

