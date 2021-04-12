---
description: La función EnumForms enumera los formatos admitidos por la impresora especificada.
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: Función EnumForms (winspool. h)
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
ms.openlocfilehash: 18cd9ad6f8e0491700d5618e29a0a629e8045366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360659"
---
# <a name="enumforms-function"></a>EnumForms función)

La función **EnumForms** enumera los formatos admitidos por la impresora especificada.

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

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora para la que se deben enumerar los formularios. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*Nivel* \[ de de\]
</dt> <dd>

Especifica la versión de la estructura a la que apunta *pForm* . Este valor debe ser 1 o 2.

</dd> <dt>

*pForm* \[ enuncia\]
</dt> <dd>

Puntero a una o varias estructuras de [**Form \_ info \_ 1**](form-info-1.md) o a una o varias estructuras de [**Form \_ info \_ 2**](form-info-2.md) . Todas las estructuras tendrán el mismo nivel.

</dd> <dt>

*cbBuf* \[ de\]
</dt> <dd>

Especifica el tamaño, en bytes, del búfer al que apunta *pForm* .

</dd> <dt>

*pcbNeeded* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes copiados en la matriz a la que *pForm* apunta (si la operación se realiza correctamente) o el número de bytes necesarios (si se produce un error porque *cbBuf* es demasiado pequeño).

</dd> <dt>

*pcReturned* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número de estructuras copiadas en la matriz a la que apunta *pForm* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Si el autor de la llamada es remoto y el *nivel* es 2, el valor de **StringType** de las estructuras devueltas de la [**información del formulario \_ \_ 2**](form-info-2.md) será siempre **String \_ LANGPAIR**.

En Windows Vista, los datos del formulario devueltos por **EnumForms** se recuperan de una caché local cuando *hPrinter* hace referencia a un servidor de impresión remoto o a una impresora hospedada por un servidor de impresión y hay al menos una conexión abierta a una impresora en el servidor de impresión remoto. En todas las demás configuraciones, se consultan los datos del formulario desde el servidor de impresión remoto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **EnumFormsW** (Unicode) y **EnumFormsA** (ANSI)<br/>                                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter (**](addprinter.md)
</dt> <dt>

[**Información de formulario \_ \_ 1**](form-info-1.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




