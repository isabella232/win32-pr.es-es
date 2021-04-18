---
description: La función ConnectToPrinterDlg muestra un cuadro de diálogo que permite a los usuarios examinar y conectarse a las impresoras de una red.
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: Función ConnectToPrinterDlg (winspool. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678375"
---
# <a name="connecttoprinterdlg-function"></a>ConnectToPrinterDlg función)

La función **ConnectToPrinterDlg** muestra un cuadro de diálogo que permite a los usuarios examinar y conectarse a las impresoras de una red. Si el usuario selecciona una impresora, la función intenta crear una conexión con ella. Si no hay un controlador adecuado instalado en el servidor, el usuario tiene la opción de crear una impresora localmente.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ de\]
</dt> <dd>

Especifica la ventana primaria del cuadro de diálogo.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Este parámetro está reservado y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente y el usuario selecciona una impresora, el valor devuelto es un identificador de la impresora seleccionada.

Si se produce un error en la función o el usuario cancela el cuadro de diálogo sin seleccionar una impresora, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

La función **ConnectToPrinterDlg** intenta crear una conexión a la impresora seleccionada. Sin embargo, si el servidor en el que reside la impresora no tiene instalado un controlador adecuado, la función ofrece al usuario la opción de crear una impresora localmente. Una aplicación que realiza la llamada puede determinar si la función ha creado una impresora localmente llamando a [**GetPrinter**](getprinter.md) con una estructura de [**\_ información \_ 2**](printer-info-2.md) de la impresora y, a continuación, examinando el miembro de **atributos** de la estructura.

Una aplicación debe llamar a [**DeletePrinter**](deleteprinter.md) para eliminar una impresora local. Una aplicación debe llamar a [**DeletePrinterConnection**](deleteprinterconnection.md) para eliminar una conexión a una impresora.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |



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

[**Información de la impresora \_ \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




