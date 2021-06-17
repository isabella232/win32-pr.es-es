---
title: Atributos (Windows Media Format SDK 11)
description: Obtenga información sobre los atributos del SDK Windows Media Format 11. Un atributo es un elemento individual de metadatos.
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- Windows Media Format SDK,attributes
- Formato de sistemas avanzados (ASF), atributos
- ASF (formato de sistemas avanzados), atributos
- attributes,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23738e20df2c6360b20b7c3da005cde6b3942d44
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262197"
---
# <a name="attributes-windows-media-format-11-sdk"></a>Atributos (Windows Media Format SDK 11)

Un atributo es un elemento individual de metadatos. La aplicación puede establecer la mayoría de los atributos y se escriben en el encabezado de un archivo ASF.

Algunos de los atributos predefinidos son atributos codificados. Estos atributos no se almacenan en el encabezado de un archivo ASF, sino que los calculan los objetos del SDK de Windows Media Format cuando se carga el archivo. Dado que los atributos codificados siempre se calculan, son inherentemente de solo lectura.

Este SDK incluye muchas definiciones de atributos que puede usar. También puede crear atributos propios para describir el contenido.

En las secciones siguientes se describen los atributos predefinidos.



| Sección                                                                | Descripción                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Lista de atributos](attribute-list.md)                                   | Proporciona una lista alfabética de todos los atributos predefinidos. Después de la lista, cada atributo se describe individualmente.                                                                          |
| [Atributos con varios valores](attributes-with-multiple-values.md) | Enumera los atributos que se pueden agregar a un archivo más de una vez.                                                                                                                                      |
| [Atributos por tipo](attributes-by-type.md)                           | Contiene listas de atributos ordenados por tipo. Estas incluyen listas de atributos de propósito especial (como los que tratan con la administración de derechos digitales) y listas de atributos sugeridos por tipo de contenido. |
| [Compatibilidad con etiquetas ID3](id3-tag-support.md)                                 | Enumera los atributos que son compatibles con las etiquetas ID3.                                                                                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMHeaderInfo::GetAttributeByIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




