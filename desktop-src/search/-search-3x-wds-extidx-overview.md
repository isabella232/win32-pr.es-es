---
description: Puede extender Windows Search para indizar el contenido y las propiedades de los nuevos formatos de archivo y los almacenes de datos mediante interfaces de complementos de datos.
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: Extensión del índice (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a74638dd5366732716335af938c00098cc3991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705501"
---
# <a name="extending-the-index-windows-search"></a>Extensión del índice (Windows Search)

Puede extender Windows Search para indizar el contenido y las propiedades de los nuevos formatos de archivo y los almacenes de datos mediante [interfaces de complementos de datos](./-search-data-addins-interfaces-entry-page.md). Para crear complementos de Windows Search, los desarrolladores de terceros deben implementar primero un almacén de datos de Shell y, a continuación, desarrollar un controlador de protocolo para que Windows Search pueda acceder a los datos para la indexación. Si tiene un formato de archivo personalizado, debe desarrollar un controlador de filtro para indizar el contenido del archivo y un controlador de propiedades para cada tipo de archivo para indizar las propiedades.

Windows Search admite actualmente la indexación de más de 200 tipos de elementos (como los formatos de archivo. txt,. html y. xml) y puede trabajar con varios tipos de almacenes de datos (como el sistema de archivos NTFS y Microsoft Outlook). Windows Search usa tecnología de filtros y controladores de protocolo similar a la de SharePoint Server. Por lo tanto, si ya tiene implementaciones para el formato de archivo, puede actualizar las implementaciones que se van a inicializar con una secuencia mediante [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) para que el filtro funcione con Windows Search.

> [!Note]  
> Los controladores de filtro, los controladores de propiedades y los controladores de protocolo deben escribirse en código nativo. Esto se debe a posibles problemas de control de versiones de Common Language Runtime (CLR) con el proceso en el que se ejecutan varios complementos.

 

Esta sección sobre cómo extender el índice con complementos contiene los siguientes temas:

-   [Desarrollar controladores de filtro](-search-ifilter-conceptual.md)
-   [Desarrollar controladores de propiedades para Windows Search](-search-3x-wds-extidx-propertyhandlers.md)
-   [Desarrollar controladores de protocolo](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a>Recursos adicionales

Para ver ejemplos de código relacionados, consulte [ejemplos de código de Windows Search](-search-samples-ovw.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de desarrollo de Windows Search](-search-developers-guide-entry-page.md)
</dt> <dt>

[Administración del índice](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Consulta del índice mediante programación](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Extensión de recursos de idioma](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
