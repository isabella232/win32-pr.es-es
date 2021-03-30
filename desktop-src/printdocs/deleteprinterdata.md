---
description: La función DeletePrinterData elimina los datos de configuración especificados para una impresora. Los datos de configuración de las impresoras se componen de un conjunto de valores con nombre y con tipo. La función DeletePrinterData elimina uno de estos valores, especificado por su nombre de valor.
ms.assetid: 03c0bd75-d6de-46e3-b8e9-5a55df5135ea
title: Función DeletePrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterData
- DeletePrinterDataA
- DeletePrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a88df8484d367ae2cc50f4a465b5db1dcd53c355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360661"
---
# <a name="deleteprinterdata-function"></a>DeletePrinterData función)

La función **DeletePrinterData** elimina los datos de configuración especificados para una impresora. Los datos de configuración de una impresora se componen de un conjunto de valores con nombre y con tipo. La función **DeletePrinterData** elimina uno de estos valores, especificado por su nombre de valor.

Llamar a **DeletePrinterData** es equivalente a llamar a la función [**DeletePrinterDataEx**](deleteprinterdataex.md) con el parámetro *pKeyName* establecido en "PrinterDriverData".

## <a name="syntax"></a>Sintaxis


```C++
DWORD DeletePrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ de\]
</dt> <dd>

Identificador de la impresora cuyos datos de configuración se van a eliminar. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pValueName* \[ de\]
</dt> <dd>

Puntero al nombre terminado en NULL del valor de datos de configuración que se va a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.

Si se produce un error en la función, el valor devuelto es un código de error del sistema.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **DeletePrinterDataW** (Unicode) y **DeletePrinterDataA** (ANSI)<br/>                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPrinterData**](enumprinterdata.md)
</dt> <dt>

[**GetPrinterData**](getprinterdata.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinter**](setprinter.md)
</dt> <dt>

[**SetPrinterData**](setprinterdata.md)
</dt> </dl>

 

 




