---
description: La función ConfigurePort muestra el cuadro de diálogo port-configuration de un puerto en el servidor especificado.
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
title: Función ConfigurePort (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurePort
- ConfigurePortA
- ConfigurePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: dbc31de341c137e8baf729a468e8576684ccef8b0a860be898c9cb5a6af34217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950445"
---
# <a name="configureport-function"></a>Función ConfigurePort

La **función ConfigurePort** muestra el cuadro de diálogo port-configuration de un puerto en el servidor especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL ConfigurePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del servidor en el que existe el puerto especificado. Si este parámetro es **NULL,** el puerto es local.

</dd> <dt>

*hWnd* \[ En\]
</dt> <dd>

Identificador en la ventana primaria del cuadro de diálogo configuración de puerto.

</dd> <dt>

*pPortName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del puerto que se va a configurar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Antes de llamar **a la función ConfigurePort,** una aplicación debe llamar a [**la función EnumPorts**](enumports.md) para determinar los nombres de puerto válidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **ConfigurePortW** (Unicode) y **ConfigurePortA** (ANSI)<br/>                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




