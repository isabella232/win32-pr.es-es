---
description: La API de impresión de GDI proporciona a las aplicaciones una interfaz de impresión independiente del dispositivo.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: API de impresión GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0239282543a68c6fe8b5d6503d085582fd9c20db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276780"
---
# <a name="gdi-print-api"></a>API de impresión GDI

La API de impresión de GDI proporciona a las aplicaciones una interfaz de impresión independiente del dispositivo. Use esta interfaz si la aplicación usa GDI para representar texto y gráficos.

Si escribe aplicaciones para Windows Vista o versiones posteriores de Windows, considere la posibilidad de usar la [API de documentos XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) y la [API de impresión XPS](xps-printing.md) para usar las interfaces de gráficos de mayor rendimiento admitidas por los controladores de impresión XPSDrv.

En esta sección se proporciona información sobre los temas siguientes.



| Tema                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca de la API de impresión GDI](about-the-gdi-print-api.md)<br/>                                 | Información general sobre la funcionalidad de impresión de GDI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Uso de la API de impresión de GDI](using-the-printing-functions.md)<br/>                            | Información sobre el uso de la API de impresión de GDI en una aplicación.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Referencia de la API de impresión de GDI](gdi-print-api-reference.md)<br/>                                 | Descripciones detalladas de las funciones, estructuras y otros elementos de la API de impresión de GDI.<br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [Convertidor de documentos XPS de Microsoft (MXDC)](microsoft-xps-document-converter--mxdc-.md)<br/> | El [convertidor de documentos XPS de Microsoft (MXDC)](microsoft-xps-document-converter--mxdc-.md) es un componente que permite a las aplicaciones usar la API de impresión de GDI con impresoras que tienen un controlador de impresión XPSDrv.<br/>                                                                                                                                                                                                                                                                                               |
| [Escritor de documentos XPS de Microsoft (MXDW)](microsoft-xps-document-writer.md)<br/>              | El [escritor de documentos XPS de Microsoft (MXDW)](microsoft-xps-document-writer.md) proporciona a las aplicaciones la funcionalidad "guardar como XPS" o "exportar a XPS". Las aplicaciones que no crean de forma nativa el contenido de un documento XPS pueden usar MXDW para crear archivos de documento XPS sin usar la [API de documentos XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)). La API de documento XPS, sin embargo, proporciona una aplicación con la capacidad de usar las interfaces de gráficos de mayor rendimiento que son compatibles con los controladores de impresión XPSDrv.<br/> |



 

En el diagrama siguiente se muestra la relación de la API de impresión de GDI con las otras API de impresión que puede usar una aplicación.

![diagrama que muestra la relación de la API de impresión de GDI con las otras API de impresión que puede usar una aplicación Win32.](images/print-apis-gdi.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[API de impresión XPS](xps-printing.md)
</dt> <dt>

[API del administrador de trabajos de impresión](print-spooler-api.md)
</dt> <dt>

[Print ticket API](print-ticket-api.md)
</dt> </dl>

 

