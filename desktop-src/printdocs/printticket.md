---
description: Busque información sobre el elemento PrintTicket. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a38638083f6a6aabd0290fa3466a30fd50f7375
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248415"
---
# <a name="printticket"></a>PrintTicket

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento PrintTicket es el elemento raíz del documento PrintTicket. Un elemento PrintTicket contiene toda la información de formato de trabajo necesaria para generar un trabajo.

## <a name="element-tag"></a>Etiqueta de elemento

&lt;PrintTicket&gt;

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML      | Detalles                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Especifica la versión del esquema que define los tipos de elemento y su estructura, un literal de tipo integer. La versión del esquema actual es "1". Este atributo es necesario. <br/> |



 

Para más información, consulte la [sección Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Detalles                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | Solo raíz del documento.<br/>                                                                                     |
| Elementos secundarios<br/>  | *Característica* (cero o más)<br/> *ParameterInit* (cero o más)<br/> *Propiedad* (cero o más)<br/> |
| Este elemento<br/>    | No se permiten datos de caracteres.<br/> No se permiten elementos secundarios duplicados relacionados.<br/>                  |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Las dependencias de configuración solo se aplican a los elementos de un documento PrintCapabilities.

## <a name="example"></a>Ejemplo

Vea [ejemplo de PrintTicket.](printticket-example.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




