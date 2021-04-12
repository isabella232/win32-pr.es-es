---
title: Características de metadatos
description: Los metadatos se usan en archivos ASF para describir el contenido y las propiedades del archivo.
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- SDK de Windows Media Format, características de metadatos
- Windows Media Format SDK, características
- Advanced Systems Format (ASF), características de metadatos
- ASF (formato de sistemas avanzados), características de metadatos
- Advanced Systems Format (ASF), características
- ASF (formato de sistemas avanzados), características
- metadatos, características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ea31885a1c1635ee4778683858876572e32262
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104420451"
---
# <a name="metadata-features"></a>Características de metadatos

Los metadatos se usan en archivos ASF para describir el contenido y las propiedades del archivo. Todos los archivos ASF que cree deben incluir los metadatos adecuados. (Para obtener información general, consulte [metadatos](metadata.md)). El SDK de Windows Media Format incluye compatibilidad con la edición de metadatos mediante el objeto de escritor, el objeto de editor de metadatos y los objetos de lector y lector sincrónicos. Se incluye compatibilidad nativa para una amplia variedad de atributos de metadatos. Vea [atributos](attributes.md) para obtener una lista de los atributos predefinidos.

La compatibilidad de metadatos proporcionada por los distintos objetos del SDK de Windows Media Format es flexible y eficaz. Las principales características de los metadatos se resumen en la siguiente lista:

-   Tamaño de atributo flexible. Los atributos de metadatos no tienen un tamaño limitado.
-   Atributos de nivel de secuencia. Los metadatos de los archivos ASF se pueden asignar al archivo en su totalidad o a una secuencia determinada.
-   Atributos duplicados. Un atributo con nombre se puede usar varias veces en el mismo archivo. Esta característica es de uso particular cuando se asignan atributos descriptivos de contenido. Por ejemplo, una canción puede tener varios autores, cada uno de los cuales requiere un atributo **Author** independiente en el archivo.
-   Varios idiomas. Cada atributo tiene un idioma asociado. Puede establecer los idiomas admitidos y, a continuación, asignar uno a cada atributo que escriba. Dado que puede duplicar atributos, puede proporcionar los atributos más importantes en varios idiomas para llegar a un público más grande. Si no especifica un idioma, se usará el idioma predeterminado (obtenido del sistema operativo del equipo que ejecuta la aplicación).
-   Atributos complejos. Algunos de los atributos predefinidos admiten datos estructurados. Para estos atributos, el tipo de datos es binario, pero el valor es una estructura definida en este SDK.

En los temas siguientes se describen las demás características de metadatos admitidas.



| Tema                                  | Descripción                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [Compatibilidad con ID3](id3.md)                 | Describe la compatibilidad con tramas ID3 mediante los objetos del SDK de Windows Media Format. |
| [Metadatos personalizados](custom-metadata.md) | Describe las implicaciones del uso de metadatos personalizados.                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características**](features.md)
</dt> <dt>

[**Interfaz IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**Interfaz IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[**Interfaz IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[**Metadatos**](metadata.md)
</dt> </dl>

 

 




