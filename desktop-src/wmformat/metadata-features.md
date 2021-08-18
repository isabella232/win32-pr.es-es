---
title: Características de metadatos
description: Los metadatos se usan en archivos ASF para describir el contenido y las propiedades del archivo.
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- Windows SDK de formato multimedia, características de metadatos
- Windows SDK de formato multimedia, características
- Formato de sistemas avanzados (ASF), características de metadatos
- ASF (formato de sistemas avanzados), características de metadatos
- Formato de sistemas avanzados (ASF), características
- ASF (formato de sistemas avanzados), características
- metadata,features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6865e54f2eeabcb96dd88df27aba578a9169ed84857d17af5602848041f24118
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700457"
---
# <a name="metadata-features"></a>Características de metadatos

Los metadatos se usan en archivos ASF para describir el contenido y las propiedades del archivo. Todos los archivos ASF que cree deben incluir los metadatos adecuados. (Para obtener información general, vea [Metadatos).](metadata.md) El SDK Windows Media Format incluye compatibilidad con la edición de metadatos a través del objeto de escritor, el objeto del editor de metadatos y los objetos lector y lector sincrónico. Se incluye compatibilidad nativa con una amplia variedad de atributos de metadatos. Consulte [Atributos](attributes.md) para obtener una lista de los atributos predefinidos.

La compatibilidad con metadatos proporcionada por los distintos objetos del SDK Windows Media Format es flexible y eficaz. Las características de metadatos principales se resumen en la lista siguiente:

-   Tamaño de atributo flexible. Los atributos de metadatos no tienen un tamaño limitado.
-   Atributos de nivel de flujo. Los metadatos de los archivos ASF se pueden asignar al archivo como un todo o a una secuencia determinada.
-   Atributos duplicados. Un atributo con nombre se puede usar varias veces en el mismo archivo. Esta característica es de uso particular al asignar atributos descriptivos de contenido. Por ejemplo, una canción puede tener varios autores, cada uno de los cual requiere un atributo **Author** independiente en el archivo.
-   Varios idiomas. Cada atributo tiene un idioma asociado. Puede establecer los idiomas admitidos y, a continuación, asignar uno a cada atributo que escriba. Dado que puede duplicar atributos, puede proporcionar los atributos más importantes en varios idiomas para llegar a un público mayor. Si no especifica un idioma, se usará el idioma predeterminado (obtenido del sistema operativo del equipo que ejecuta la aplicación).
-   Atributos complejos. Algunos de los atributos predefinidos admiten datos estructurados. Para estos atributos, el tipo de datos es binario, pero el valor es una estructura definida en este SDK.

En los temas siguientes se tratan las otras características de metadatos admitidas.



| Tema                                  | Descripción                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [Compatibilidad con ID3](id3.md)                 | Describe la compatibilidad con fotogramas ID3 mediante los objetos del SDK Windows Media Format. |
| [Metadatos personalizados](custom-metadata.md) | Describe las implicaciones de usar metadatos personalizados.                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características**](features.md)
</dt> <dt>

[**IWMHeaderInfo (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[**IWMHeaderInfo2 (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[**IWMHeaderInfo3 (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[**Metadatos**](metadata.md)
</dt> </dl>

 

 




