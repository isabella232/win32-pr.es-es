---
description: Esta interfaz IXpsOMPrintTicketResource de la API de documentos XPS proporciona acceso a un vale de impresión existente y también la capacidad de crear un vale de impresión en un OM XPS.
ms.assetid: 53c95da0-1601-4945-83a1-e3266d251aee
title: Interfaces de vales de impresión de OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f629e716db7098f8f6999df758fd3b73e3f82b83308a3dd68d5f247d6cd709a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117867761"
---
# <a name="xps-om-print-ticket-interfaces"></a>Interfaces de vales de impresión de OM XPS

Esta [**interfaz IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) de la API de documentos XPS proporciona acceso a un vale de impresión existente y también la capacidad de crear un vale de impresión en un OM XPS.

## <a name="print-ticket-resources"></a>Imprimir recursos de vale

La [**interfaz IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) permite a un programa leer el contenido de un vale de impresión existente llamando al método **GetPrintTicketResource** de una interfaz que admite un vale de impresión. Se pueden agregar nuevos recursos de vale de impresión a una parte del documento mediante una llamada a **SetPrintTicketResource.**

Hay tres niveles de vale de impresión, que especifican el ámbito del vale de impresión. Los niveles de vale de impresión son: el nivel de trabajo (o paquete), el nivel de documento y el nivel de página. En la tabla siguiente se muestra la relación entre el nivel de vale de impresión, la interfaz XPS OM correspondiente y los métodos usados para acceder al recurso de vale de impresión.

| Nivel de vale de impresión | Interfaz                                                | Get (Método)                                                                      | Método Set                                                                      |
|--------------------|----------------------------------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Trabajo                | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getprintticketresource) | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-setprintticketresource) |
| Documento           | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)                 | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getprintticketresource)         | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-setprintticketresource)         |
| Página               | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)       | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getprintticketresource)    | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-setprintticketresource)    |



 

## <a name="print-ticket-content"></a>Imprimir contenido de vale

Se puede acceder al contenido de un recurso de vale de impresión existente leyendo desde la secuencia asociada al recurso. El [**método GetStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-getstream) de la interfaz [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) devuelve el puntero a una secuencia de solo lectura que contiene el contenido con formato XML del vale de impresión. El formato del contenido del vale de impresión se describe en [especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Se puede crear un nuevo recurso de vale de impresión mediante la creación de una nueva [**interfaz IXpsOMPrintTicketResource.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) Se escribe un vale de impresión válido con formato XML en una secuencia y se crea un URI de parte para identificar el elemento de vale de impresión. Para obtener más información sobre el contenido de un vale de impresión válido, consulte [especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip). La secuencia y el URI de la parte se pasan como parámetros de la llamada [**SetContent**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-setcontent) para establecer el nuevo recurso de vale de impresión y el recurso de vale de impresión se agrega al elemento de documento correspondiente mediante una llamada al método **SetPrintTicketResource** que se muestra en la tabla anterior.

## <a name="print-ticket-inheritance"></a>Herencia de vales de impresión

Los vales de impresión heredan las propiedades de los vales de impresión con mayor ámbito. Por ejemplo, un vale de impresión de nivel de documento hereda las propiedades del vale de impresión de nivel de trabajo asociado a la secuencia de documentos del documento. Del mismo modo, un vale de impresión de nivel de página hereda las propiedades del vale de impresión de nivel de documento asociado al documento de la página. En este proceso de herencia, las propiedades especificadas en el vale de impresión de nivel inferior invalidan las propiedades correspondientes que, de lo contrario, se heredarán del vale de impresión de nivel superior.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



