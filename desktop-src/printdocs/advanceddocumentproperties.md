---
description: La función AdvancedDocumentProperties muestra un cuadro de diálogo de configuración de impresora para la impresora especificada, lo que permite al usuario configurar esa impresora.
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: Función AdvancedDocumentProperties (winspool. h)
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
ms.openlocfilehash: da8754add6e3f5997354c940c303c41d4588c7b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817771"
---
# <a name="advanceddocumentproperties-function"></a>AdvancedDocumentProperties función)

La función **AdvancedDocumentProperties** muestra un cuadro de diálogo de configuración de impresora para la impresora especificada, lo que permite al usuario configurar esa impresora.

Esta función es un caso especial de la función [**DocumentProperties**](documentproperties.md) . Para obtener más información, vea la sección Comentarios.

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

*hWnd* \[ de\]
</dt> <dd>

Identificador de la ventana primaria del cuadro de diálogo de configuración de la impresora.

</dd> <dt>

*hPrinter* \[ de\]
</dt> <dd>

Identificador de un objeto de impresora. Use la función [**OpenPrinter**](openprinter.md) o [**AddPrinter (**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pDeviceName* \[ de\]
</dt> <dd>

Un puntero a una cadena terminada en null que especifica el nombre del dispositivo para el que se debe mostrar un cuadro de diálogo de configuración de impresora.

</dd> <dt>

*pDevModeOutput* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contendrá los datos de configuración especificados por el usuario.

</dd> <dt>

*pDevModeInput* \[ de\]
</dt> <dd>

Puntero a una estructura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contiene los datos de configuración que se utilizan para inicializar los controles del cuadro de diálogo de configuración de la impresora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función [**DocumentProperties**](documentproperties.md) con estos parámetros es correcta, el valor devuelto de **AdvancedDocumentProperties** es 1. De lo contrario, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y podría no volver inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que parezca que la aplicación no responde.

 

Esta función solo puede mostrar el cuadro de diálogo Configuración de impresora para que un usuario pueda configurarlo. Para obtener más control, utilice [**DocumentProperties**](documentproperties.md). Los parámetros de entrada de esta función se pasan directamente a **DocumentProperties** y el valor *fMode* se establece en DM \_ en \_ buffer \| DM en el \_ \_ \| búfer DM \_ out \_ . A diferencia de **DocumentProperties**, esta función solo devuelve 1 o 0. Por lo tanto, no se puede determinar el tamaño necesario de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) estableciendo *pDevMode* en cero.

Una aplicación puede obtener el nombre al que apunta el parámetro *pDeviceName* llamando a la función [**GetPrinter**](getprinter.md) y, a continuación, examinando el miembro **pPrinterName** de la estructura de la información de la [**impresora \_ \_ 2**](printer-info-2.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **AdvancedDocumentPropertiesW** (Unicode) y **AdvancedDocumentPropertiesA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter (**](addprinter.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**DocumentProperties**](documentproperties.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Información de la impresora \_ \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




