---
description: El comprobador de tipo de archivo es una herramienta que permite a los fabricantes de software independientes (ISV) comprobar que los tipos de archivo únicos se implementan correctamente.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Comprobador de tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8e4a588e4889241762a9d8e0567d4a4542c0255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909566"
---
# <a name="file-type-verifier"></a>Comprobador de tipo de archivo

El comprobador de tipo de archivo es una herramienta que permite a los fabricantes de software independientes (ISV) comprobar que los tipos de archivo únicos se implementan correctamente. Las implementaciones de alta calidad de los controladores de tipo de archivo son cruciales para una buena experiencia del usuario, ya que los usuarios interactúan con el formato de archivo de muchas maneras en el explorador de Windows. Los usuarios pueden realizar búsquedas de texto completo, ordenar por metadatos personalizados o ver miniaturas enriquecidas y vistas previas del formato de archivo.

Para obtener instrucciones sobre el uso del comprobador de tipo de archivo, consulte [Cómo usar el comprobador de tipo de archivo](how-to-use-the-file-type-verifier.md).

## <a name="about-the-file-type-verifier-tool"></a>Acerca de la herramienta Comprobador de tipo de archivo

Comprobador de tipo de archivo es un programa que está disponible como parte del [SDK de Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Está diseñado para ayudar a los desarrolladores que crean [tipos de archivo](fa-file-types.md) de Windows personalizados para detectar posibles problemas con sus tipos de archivo. Aunque el comprobador de tipo de archivo solo se ejecuta en Windows 7 y versiones posteriores, las reglas que el comprobador de tipo de archivo aplica a todas las versiones de Windows en las que están disponibles las características que comprueba.

El comprobador de tipo de archivo ejecuta varias pruebas en el tipo de archivo para comprobar que se ha registrado correctamente, y que proporciona los [controladores de tipo de archivo](fa-file-extensions.md) adecuados para mostrar el tipo de archivo correctamente en el explorador de Windows y, cuando sea necesario, que admita la indización del contenido del archivo.

El comprobador de tipo de archivo prueba lo siguiente:

-   [Controladores de vista previa](building-preview-handlers.md)
-   [Controladores en miniatura](building-thumbnail-providers.md)
-   [Controladores de propiedades](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [Controladores de verbos](fa-verbs.md)
-   [Filtros (IFilter)](../search/-search-3x-wds-extidx-filters.md)
-   [Asociaciones de tipo](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [Tipos percibidos](fa-perceivedtypes.md)
-   [Propiedades importantes](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo usar el comprobador de tipo de archivo](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[Registro de aplicaciones](app-registration.md)
</dt> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> <dt>

[Cómo funcionan las asociaciones de archivos](fa-how-work.md)
</dt> <dt>

[Vista de contenido por tipo de archivo o tipo](prophand-content-view.md)
</dt> <dt>

[Controladores de tipo de archivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores de programación](fa-progids.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrices de asociación](fa-associationarray.md)
</dt> </dl>

 

 
