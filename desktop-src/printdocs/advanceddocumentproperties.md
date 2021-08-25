---
description: La función AdvancedDocumentProperties muestra un cuadro de diálogo de configuración de impresora para la impresora especificada, lo que permite al usuario configurar esa impresora.
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: Función AdvancedDocumentProperties (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdvancedDocumentProperties
- AdvancedDocumentPropertiesA
- AdvancedDocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 2451f8e0668e0064566511bbf5eeb05e65094967486142719629400cf8d97348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720275"
---
# <a name="advanceddocumentproperties-function"></a>Función AdvancedDocumentProperties

La **función AdvancedDocumentProperties** muestra un cuadro de diálogo de configuración de impresora para la impresora especificada, lo que permite al usuario configurar esa impresora.

Esta función es un caso especial de la [**función DocumentProperties.**](documentproperties.md) Para más información, consulte la sección Comentarios.

## <a name="syntax"></a>Sintaxis


```C++
LONG AdvancedDocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ En\]
</dt> <dd>

Identificador de la ventana primaria del cuadro de diálogo de configuración de impresora.

</dd> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de un objeto de impresora. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pDeviceName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del dispositivo para el que se debe mostrar un cuadro de diálogo de configuración de impresora.

</dd> <dt>

*pDevModeOutput* \[ out\]
</dt> <dd>

Puntero a una [**estructura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contendrá los datos de configuración especificados por el usuario.

</dd> <dt>

*pDevModeInput* \[ En\]
</dt> <dd>

Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contiene los datos de configuración utilizados para inicializar los controles del cuadro de diálogo de configuración de impresora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la [**función DocumentProperties**](documentproperties.md) con estos parámetros es correcta, el valor devuelto de **AdvancedDocumentProperties** es 1. De lo contrario, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

Esta función solo puede mostrar el cuadro de diálogo configuración de impresora para que un usuario pueda configurarla. Para obtener más control, use [**DocumentProperties**](documentproperties.md). Los parámetros de entrada de esta función se pasan directamente a **DocumentProperties** y el valor *fMode* se establece en DM \_ IN BUFFER DM IN PROMPT DM OUT \_ \| \_ \_ \| \_ \_ BUFFER. A **diferencia de DocumentProperties,** esta función solo devuelve 1 o 0. Por lo tanto, no puede determinar el tamaño necesario [**de DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) estableciendo *pDevMode* en cero.

Una aplicación puede obtener el nombre al que apunta el parámetro *pDeviceName* llamando a la función [**GetPrinter**](getprinter.md) y, a continuación, examinando el **miembro pPrinterName** de la [**estructura PRINTER INFO \_ \_ 2.**](printer-info-2.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **AdvancedDocumentPropertiesW** (Unicode) y **AdvancedDocumentPropertiesA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Addprinter**](addprinter.md)
</dt> <dt>

[**Devmode**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**Documentproperties**](documentproperties.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**INFORMACIÓN \_ DE IMPRESORA \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




