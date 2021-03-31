---
description: La función AddPrinterConnection agrega una conexión a la impresora especificada para el usuario actual.
ms.assetid: 6decf89a-1411-4e7e-aa20-60e7068658c2
title: Función AddPrinterConnection (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection
- AddPrinterConnectionA
- AddPrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: dae1f823f89b69526218ab4c027642fb54e3cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911182"
---
# <a name="addprinterconnection-function"></a>AddPrinterConnection función)

La función **AddPrinterConnection** agrega una conexión a la impresora especificada para el usuario actual.

## <a name="syntax"></a>Sintaxis


```C++
BOOL AddPrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre de una impresora a la que el usuario actual desea establecer una conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Cuando Windows establece una conexión con una impresora, puede que tenga que copiar los archivos del controlador de impresora en el servidor al que está conectada la impresora. Si el usuario no tiene permiso para copiar archivos en la ubicación adecuada, se produce un error en la función **AddPrinterConnection** y [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve el error \_ acceso \_ denegado.

Una conexión de impresora establecida mediante una llamada a **AddPrinterConnection** se enumerará cuando se llame a [**EnumPrinters**](enumprinters.md) con *dwType* establecido en \_ conexión de enumeración de impresora \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **AddPrinterConnectionW** (Unicode) y **AddPrinterConnectionA** (ANSI)<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**ConnectToPrinterDlg**](connecttoprinterdlg.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> </dl>

 

