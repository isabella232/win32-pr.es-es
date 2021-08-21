---
description: La función WritePrinter notifica al administrador de trabajos de impresión que los datos se deben escribir en la impresora especificada.
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: Función WritePrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WritePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 4b8b413854f8634477f7fec9010f4306587a093bd5c791b1b7d0117b6c3ef91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971164"
---
# <a name="writeprinter-function"></a>Función WritePrinter

La **función WritePrinter** notifica al administrador de trabajos de impresión que los datos se deben escribir en la impresora especificada.

> [!Note]  
> **WritePrinter solo** admite la impresión GDI y no se debe usar para la impresión XPS. Si el trabajo de impresión usa XPS o la ruta de impresión OpenXPS, use [xps Print API](/windows/desktop/printdocs/xps-printing). No se admite el envío de trabajos de impresión XPS o OpenXPS al colador mediante **WritePrinter** y puede dar lugar a resultados indeterminados.

 

## <a name="syntax"></a>Sintaxis


```C++
BOOL WritePrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*pBuf* \[ En\]
</dt> <dd>

Puntero a una matriz de bytes que contiene los datos que se deben escribir en la impresora.

</dd> <dt>

*cbBuf* \[ En\]
</dt> <dd>

Tamaño, en bytes, de la matriz.

</dd> <dt>

*pcWritten* \[ out\]
</dt> <dd>

Puntero a un valor que recibe el número de bytes de datos que se escribieron en la impresora.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un valor distinto de cero.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

La secuencia de un trabajo de impresión es la siguiente:

1.  Para comenzar un trabajo de impresión, llame [**a StartDocPrinter**](startdocprinter.md).
2.  Para comenzar cada página, llame a [**StartPagePrinter**](startpageprinter.md).
3.  Para escribir datos en una página, llame a **WritePrinter**.
4.  Para finalizar cada página, llame a [**EndPagePrinter**](endpageprinter.md).
5.  Repita 2, 3 y 4 para tantas páginas como sea necesario.
6.  Para finalizar el trabajo de impresión, llame [**a EndDocPrinter**](enddocprinter.md).

Cuando un documento de alto nivel (por ejemplo, un archivo de Adobe PDF o Microsoft Word) u otros datos de impresora (como PCL, PS o HPGL) se envían directamente a una impresora, la configuración de impresión definida en el documento precede sobre Windows de impresión. Los documentos se devuelven cuando el valor del miembro *pDatatype* de la estructura [**DOC INFO \_ \_ 1**](doc-info-1.md) que se pasó en el *parámetro pDocInfo* de la llamada [**a StartDocPrinter**](startdocprinter.md) es "RAW" debe describir completamente la configuración del trabajo de impresión [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)-style en el lenguaje comprendido por el hardware.

En versiones de Windows anteriores a Windows XP, cuando una página de un archivo en cola supera aproximadamente 350 MB, puede no imprimirse y no enviar un mensaje de error. Por ejemplo, esto puede ocurrir al imprimir archivos EMF grandes. El límite de tamaño de página en las versiones de Windows anteriores a Windows XP depende de muchos factores, como la cantidad de memoria virtual disponible, la cantidad de memoria asignada mediante la llamada a procesos y la cantidad de fragmentación en el montón de procesos. En Windows XP y versiones posteriores de Windows, los archivos EMF deben tener un tamaño de 2 GB o menos. Si **writePrinter se** usa para escribir datos que no son EMF, como la PDL lista para impresora, el tamaño del archivo solo está limitado por el espacio en disco disponible.

## <a name="examples"></a>Ejemplos

Para obtener un programa de ejemplo que use esta función, [vea Cómo: Imprimir mediante la API de impresión de GDI.](how-to--print-using-the-gdi-print-api.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

