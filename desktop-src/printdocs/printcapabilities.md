---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c6dd8ce98b071f1eb239762544a9b72160035
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105721393"
---
# <a name="printcapabilities"></a>PrintCapabilities

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento PrintCapabilities representa la raíz del documento PrintCapabilities. El documento de PrintCapabilities contiene toda la información necesaria para describir los atributos de dispositivo admitidos, dada una configuración de dispositivo concreta.

## <a name="element-tag"></a>Etiqueta de elemento

<PrintCapabilities>

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML      | Detalles                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Especifica la versión del esquema que define los tipos de elemento y su estructura. El atributo version es de tipo Integer. La versión del esquema actual se designa como "1". Este atributo es necesario. <br/> |



 

Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Detalles                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | Solo raíz de documento.<br/>                                                                                    |
| Elementos secundarios<br/>  | *Característica* (cero o más)<br/> *ParameterDef* (cero o más)<br/> *Propiedad* (cero o más)<br/> |
| Este elemento<br/>    | No se permiten datos de caracteres.<br/> No se permiten nodos secundarios duplicados.<br/>                 |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Es posible que el elemento raíz no tenga dependencias de configuración.

## <a name="example"></a>Ejemplo

Vea [ejemplo de documento de PrintCapabilities](printcapabilities-document-example.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




