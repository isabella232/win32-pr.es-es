---
description: La función ConnectToPrinterDlg muestra un cuadro de diálogo que permite a los usuarios examinar impresoras de una red y conectarse a estas.
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: Función ConnectToPrinterDlg (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectToPrinterDlg
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9af428533d111300d31f6529a0a030fc3b81ee7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168086"
---
# <a name="connecttoprinterdlg-function"></a>Función ConnectToPrinterDlg

La **función ConnectToPrinterDlg** muestra un cuadro de diálogo que permite a los usuarios examinar impresoras de una red y conectarse a estas. Si el usuario selecciona una impresora, la función intenta crear una conexión a ella. Si no hay un controlador adecuado instalado en el servidor, el usuario tiene la opción de crear una impresora localmente.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwnd* \[ En\]
</dt> <dd>

Especifica la ventana primaria del cuadro de diálogo.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Este parámetro está reservado y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente y el usuario selecciona una impresora, el valor devuelto es un identificador para la impresora seleccionada.

Si se produce un error en la función o el usuario cancela el cuadro de diálogo sin seleccionar una impresora, el valor devuelto es **NULL.**

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

La **función ConnectToPrinterDlg** intenta crear una conexión a la impresora seleccionada. Sin embargo, si el servidor en el que reside la impresora no tiene instalado un controlador adecuado, la función ofrece al usuario la opción de crear una impresora localmente. Una aplicación de llamada puede determinar si la función ha creado una impresora localmente llamando a [**GetPrinter**](getprinter.md) con una estructura [**PRINTER INFO \_ \_ 2**](printer-info-2.md) y, a continuación, examinando el miembro Attributes de **esa** estructura.

Una aplicación debe llamar a [**DeletePrinter para**](deleteprinter.md) eliminar una impresora local. Una aplicación debe llamar a [**DeletePrinterConnection para**](deleteprinterconnection.md) eliminar una conexión a una impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>WinSpool.drv</dt> </dl>                   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterConnection**](addprinterconnection.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




