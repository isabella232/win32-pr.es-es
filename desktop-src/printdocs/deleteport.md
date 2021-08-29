---
description: La función DeletePort muestra un cuadro de diálogo que permite al usuario eliminar un nombre de puerto.
ms.assetid: 5f5788c2-c781-4106-abd2-98556d0a22de
title: Función DeletePort (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePort
- DeletePortA
- DeletePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fd1c54e6daa70ed3bfdb7c748f470da45f38445ca2588d97d2b195906b957b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950085"
---
# <a name="deleteport-function"></a>Función DeletePort

La **función DeletePort** muestra un cuadro de diálogo que permite al usuario eliminar un nombre de puerto.

## <a name="syntax"></a>Sintaxis


```C++
BOOL DeletePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en cero que especifica el nombre del servidor para el que se debe eliminar el puerto. Si este parámetro es **NULL,** se elimina un puerto local.

</dd> <dt>

*hWnd* \[ En\]
</dt> <dd>

Identificador de la ventana primaria del cuadro de diálogo de eliminación de puertos.

</dd> <dt>

*pPortName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en cero que especifica el nombre del puerto que se debe eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Una aplicación puede recuperar los nombres de puertos válidos llamando a la [**función EnumPorts.**](enumports.md)

La **función DeletePort** devuelve un error si una impresora está conectada actualmente al puerto especificado.

El autor de la llamada **de la función DeletePort** debe tener acceso SERVER ACCESS ADMINISTER al servidor al \_ que está conectado el \_ puerto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **DeletePortW** (Unicode) y **DeletePortA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPort**](addport.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




