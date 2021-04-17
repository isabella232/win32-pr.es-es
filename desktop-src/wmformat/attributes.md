---
title: Atributos (Windows Media Format 11 SDK)
description: Atributos
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- SDK de Windows Media Format, atributos
- Advanced Systems Format (ASF), atributos
- ASF (formato de sistemas avanzados), atributos
- atributos, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c209558ed4803fee96e9b482302af1864cbf988b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421827"
---
# <a name="attributes-windows-media-format-11-sdk"></a>Atributos (Windows Media Format 11 SDK)

Un atributo es un elemento individual de metadatos. La mayoría de los atributos se pueden establecer en la aplicación y se escriben en el encabezado de un archivo ASF.

Algunos de los atributos predefinidos son atributos codificados. Estos atributos no se almacenan en el encabezado de un archivo ASF, pero se calculan mediante los objetos del SDK de Windows Media Format cuando se carga el archivo. Dado que los atributos codificados siempre se calculan, son intrínsecamente de solo lectura.

Este SDK incluye muchas definiciones de atributos que puede usar. También puede crear atributos propios para describir el contenido.

En las secciones siguientes se describen los atributos predefinidos.



| Sección                                                                | Descripción                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Lista de atributos](attribute-list.md)                                   | Proporciona una lista alfabética de todos los atributos predefinidos. Después de la lista, cada atributo se describe individualmente.                                                                          |
| [Atributos con varios valores](attributes-with-multiple-values.md) | Muestra los atributos que se pueden agregar más de una vez a un archivo.                                                                                                                                      |
| [Atributos por tipo](attributes-by-type.md)                           | Contiene listas de atributos ordenados por tipo. Estos incluyen listas de atributos especiales (como los que se ocupan de la administración de derechos digitales) y listas de atributos sugeridos por tipo de contenido. |
| [Compatibilidad con etiquetas ID3](id3-tag-support.md)                                 | Muestra los atributos que son compatibles con las etiquetas ID3.                                                                                                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMHeaderInfo::GetAttributeByIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[**IWMHeaderInfo:: SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**Trabajar con metadatos**](working-with-metadata.md)
</dt> </dl>

 

 




