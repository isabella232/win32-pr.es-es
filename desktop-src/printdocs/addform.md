---
description: La función AddForm agrega un formulario a la lista de formularios disponibles que se pueden seleccionar para la impresora especificada.
ms.assetid: 17b59019-f93a-4b57-86fb-91c61aecbac4
title: Función AddForm (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddForm
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2de3ddbdc57a5a41bac048a94a8175cd124df4ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263116"
---
# <a name="addform-function"></a>Función AddForm

La **función AddForm** agrega un formulario a la lista de formularios disponibles que se pueden seleccionar para la impresora especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddForm(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pForm
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora que admite la impresión con el formulario especificado. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Nivel de la estructura a la que *apunta pForm.* Este valor debe ser 1 o 2.

</dd> <dt>

*pForm* \[ En\]
</dt> <dd>

Puntero a una [**estructura FORM \_ INFO \_ 1**](form-info-1.md) [**o FORM INFO \_ \_ 2.**](form-info-2.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Una aplicación puede determinar qué formularios están disponibles para una impresora mediante una llamada a la [**función EnumForms.**](enumforms.md)

Si *pForm* apunta a [**FORM INFO \_ \_ 2,**](form-info-2.md) **AddForm** producirá un error si ya existe un formulario con el nombre especificado o el valor *pKeyword* de la estructura ya existe.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumForms**](enumforms.md)
</dt> <dt>

[**FORM \_ INFO \_ 1**](form-info-1.md)
</dt> <dt>

[**FORM \_ INFO \_ 2**](form-info-2.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




