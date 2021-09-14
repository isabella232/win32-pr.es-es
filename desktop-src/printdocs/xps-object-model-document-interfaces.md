---
description: Las interfaces de documento proporcionan acceso a los componentes del paquete XPS que determinan la estructura de un documento en un OM XPS.
ms.assetid: 3302d164-81ad-4198-a116-f967e7a14147
title: Interfaces de documento de XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc191c4c0b8ec5571331022321a8ae829587022
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252284"
---
# <a name="xps-om-document-interfaces"></a>Interfaces de documento de XPS OM

Las interfaces de documento proporcionan acceso a los componentes del paquete XPS que determinan la estructura de un documento en un OM XPS. En la tabla siguiente se enumeran las interfaces de documento.



| Nombre de la interfaz                                                      | Interfaces secundarias lógicas                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>           | Representa un conjunto de documentos enlazados en una lista ordenada.<br/> Las interfaces secundarias se recopilan en [**una interfaz IXpsOMDocumentCollection.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/>                                                                                                                                                                                                  |
| [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                 | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | Representa un único elemento FixedDocument y enlaza la colección de referencias de página de las páginas de un documento.<br/> Las interfaces secundarias se recopilan en una [**interfaz IXpsOMPageReferenceCollection.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)<br/> La estructura del documento se expone en una [**interfaz IXpsOMDocumentStructureResource.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> |
| [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>       | [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                   | Una versión ligera virtualizada de una página del documento. Una referencia de página describe las características principales de la página (por ejemplo, sus dimensiones), pero no incluye ningún contenido de la página.<br/>                                                                                                                                                                                             |
| [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/>     | None<br/>                                               | Colección de objetos de la página que son destinos de hipervínculo.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>       | None<br/>                                               | Colección de los recursos de elemento asociados a una página.<br/>                                                                                                                                                                                                                                                                                                                                |



 

## <a name="contents"></a>Contenido

-   [Trabajar con interfaces IXpsOMDocumentSequence](working-with-xpsomdocumentsequence-interfaces.md) contiene información sobre el uso de las interfaces siguientes:
    -   [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
    -   [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
-   [Trabajar con interfaces IXpsOMDocument](working-with-xpsomdocument-interfaces.md) contiene información sobre el uso de las interfaces siguientes:
    -   [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
    -   [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
    -   [**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
-   [Trabajar con interfaces IXpsOMPageReference](working-with-xpsompagereference-interfaces.md) contiene información sobre el uso de las interfaces siguientes:
    -   [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
    -   [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
    -   [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
    -   [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)

 

 




