---
description: La función EnumPrinterData enumera los datos de configuración de una impresora especificada.
ms.assetid: 0a4c8436-46fe-4e21-8d55-c5031a3d1b38
title: Función EnumPrinterData (winspool. h)
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
ms.openlocfilehash: d7c175b0c90853a592e0ff979095d41432c16b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276661"
---
# <a name="enumprinterdata-function"></a>EnumPrinterData función)

La función **EnumPrinterData** enumera los datos de configuración de una impresora especificada.

Para recuperar los datos de configuración en una sola llamada, utilice la función [**EnumPrinterDataEx**](enumprinterdataex.md) .

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

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora cuyos datos de configuración se van a obtener. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*dwIndex* \[ de\]
</dt> <dd>

Valor de índice que especifica el valor de los datos de configuración que se va a recuperar.

Establezca este parámetro en cero para la primera llamada a **EnumPrinterData** para un identificador de impresora especificado. A continuación, incremente el parámetro en uno para las llamadas posteriores que impliquen la misma impresora, hasta que la función devuelva el ERROR \_ no \_ más \_ elementos. Vea la siguiente sección de comentarios para obtener más información.

Si usa la técnica mencionada en las descripciones de los parámetros *cbValueName* y *cbData* para obtener los valores de tamaño de búfer adecuados, al establecer ambos parámetros en cero en una primera llamada a **EnumPrinterData** para un identificador de impresora especificado, el valor de *dwIndex* no es relevante para esa llamada. Establezca *dwIndex* en cero en la siguiente llamada a **EnumPrinterData** para iniciar el proceso de enumeración real.

Los valores de los datos de configuración no están ordenados. Los valores nuevos tendrán un índice arbitrario. Esto significa que la función **EnumPrinterData** puede devolver valores en cualquier orden.

</dd> <dt>

*pValueName* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe el nombre del valor de los datos de configuración, incluido un carácter nulo de terminación.

</dd> <dt>

*cbValueName* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pValueName*.

Si desea que el sistema operativo proporcione un tamaño de búfer adecuado, establezca este parámetro y el parámetro *cbData* en cero para la primera llamada a **EnumPrinterData** para un identificador de impresora especificado. Cuando la función devuelve, la variable a la que apunta *pcbValueName* contendrá un tamaño de búfer que es lo suficientemente grande como para enumerar correctamente todos los nombres de los valores de los datos de configuración de la impresora.

</dd> <dt>

*pcbValueName* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes almacenados en el búfer al que apunta *pValueName*.

</dd> <dt>

*pType* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe un código que indica el tipo de datos almacenados en el valor especificado. Para obtener una lista de los códigos de tipo posibles, vea [Registry Value Types](/windows/desktop/SysInfo/registry-value-types). El parámetro *pType* puede ser **null** si no se requiere el código de tipo.

</dd> <dt>

*pdata* \[ enuncia\]
</dt> <dd>

Un puntero a un búfer que recibe el valor de los datos de configuración.

Este parámetro puede ser **null** si el valor de los datos de configuración no es necesario.

</dd> <dt>

*cbData* \[ de\]
</dt> <dd>

Tamaño, en bytes, del búfer al que apunta *pdata*.

Si desea que el sistema operativo proporcione un tamaño de búfer adecuado, establezca este parámetro y el parámetro *cbValueName* en cero para la primera llamada a **EnumPrinterData** para un identificador de impresora especificado. Cuando la función devuelve, la variable a la que apunta *pcbData* contendrá un tamaño de búfer que es lo suficientemente grande como para enumerar correctamente todos los nombres de los valores de los datos de configuración de la impresora.

</dd> <dt>

*pcbData* \[ enuncia\]
</dt> <dd>

Puntero a una variable que recibe el número de bytes almacenados en el búfer al que apunta *pdata*.

Este parámetro puede ser **null** si *pdata* es **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error del sistema.

La función devuelve el ERROR \_ no hay \_ más \_ elementos cuando no hay más valores de datos de configuración para recuperar en un identificador de impresora especificado.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

**EnumPrinterData** recupera los datos de configuración de la impresora establecidos por la función [**SetPrinterData**](setprinterdata.md) . Los datos de configuración de una impresora se componen de un conjunto de valores con nombre y con tipo. La función **EnumPrinterData** obtiene uno de estos valores, y su nombre y código de tipo, cada vez que lo llame. Llame a la función **EnumPrinterData** varias veces consecutivas para obtener todos los valores de datos de configuración de una impresora.

Los datos de configuración de la impresora se almacenan en el registro. Al enumerar los datos de configuración de la impresora, debe evitar llamar a las funciones del registro que podrían cambiar los datos.

Si desea que el sistema operativo proporcione un tamaño de búfer adecuado, llame primero a **EnumPrinterData** con los parámetros *cbValueName* y *cbData* establecidos en cero, como se indicó anteriormente en la sección de parámetros. El valor de *dwIndex* no es relevante para esta llamada. Cuando la función devuelve, \* *pcbValueName* y \* *pcbData* contendrán tamaños de búfer lo suficientemente grandes como para enumerar todos los valores y nombres de los datos de configuración de la impresora. En la siguiente llamada, asigne el nombre de valor y los búferes de datos, establezca *cbValueName* y *cbData* en los tamaños en bytes de los búferes asignados y establezca *dwIndex* en cero. Después, continúe llamando a la función **EnumPrinterData** , incrementando *dwIndex* en uno cada vez, hasta que la función devuelva el error \_ no \_ más \_ elementos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
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

 

