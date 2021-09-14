---
description: La función StartDocPrinter notifica al administrador de trabajos de impresión que un documento se va a colar para imprimirlo.
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
title: Función StartDocPrinter (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartDocPrinter
- StartDocPrinterA
- StartDocPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f8bdb0ae08c88e553dad3a91f0f1a578bed4ad39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361094"
---
# <a name="startdocprinter-function"></a>Función StartDocPrinter

La **función StartDocPrinter** notifica al administrador de trabajos de impresión que un documento se va a colar para imprimirlo.

## <a name="syntax"></a>Sintaxis


```C++
DWORD StartDocPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pDocInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPrinter* \[ En\]
</dt> <dd>

Identificador de la impresora. Use la [**función OpenPrinter**](openprinter.md) [**o AddPrinter**](addprinter.md) para recuperar un identificador de impresora.

</dd> <dt>

*Nivel* \[ En\]
</dt> <dd>

Versión de la estructura a la que *apunta pDocInfo.* Este valor debe ser 1.

</dd> <dt>

*pDocInfo* \[ En\]
</dt> <dd>

Puntero a una [**estructura DOC \_ INFO \_ 1**](doc-info-1.md) que describe el documento que se imprimirá.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto identifica el trabajo de impresión.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Se trata de una función de bloqueo o sincrónica y es posible que no se devuelva inmediatamente. La rapidez con la que se devuelve esta función depende de factores en tiempo de ejecución, como el estado de la red, la configuración del servidor de impresión y los factores de implementación del controlador de impresora que son difíciles de predecir al escribir una aplicación. Llamar a esta función desde un subproceso que administra la interacción con la interfaz de usuario podría hacer que la aplicación parezca no responder.

 

La secuencia típica para un trabajo de impresión es la siguiente:

1.  Para iniciar un trabajo de impresión, llame **a StartDocPrinter**.
2.  Para comenzar cada página, llame [**a StartPagePrinter**](startpageprinter.md).
3.  Para escribir datos en una página, llame a [**WritePrinter**](writeprinter.md).
4.  Para finalizar cada página, llame a [**EndPagePrinter**](endpageprinter.md).
5.  Repita 2, 3 y 4 para tantas páginas como sea necesario.
6.  Para finalizar el trabajo de impresión, llame a [**EndDocPrinter**](enddocprinter.md).

Tenga en cuenta que puede que no sea necesario llamar a [**StartPagePrinter**](startpageprinter.md) y [**EndPagePrinter,**](endpageprinter.md) por ejemplo, si el tipo de datos de impresión incluye la información de la página.

Cuando una página de un archivo en cola supera aproximadamente 350 MB, puede no imprimirse y no enviar un mensaje de error. Por ejemplo, esto puede ocurrir al imprimir archivos EMF grandes. El límite de tamaño de página depende de muchos factores, como la cantidad de memoria virtual disponible, la cantidad de memoria asignada mediante la llamada a procesos y la cantidad de fragmentación en el montón de procesos.

## <a name="examples"></a>Ejemplos

Para obtener un programa de ejemplo que use esta función, [vea Cómo: Imprimir mediante la API de impresión de GDI.](how-to--print-using-the-gdi-print-api.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| Archivo DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nombres Unicode y ANSI<br/>   | **StartDocPrinterW** (Unicode) e **StartDocPrinterA** (ANSI)<br/>                                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**DOC \_ INFO \_ 1**](doc-info-1.md)
</dt> <dt>

[**DOC \_ INFO \_ 2**](doc-info-2.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Funciones de la API del administrador de trabajos de impresión](printing-and-print-spooler-functions.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




