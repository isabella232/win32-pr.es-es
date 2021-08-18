---
description: La función DeleteForm quita un nombre de formulario de la lista de formularios admitidos.
ms.assetid: a2d0345f-2469-46ab-935f-777f2b33b621
title: Función DeleteForm (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteForm
- DeleteFormA
- DeleteFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: efd200a06ddea9cd5ec11396741e7ea66fb2d803a273a6d56c9d15c295263247
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112665"
---
# <a name="deleteform-function"></a>Función DeleteForm

La **función DeleteForm** quita un nombre de formulario de la lista de formularios admitidos.

## <a name="syntax"></a>Sintaxis


```C++
BOOL DeleteForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Indica el identificador de impresora abierto en el que se va a realizar esta función. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pFormName* \[ En\]
</dt> <dd>

Puntero al nombre del formulario que se va a quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

**DeleteForm** solo puede eliminar nombres de formulario que se agregaron mediante la [**función AddForm.**](addform.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **DeleteFormW** (Unicode) y **DeleteFormA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




