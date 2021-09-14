---
title: Trabajar con metadatos
description: Trabajar con metadatos
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- Windows SDK de formato multimedia, información general sobre metadatos
- Formato de sistemas avanzados (ASF), información general sobre metadatos
- ASF (formato de sistemas avanzados), información general sobre metadatos
- metadata,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050336d18947059373ddccf3f18e5d4295834293
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247173"
---
# <a name="working-with-metadata"></a>Trabajar con metadatos

El objeto de escritor, los objetos lector y lector sincrónico y el objeto del editor de metadatos proporcionan compatibilidad con metadatos. Para obtener información general sobre los metadatos, vea [Metadatos.](metadata.md) Para obtener información sobre las características que admiten metadatos en Windows SDK de formato multimedia, vea [Características de metadatos](metadata-features.md).

La interfaz para la edición de metadatos es [**IWMHeaderInfo3,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)que puede obtener llamando al método **QueryInterface** de cualquier interfaz de uno de los objetos enumerados anteriormente. **IWMHeaderInfo3** hereda los métodos de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) e [**IWMHeaderInfo2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) Los métodos de **IWMHeaderInfo3** que tratan los atributos de metadatos representan un enfoque diferente para acceder a los metadatos que el que usan los métodos de **IWMHeaderInfo**. Siempre debe usar los métodos más recientes.

Los metadatos de un archivo ASF se identifican mediante un índice y un número de secuencia. A los atributos de nivel de archivo se les asigna un número de secuencia de 0. En versiones anteriores del SDK Windows Media Format, los atributos se podían identificar por nombre. Sin embargo, dado que ahora puede duplicar nombres de atributo dentro de una secuencia, esto ya no es posible. En su lugar, puede recuperar todos los índices que coinciden con un nombre. Para obtener más información, vea [Recuperar atributos de metadatos.](retrieving-metadata-attributes.md)

Para ayudar a buscar atributos rápidamente, puede usar un número de secuencia especial, 0xFFFF. Use este número de secuencia para identificar el archivo como un todo, en lugar de una secuencia específica o los atributos de nivel de archivo. Los objetos del SDK Windows Media Format mantienen índices independientes para cada secuencia y para los atributos de nivel de archivo. Cuando se usan 0xFFFF flujo, los índices son diferentes de los que se usan al especificar una secuencia específica. Por ejemplo, el atributo que es el índice 0 para el flujo 0 no será el mismo que el atributo que es el índice 0 para el flujo 0xFFFF.

En las secciones siguientes se describe el uso de metadatos con más detalle.



| Sección                                                                    | Descripción                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Recuperar atributos de metadatos](retrieving-metadata-attributes.md)       | Describe cómo leer atributos de metadatos de un encabezado de archivo.                     |
| [Establecer atributos de metadatos](setting-metadata-attributes.md)             | Describe cómo agregar nuevos atributos de metadatos a un encabezado de archivo.                    |
| [Editar atributos de metadatos](editing-metadata-attributes.md)             | Describe cómo editar atributos de metadatos existentes.                               |
| [Quitar atributos de metadatos](removing-metadata-attributes.md)           | Describe cómo quitar atributos de metadatos existentes.                             |
| [Uso de atributos de metadatos complejos](using-complex-metadata-attributes.md) | Describe cómo trabajar con atributos cuyos valores se representan mediante estructuras. |



 

Varias de las aplicaciones de ejemplo muestran cómo recuperar y editar metadatos. En concreto, consulte el ejemplo MetadataEdit, que se incluye en las versiones de C++ y C#.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> <dt>

[**Guía de programación**](programming-guide.md)
</dt> <dt>

[**Aplicaciones de ejemplo**](sample-applications.md)
</dt> </dl>

 

 




