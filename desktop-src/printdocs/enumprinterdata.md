---
description: La función EnumPrinterData enumera los datos de configuración de una impresora especificada.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: Función EnumPrinterData (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterData
- EnumPrinterDataA
- EnumPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a542b6a0432ccf7065d94eeb8ebb3acbd8e2ace22044f2cc8984a1f4b2404299
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846085"
---
# <a name="enumprinterdata-function"></a>Función EnumPrinterData

La **función EnumPrinterData** enumera los datos de configuración de una impresora especificada.

Para recuperar los datos de configuración en una sola llamada, use la [**función EnumPrinterDataEx.**](enumprinterdataex.md)

## <a name="syntax"></a>Sintaxis


```C++
DWORD EnumPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   dwIndex,
  _Out_ LPTSTR  pValueName,
  _In_  DWORD   cbValueName,
  _Out_ LPDWORD pcbValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbData,
  _Out_ LPDWORD pcbData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora cuyos datos de configuración se obtendrán. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*dwIndex* \[ En\]
</dt> <dd>

Valor de índice que especifica el valor de datos de configuración que se recuperará.

Establezca este parámetro en cero para la primera llamada a **EnumPrinterData para** un identificador de impresora especificado. A continuación, incremente el parámetro en uno para las llamadas posteriores que impliquen la misma impresora, hasta que la función devuelva ERROR \_ NO \_ MORE \_ ITEMS. Consulte la siguiente sección Comentarios para obtener más información.

Si usa la técnica mencionada en las descripciones de los parámetros *cbValueName* y *cbData* para obtener los valores de tamaño de búfer adecuados, estableciendo ambos parámetros en cero en una primera llamada a **EnumPrinterData** para un identificador de impresora especificado, el valor de *dwIndex* no importa para esa llamada. Establezca *dwIndex* en cero en la siguiente llamada a **EnumPrinterData para** iniciar el proceso de enumeración real.

Los valores de datos de configuración no están ordenados. Los nuevos valores tendrán un índice arbitrario. Esto significa que la **función EnumPrinterData** puede devolver valores en cualquier orden.

</dd> <dt>

*pValueName* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe el nombre del valor de datos de configuración, incluido un carácter nulo de terminación.

</dd> <dt>

*cbValueName* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pValueName.*

Si desea que el sistema operativo proporcione un tamaño de búfer adecuado, establezca este parámetro y el parámetro *cbData* en cero para la primera llamada a **EnumPrinterData** para un identificador de impresora especificado. Cuando la función devuelve un resultado, la variable a la que apunta *kbValueName* contendrá un tamaño de búfer lo suficientemente grande como para enumerar correctamente todos los nombres de valor de datos de configuración de la impresora.

</dd> <dt>

*nameValueName* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes almacenados en el búfer al que apunta *pValueName.*

</dd> <dt>

*pType* \[ out\]
</dt> <dd>

Puntero a una variable que recibe un código que indica el tipo de datos almacenados en el valor especificado. Para obtener una lista de los códigos de tipo posibles, vea [Tipos de valor del Registro](/windows/desktop/SysInfo/registry-value-types). El *parámetro pType* puede ser **NULL** si no se requiere el código de tipo.

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe el valor de datos de configuración.

Este parámetro puede ser **NULL si** no se requiere el valor de los datos de configuración.

</dd> <dt>

*cbData* \[ En\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pData*.

Si desea que el sistema operativo proporcione un tamaño de búfer adecuado, establezca este parámetro y el parámetro *cbValueName* en cero para la primera llamada a **EnumPrinterData** para un identificador de impresora especificado. Cuando la función devuelve un resultado, la variable a la que apunta *pwData* contendrá un tamaño de búfer lo suficientemente grande como para enumerar correctamente todos los nombres de valor de datos de configuración de la impresora.

</dd> <dt>

*pwData* \[ out\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes almacenados en el búfer al que apunta *pData*.

Este parámetro puede ser **NULL si** *pData* es **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un código de error del sistema.

La función devuelve ERROR NO MORE ITEMS cuando no hay más valores de datos de configuración que recuperar \_ para un identificador de impresora \_ \_ especificado.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

**EnumPrinterData recupera los** datos de configuración de impresora establecidos por la [**función SetPrinterData.**](setprinterdata.md) Los datos de configuración de una impresora constan de un conjunto de valores con nombre y con tipo. La **función EnumPrinterData** obtiene uno de estos valores, y su nombre y un código de tipo, cada vez que se llama a él. Llame a **la función EnumPrinterData varias** veces seguidas para obtener todos los valores de datos de configuración de una impresora.

Los datos de configuración de impresora se almacenan en el Registro. Al enumerar los datos de configuración de la impresora, debe evitar llamar a funciones del Registro que puedan cambiar los datos.

Si desea que el sistema operativo proporcione un tamaño de búfer adecuado, llame primero a **EnumPrinterData** con los parámetros *cbValueName* y *cbData* establecidos en cero, como se indicó anteriormente en la sección Parámetros. El valor de *dwIndex* no importa para esta llamada. Cuando la función devuelve un \* *resultado,nameValueName* y \* *pwData* contendrán tamaños de búfer lo suficientemente grandes como para enumerar todos los nombres y valores de los valores de los datos de configuración de la impresora. En la siguiente llamada, asigne el nombre de valor y los búferes de datos, establezca *cbValueName* y *cbData* en los tamaños en bytes de los búferes asignados y *establezca dwIndex* en cero. A partir de entonces, continúe con la llamada a la función **EnumPrinterData,** *incrementando dwIndex* en una cada vez, hasta que la función devuelva ERROR \_ NO MORE \_ \_ ITEMS.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **EnumPrinterDataW** (Unicode) y **EnumPrinterDataA** (ANSI)<br/>                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterData**](deleteprinterdata.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> </dl>

 

