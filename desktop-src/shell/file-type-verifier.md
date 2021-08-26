---
description: File Type Verifier es una herramienta que permite a los proveedores de software independientes (ISV) comprobar que sus tipos de archivo únicos se implementan correctamente.
ms.assetid: 1BD7452B-2DF5-44e9-9B09-C29ABFFA5F93
title: Comprobador de tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad3d3e66d85413a209c6899ce16061fa1fd46468fa32462026485d49b7326dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009515"
---
# <a name="file-type-verifier"></a>Comprobador de tipo de archivo

File Type Verifier es una herramienta que permite a los proveedores de software independientes (ISV) comprobar que sus tipos de archivo únicos se implementan correctamente. Las implementaciones de alta calidad de los controladores de tipos de archivo son fundamentales para una buena experiencia del usuario, ya que los usuarios interactúan con el formato de archivo de muchas maneras en Windows Explorer. Los usuarios pueden realizar búsquedas de texto completo, ordenar por metadatos personalizados o ver vistas previas y miniaturas enriquecciones del formato de archivo.

Para obtener instrucciones sobre el uso del comprobador de tipos de archivo, [vea How to Use the File Type Verifier](how-to-use-the-file-type-verifier.md).

## <a name="about-the-file-type-verifier-tool"></a>Acerca de la herramienta Comprobador de tipos de archivo

File Type Verifier es un programa que está disponible como parte del [SDK Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Está diseñado para ayudar a los desarrolladores que crean tipos de Windows [personalizados a](fa-file-types.md) detectar posibles problemas con sus tipos de archivo. Aunque el comprobador de tipos de archivo solo se ejecuta en Windows 7 y versiones posteriores, las reglas que aplica el comprobador de tipos de archivo se aplican a todas las versiones de Windows en las que las características que comprueba están disponibles.

El comprobador de tipos de archivo ejecuta varias pruebas en el tipo de archivo para comprobar que está registrado correctamente y que proporciona los controladores de tipo de archivo [adecuados](fa-file-extensions.md) para mostrar el tipo de archivo correctamente en el Explorador de Windows y, si procede, que admite la indexación del contenido del archivo.

El comprobador de tipos de archivo prueba lo siguiente:

-   [Controladores de vista previa](building-preview-handlers.md)
-   [Controladores de miniaturas](building-thumbnail-providers.md)
-   [Controladores de propiedades](../search/-search-3x-wds-extidx-propertyhandlers.md)
-   [Controladores de verbos](fa-verbs.md)
-   [Filtros (IFilter)](../search/-search-3x-wds-extidx-filters.md)
-   [Asociaciones de tipo](../properties/building-property-handlers-user-friendly-kind-names.md)
-   [Tipos percibidos](fa-perceivedtypes.md)
-   [Propiedades importantes](../search/-shell-systemdefinedpropertiesforfileformats.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo usar el comprobador de tipos de archivo](how-to-use-the-file-type-verifier.md)
</dt> <dt>

[Registro de aplicaciones](app-registration.md)
</dt> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> <dt>

[Cómo funcionan las asociaciones de archivos](fa-how-work.md)
</dt> <dt>

[Vista de contenido por tipo de archivo o tipo](prophand-content-view.md)
</dt> <dt>

[Controladores de tipos de archivo](fa-file-extensions.md)
</dt> <dt>

[Identificadores mediante programación](fa-progids.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrices de asociación](fa-associationarray.md)
</dt> </dl>

 

 
