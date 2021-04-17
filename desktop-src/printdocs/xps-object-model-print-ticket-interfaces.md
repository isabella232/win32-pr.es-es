---
description: Esta interfaz IXpsOMPrintTicketResource de la API de documento XPS proporciona acceso a una solicitud de impresión existente y también a la capacidad de crear una solicitud de impresión en un OM XPS.
ms.assetid: 53c95da0-1601-4945-83a1-e3266d251aee
title: Interfaces de vales de impresión de XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646089455e7106b1be3716c0ccf0774be361f130
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717431"
---
# <a name="xps-om-print-ticket-interfaces"></a>Interfaces de vales de impresión de XPS OM

Esta interfaz [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) de la API de documento XPS proporciona acceso a una solicitud de impresión existente y también a la capacidad de crear una solicitud de impresión en un OM XPS.

## <a name="print-ticket-resources"></a>Imprimir recursos de entradas

La interfaz [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) permite a un programa leer el contenido de una solicitud de impresión existente llamando al método **GetPrintTicketResource** de una interfaz que admite una solicitud de impresión. Se pueden agregar nuevos recursos de la solicitud de impresión a un elemento de documento mediante una llamada a **SetPrintTicketResource**.

Hay tres niveles de vale de impresión, que especifican el ámbito de la solicitud de impresión. Los niveles de vale de impresión son: el nivel de trabajo (o paquete), el nivel de documento y el nivel de página. En la tabla siguiente se muestra la relación entre el nivel de entrada de impresión, la interfaz de OM de XPS correspondiente y los métodos utilizados para tener acceso al recurso de la solicitud de impresión.

| Imprimir nivel de vale | Interfaz                                                | Get (Método)                                                                      | Método Set                                                                      |
|--------------------|----------------------------------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Trabajo                | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getprintticketresource) | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-setprintticketresource) |
| Documento           | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)                 | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getprintticketresource)         | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-setprintticketresource)         |
| Página               | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)       | [**GetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getprintticketresource)    | [**SetPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-setprintticketresource)    |



 

## <a name="print-ticket-content"></a>Imprimir el contenido del vale

Se puede tener acceso al contenido de un recurso de la solicitud de impresión existente mediante la lectura de la secuencia asociada con el recurso. El método [**GetStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-getstream) de la interfaz [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) devuelve el puntero a una secuencia de solo lectura que contiene el contenido con formato XML de la solicitud de impresión. El formato del contenido del vale de impresión se describe en la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Se puede crear un nuevo recurso de solicitud de impresión mediante la creación de una nueva interfaz [**IXpsOMPrintTicketResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomprintticketresource) . Un vale de impresión con formato XML válido se escribe en una secuencia y se crea un URI de parte para identificar la parte de la solicitud de impresión. Para obtener más información sobre el contenido de una solicitud de impresión válida, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip). La secuencia y el URI de la parte se pasan como parámetros de la llamada a [**SetContent**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomprintticketresource-setcontent) para establecer el nuevo recurso de la solicitud de impresión y el recurso de la solicitud de impresión se agrega al elemento de documento correspondiente llamando al método **SetPrintTicketResource** mostrado en la tabla anterior.

## <a name="print-ticket-inheritance"></a>Herencia de entradas de impresión

Los vales de impresión heredan las propiedades de las solicitudes de impresión con un ámbito mayor. Por ejemplo, un vale de impresión de nivel de documento hereda las propiedades de la solicitud de impresión de nivel de trabajo que está asociada a la secuencia de documentos del documento. Del mismo modo, un vale de impresión en el nivel de página hereda las propiedades de la solicitud de impresión de nivel de documento que está asociada con el documento de la página. En este proceso de herencia, las propiedades que se especifican en el vale de impresión de nivel inferior invalidan las propiedades correspondientes que, de lo contrario, se heredarían de la solicitud de impresión de nivel superior.

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

 

 



