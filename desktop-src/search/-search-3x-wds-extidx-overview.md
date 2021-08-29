---
description: Puede ampliar Windows search para indexar el contenido y las propiedades de nuevos formatos de archivo y almacenes de datos mediante interfaces de complemento de datos.
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: Extensión del índice (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6faa3ab6ba7631840bcc324bbd163c9e182c611be7e94c6a856e9949ca6857e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597885"
---
# <a name="extending-the-index-windows-search"></a>Extensión del índice (Windows Search)

Puede ampliar Windows Search para indexar el contenido y las propiedades de nuevos formatos de archivo y almacenes de datos mediante [interfaces de complemento de datos](./-search-data-addins-interfaces-entry-page.md). Para crear complementos de Windows Search, los desarrolladores de terceros primero deben implementar un almacén de datos de Shell y, a continuación, desarrollar un controlador de protocolo para que Windows Search pueda acceder a los datos para la indexación. Si tiene un formato de archivo personalizado, debe desarrollar un controlador de filtro para indexar el contenido del archivo y un controlador de propiedades para cada tipo de archivo para indexar las propiedades.

Windows Search admite actualmente la indexación de más de 200 tipos de elementos (como formatos de archivo .txt, .html y .xml) y puede trabajar con varios tipos de almacenes de datos (como el sistema de archivos NTFS y Microsoft Outlook). Windows La búsqueda usa tecnología de filtro y controlador de protocolo similar a SharePoint Server. Por lo tanto, si ya tiene implementaciones para el formato de archivo, puede actualizar las implementaciones que se inicializarán con una secuencia mediante [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) para que el filtro funcione con Windows Search.

> [!Note]  
> Los controladores de filtro, los controladores de propiedades y los controladores de protocolo deben escribirse en código nativo. Esto se debe a posibles problemas de control de versiones de Common Language Runtime (CLR) con el proceso en el que se ejecutan varios complementos.

 

Esta sección sobre cómo ampliar el índice con complementos contiene los temas siguientes:

-   [Desarrollar controladores de filtro](-search-ifilter-conceptual.md)
-   [Desarrollar controladores de propiedades para Windows búsqueda](-search-3x-wds-extidx-propertyhandlers.md)
-   [Desarrollar controladores de protocolo](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a>Recursos adicionales

Para obtener ejemplos de código relacionados, [vea Windows Ejemplos de código de búsqueda.](-search-samples-ovw.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Guía de desarrollo de búsqueda](-search-developers-guide-entry-page.md)
</dt> <dt>

[Administración del índice](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Consulta del índice mediante programación](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Extensión de recursos de lenguaje](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
