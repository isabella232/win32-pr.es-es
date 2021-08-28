---
description: La función GetForm recupera información sobre un formulario especificado.
ms.assetid: 10b25748-6d7c-46ab-bd2c-9b6126a1d7d1
title: Función GetForm (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetForm
- GetFormA
- GetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: bf5263d0de24d86053f8293f2fc9f6c410519ddef568cec9f4692223166e6ab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971444"
---
# <a name="getform-function"></a>Función GetForm

La **función GetForm** recupera información sobre un formulario especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL GetForm(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pFormName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pFormName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del formulario. Para obtener los nombres de los formularios admitidos por la impresora, llame a la [**función EnumForms.**](enumforms.md)

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Versión de la estructura a la que *apunta pForm.* Este valor debe ser 1 o 2.

</dd> <dt>

*pForm* \[ out\]
</dt> <dd>

Puntero a una matriz de bytes que recibe la estructura [**FORM \_ INFO \_ 1**](form-info-1.md) o [**FORM INFO \_ \_ 2 inicializada.**](form-info-2.md)

</dd> <dt>

*cbBuf* \[ En\]
</dt> <dd>

Tamaño, en bytes, de la *matriz pForm.*

</dd> <dt>

*pwNeeded* \[ out\]
</dt> <dd>

Puntero a un valor que especifica el número de bytes copiados si la función se realiza correctamente o el número de bytes necesarios si *cbBuf* es demasiado pequeño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Si el autor de la llamada es remoto y *level* es 2, el valor **StringType** del [**FORMULARIO INFO \_ \_ 2**](form-info-2.md) devuelto siempre será STRING \_ LANGPAIR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **GetFormW** (Unicode) y **GetFormA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**DeleteForm**](deleteform.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

 




