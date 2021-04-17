---
description: El escritor de documentos XPS de Microsoft (MXDW) es un controlador de impresión en un archivo que permite a una aplicación Windows crear archivos de documento de XML Paper Specification (XPS) en versiones de Windows a partir de Windows XP con Service Pack 2 (SP2).
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Escritor de documentos XPS de Microsoft (MXDW)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c355460112167577c2b6867774c402182084d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697691"
---
# <a name="microsoft-xps-document-writer-mxdw"></a>Escritor de documentos XPS de Microsoft (MXDW)

El escritor de documentos XPS de Microsoft (MXDW) es un controlador de impresión en un archivo que permite a una aplicación Windows crear archivos de documento de XML Paper Specification (XPS) en versiones de Windows a partir de Windows XP con Service Pack 2 (SP2). El uso de MXDW permite a una aplicación Windows guardar su contenido como un documento XPS sin cambiar el código de programa de la aplicación.

## <a name="when-to-use"></a>Cuándo usar

Como usuario, debería seleccionar MXDW cuando desee crear un documento XPS desde una aplicación de Windows que no tenga la opción de guardar su contenido como un documento XPS.

Como desarrollador de aplicaciones, recomendaría MXDW a los usuarios que quieren crear documentos XPS cuando la aplicación no ofrece la opción de guardar como un documento XPS. Para obtener más información sobre la especificación de papel XML y los documentos XPS, consulte [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) y [XPS Specification and License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).

MXDW se instala automáticamente en Windows Vista y versiones posteriores de Windows y se puede descargar e instalar en Windows XP con SP2 y Windows Server 2003.

## <a name="installation"></a>Instalación

En Windows Vista y versiones posteriores de Windows, el MXDW se instala automáticamente cuando se instala el sistema operativo.

**Windows XP con SP2 y Windows Server 2003**: Descargue e instale .net Framework 3,0 o XPS Essential Pack desde el centro de [descarga de Microsoft](https://www.microsoft.com/downloads/en/default.aspx).

## <a name="how-to-use"></a>Cómo se usa

Una vez instalado, MXDW aparece como una cola de impresión disponible en el cuadro de diálogo Imprimir presentado por una aplicación. Cuando se selecciona MXDW como impresora, se solicita al usuario el nombre de archivo que se va a crear como documento XPS que captura la salida de impresión de la aplicación.

La siguiente imagen muestra el MXDW que se selecciona como impresora en el cuadro de diálogo de impresión común de Windows Vista.

![imagen del cuadro de diálogo Imprimir que muestra la selección del escritor de documentos XPS de Microsoft (mxdw)](images/choosingmxdwinvista.gif)

Los desarrolladores de aplicaciones pueden personalizar el resultado de MXDW con los [valores de configuración de MXDW](mxdw-configuration-settings.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Especificaciones de XPS y descargas de licencias](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Herramienta de cumplimiento de isXPS](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))
</dt> <dt>

[Opciones de configuración de MXDW](mxdw-configuration-settings.md)
</dt> </dl>

 

 
