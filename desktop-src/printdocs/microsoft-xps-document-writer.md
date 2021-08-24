---
description: Escritor de documentos XPS de Microsoft (MXDW) es un controlador de impresión a archivo que permite a una aplicación de Windows crear archivos de documento de XML Paper Specification (XPS) en versiones de Windows a partir de Windows XP con Service Pack 2 (SP2).
ms.assetid: cb431700-f10f-4c53-9944-d6769895595d
title: Escritor de documentos XPS de Microsoft (MXDW)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dba69a6efff4f2da0ab0cc03bdc71468dada14c457de7685053096d2fba672d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938895"
---
# <a name="microsoft-xps-document-writer-mxdw"></a>Escritor de documentos XPS de Microsoft (MXDW)

Escritor de documentos XPS de Microsoft (MXDW) es un controlador de impresión a archivo que permite a una aplicación de Windows crear archivos de documento de XML Paper Specification (XPS) en versiones de Windows a partir de Windows XP con Service Pack 2 (SP2). El uso de MXDW permite que una aplicación Windows guarde su contenido como un documento XPS sin cambiar el código del programa de la aplicación.

## <a name="when-to-use"></a>Cuándo usar

Como usuario, seleccionaría el MXDW cuando quiera crear un documento XPS desde una aplicación de Windows que no tenga la opción de guardar su contenido como un documento XPS.

Como desarrollador de aplicaciones, se recomienda el MXDW a los usuarios que quieran crear documentos XPS cuando la aplicación no ofrezca la opción de guardar como un documento XPS. Para obtener más información sobre los documentos XML Paper Specification [](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) y XPS, vea XML Paper Specification y [XPS Specification and License Downloads](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).

MXDW se instala automáticamente en Windows Vista y versiones posteriores de Windows y se puede descargar e instalar en Windows XP con SP2 y Windows Server 2003.

## <a name="installation"></a>Instalación

En Windows Vista y versiones posteriores de Windows, el MXDW se instala automáticamente cuando se instala el sistema operativo.

Windows XP con SP2 y **Windows Server 2003:** descargue e instale .Net Framework 3.0 o XPS Essential Pack desde el Centro de descarga de [Microsoft](https://www.microsoft.com/downloads/en/default.aspx).

## <a name="how-to-use"></a>Cómo se usa

Cuando se instala, MXDW aparece como una cola de impresión disponible en el cuadro de diálogo Imprimir presentado por una aplicación. Cuando se selecciona MXDW como impresora, se solicita al usuario el nombre de archivo que se va a crear como el documento XPS que captura la salida de impresión de la aplicación.

En la imagen siguiente se muestra el MXDW seleccionado como impresora en el cuadro de diálogo Windows de impresión común de Vista.

![una imagen del cuadro de diálogo de impresión que muestra la selección del escritor de documentos microsoft xps (mxdw)](images/choosingmxdwinvista.gif)

Los desarrolladores de aplicaciones pueden personalizar la salida de MXDW mediante las [opciones de configuración de MXDW](mxdw-configuration-settings.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Especificación XPS y descargas de licencias](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[IsXPS Conformance Tool](/previous-versions/dotnet/netframework-3.0/aa348104(v=vs.85))
</dt> <dt>

[Opciones de configuración de MXDW](mxdw-configuration-settings.md)
</dt> </dl>

 

 
