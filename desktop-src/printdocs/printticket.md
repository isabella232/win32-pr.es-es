---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d2e225eb38584e290db55c33594be80d0d7999
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105689704"
---
# <a name="printticket"></a>PrintTicket

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento PrintTicket es el elemento raíz del documento PrintTicket. Un elemento PrintTicket contiene toda la información de formato del trabajo necesaria para generar un trabajo.

## <a name="element-tag"></a>Etiqueta de elemento

<PrintTicket>

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML      | Detalles                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Especifica la versión del esquema que define los tipos de elemento y su estructura, un literal de tipo entero. La versión del esquema actual es "1". Este atributo es necesario. <br/> |



 

Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Detalles                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | Solo raíz de documento.<br/>                                                                                     |
| Elementos secundarios<br/>  | *Característica* (cero o más)<br/> *ParameterInit* (cero o más)<br/> *Propiedad* (cero o más)<br/> |
| Este elemento<br/>    | No se permiten datos de caracteres.<br/> No se permiten nodos secundarios duplicados.<br/>                  |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Las dependencias de configuración solo se pueden aplicar a los elementos de un documento de PrintCapabilities.

## <a name="example"></a>Ejemplo

Vea el [ejemplo de PrintTicket](printticket-example.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




