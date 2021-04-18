---
description: En este tema se describe cómo usar las interfaces de nivel de página que proporcionan acceso al contenido de una página en un OM XPS.
ms.assetid: 7127ee28-eca9-4e0e-a27a-9051eb105b27
title: Trabajar con interfaces de página de XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8350409f2f436cc4ec2293e735c3f020b49bea68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697330"
---
# <a name="working-with-xps-om-page-interfaces"></a>Trabajar con interfaces de página de XPS OM

En este tema se describe cómo usar las interfaces de nivel de página que proporcionan acceso al contenido de una página en un OM XPS.



| Nombre de interfaz                                                                                                                                                                              | Interfaces secundarias lógicas                                                                                                                                                                                            | Descripción                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                                                                                                                                                 | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                                                                         | Objeto raíz del contenido de la página.<br/> Este objeto representa un elemento de documento.<br/>                                                |
| [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable)<br/>                                                                                                                                       | [**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/> [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/> [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/> | Las interfaces que se derivan de la interfaz [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) se pueden almacenar en un diccionario de recursos y compartirse.<br/> |
| [**IXpsOMRemoteDictionaryResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)<br/> [**IXpsOMRemoteDictionaryResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)<br/> | [**IXpsOMDictionary**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                                             | Contiene un diccionario de recursos.<br/>                                                                                                         |
| [**IXpsOMDictionary**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                     | None<br/>                                                                                                                                                                                                     | Hace referencia a los recursos que comparten otros objetos.<br/>                                                                              |
| [**IXpsOMStoryFragmentsResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)<br/>                                                                                                             | None<br/>                                                                                                                                                                                                     | Proporciona acceso al contenido de la secuencia de recursos de la parte StoryFragments del documento.<br/>                                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IXpsOMDictionary**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)
</dt> <dt>

[**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
</dt> <dt>

[**Interfaz IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**Interfaz IXpsOMRemoteDictionaryResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)
</dt> <dt>

[**Interfaz IXpsOMRemoteDictionaryResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)
</dt> <dt>

[**Interfaz IXpsOMStoryFragmentsResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)
</dt> </dl>

 

 




