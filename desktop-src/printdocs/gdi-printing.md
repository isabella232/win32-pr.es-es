---
description: La API de impresión GDI proporciona a las aplicaciones una interfaz de impresión independiente del dispositivo.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: API de impresión de GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc2a872b3a310ea44ddfc84103ddbd11cff61998d4884dca5f490e88c3d73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949205"
---
# <a name="gdi-print-api"></a>API de impresión de GDI

La API de impresión GDI proporciona a las aplicaciones una interfaz de impresión independiente del dispositivo. Use esta interfaz si la aplicación usa GDI para representar texto y gráficos.

Si escribe aplicaciones para Windows Vista o versiones posteriores de Windows, considere la posibilidad de usar la API de documentos [XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) y la API de impresión [XPS](xps-printing.md) para usar las interfaces gráficas de mayor rendimiento compatibles con los controladores de impresión XPSDrv.

En esta sección se proporciona información sobre los temas siguientes.



| Tema                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de la API de impresión de GDI](about-the-gdi-print-api.md)<br/>                                 | Información general sobre la funcionalidad de impresión GDI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Uso de la API de impresión GDI](using-the-printing-functions.md)<br/>                            | Información sobre el uso de la API de impresión de GDI en una aplicación.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Referencia de la API de impresión de GDI](gdi-print-api-reference.md)<br/>                                 | Descripciones detalladas de las funciones, estructuras y otros elementos de la API de impresión de GDI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md)<br/> | Microsoft [XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) es un componente que permite a las aplicaciones usar la API de impresión GDI con impresoras que tienen un controlador de impresión XPSDrv.<br/>                                                                                                                                                                                                                                                                                               |
| [Escritor de documentos XPS de Microsoft (MXDW)](microsoft-xps-document-writer.md)<br/>              | El [Escritor de documentos XPS de Microsoft (MXDW)](microsoft-xps-document-writer.md) proporciona a las aplicaciones la funcionalidad "guardar como XPS" o "exportar a XPS". Las aplicaciones que no crean contenido de documento XPS de forma nativa pueden usar MXDW para crear archivos de documento XPS sin usar [la API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)). Sin embargo, la API de documentos XPS proporciona a una aplicación la capacidad de usar las interfaces gráficas de mayor rendimiento compatibles con los controladores de impresión XPSDrv.<br/> |



 

En el diagrama siguiente se muestra la relación de la API de impresión de GDI con las otras API de impresión que puede usar una aplicación.

![diagrama que muestra la relación de la API de impresión gdi con las otras API de impresión que puede usar una aplicación win32](images/print-apis-gdi.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[XPS Print API](xps-printing.md)
</dt> <dt>

[Print Spooler API](print-spooler-api.md)
</dt> <dt>

[API de impresión de vales](print-ticket-api.md)
</dt> </dl>

 

