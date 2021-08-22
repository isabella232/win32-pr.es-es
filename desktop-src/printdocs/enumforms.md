---
description: La función EnumForms enumera los formularios admitidos por la impresora especificada.
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: Función EnumForms (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumForms
- EnumFormsA
- EnumFormsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c1e5ce18e81e4d775fdc801517867491740a7dd5035fc730226cb084e5af7d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118732703"
---
# <a name="enumforms-function"></a>Función EnumForms

La **función EnumForms** enumera los formularios admitidos por la impresora especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL EnumForms(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora para la que se deben enumerar los formularios. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Especifica la versión de la estructura a la que *apunta pForm.* Este valor debe ser 1 o 2.

</dd> <dt>

*pForm* \[ out\]
</dt> <dd>

Puntero a una o varias estructuras [**de FORM \_ INFO \_ 1**](form-info-1.md) o a una o varias estructuras [**de FORM INFO \_ \_ 2.**](form-info-2.md) Todas las estructuras tendrán el mismo nivel.

</dd> <dt>

*cbBuf* \[ En\]
</dt> <dd>

Especifica el tamaño, en bytes, del búfer al que *apunta pForm.*

</dd> <dt>

*pwNeeded* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes copiados en la matriz a la que *apunta pForm* (si la operación se realiza correctamente) o el número de bytes necesarios (si se produce un error porque *cbBuf* es demasiado pequeño).

</dd> <dt>

*pcReturned* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de estructuras copiadas en la matriz a la que *apunta pForm.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Si el autor de la llamada es remoto y *level* es 2, el valor **StringType** de las estructuras [**DE FORM INFO \_ \_ 2**](form-info-2.md) devueltas siempre será **STRING \_ LANGPAIR.**

En Windows Vista, los datos de formulario devueltos por **EnumForms** se recuperan de una caché local cuando *hPrinter* hace referencia a un servidor de impresión remoto o a una impresora hospedada por un servidor de impresión y hay al menos una conexión abierta a una impresora en el servidor de impresión remoto. En todas las demás configuraciones, los datos del formulario se consultan desde el servidor de impresión remoto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **EnumFormsW** (Unicode) y **EnumFormsA** (ANSI)<br/>                                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinter**](addprinter.md)
</dt> <dt>

[**FORM \_ INFO \_ 1**](form-info-1.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




