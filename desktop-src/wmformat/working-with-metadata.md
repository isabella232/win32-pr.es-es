---
title: Trabajar con metadatos
description: Trabajar con metadatos
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- SDK de Windows Media Format, información general sobre metadatos
- Advanced Systems Format (ASF), información general sobre metadatos
- ASF (formato de sistemas avanzados), información general sobre metadatos
- metadatos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050336d18947059373ddccf3f18e5d4295834293
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104420459"
---
# <a name="working-with-metadata"></a>Trabajar con metadatos

El objeto de escritor proporciona compatibilidad con metadatos, el lector y los objetos de lector sincrónicos, y el objeto de editor de metadatos. Para obtener información general sobre los metadatos, vea [metadatos](metadata.md). Para obtener información sobre las características que admiten metadatos en el SDK de Windows Media Format, vea [características de metadatos](metadata-features.md).

La interfaz para la edición de metadatos es [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), que puede obtener llamando al método **QueryInterface** de cualquier interfaz en uno de los objetos enumerados anteriormente. **IWMHeaderInfo3** hereda los métodos de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) y [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2). Los métodos de **IWMHeaderInfo3** que se ocupan de los atributos de metadatos representan un enfoque diferente para tener acceso a los metadatos de los que usan los métodos de **IWMHeaderInfo**. Siempre debe usar los métodos más recientes.

Los metadatos de un archivo ASF se identifican mediante un índice y un número de secuencia. A los atributos de nivel de archivo se les asigna un número de secuencia de 0. En versiones anteriores del SDK de Windows Media Format, los atributos se pueden identificar por su nombre. Sin embargo, dado que ahora puede duplicar los nombres de atributo dentro de una secuencia, esto ya no es posible. En su lugar, puede recuperar todos los índices que coinciden con un nombre. Para obtener más información, vea [recuperar atributos de metadatos](retrieving-metadata-attributes.md).

Para ayudar a encontrar los atributos rápidamente, puede usar un número de secuencia especial, 0xFFFF. Use este número de secuencia para identificar el archivo como un todo, en lugar de una secuencia específica o los atributos de nivel de archivo. Los objetos del SDK de Windows Media Format mantienen índices independientes para cada flujo y para los atributos de nivel de archivo. Cuando se usa el flujo 0xFFFF, los índices son diferentes de los que se usan al especificar una secuencia específica. Por ejemplo, el atributo que es el índice 0 de la secuencia 0 no será el mismo que el atributo que es el índice 0 para el flujo 0xFFFF.

En las secciones siguientes se describe el uso de metadatos con mayor detalle.



| Sección                                                                    | Descripción                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Recuperación de atributos de metadatos](retrieving-metadata-attributes.md)       | Describe cómo leer los atributos de metadatos de un encabezado de archivo.                     |
| [Establecer atributos de metadatos](setting-metadata-attributes.md)             | Describe cómo agregar nuevos atributos de metadatos a un encabezado de archivo.                    |
| [Editar atributos de metadatos](editing-metadata-attributes.md)             | Describe cómo editar los atributos de metadatos existentes.                               |
| [Quitar atributos de metadatos](removing-metadata-attributes.md)           | Describe cómo quitar atributos de metadatos existentes.                             |
| [Usar atributos de metadatos complejos](using-complex-metadata-attributes.md) | Describe cómo trabajar con atributos cuyos valores se representan mediante estructuras. |



 

Algunas de las aplicaciones de ejemplo muestran cómo recuperar y editar metadatos. En concreto, vea el ejemplo MetadataEdit, que se incluye en las versiones de C++ y C#.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> <dt>

[**Aplicaciones de ejemplo**](sample-applications.md)
</dt> </dl>

 

 




