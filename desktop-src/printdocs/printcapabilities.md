---
description: Obtenga información sobre el elemento PrintCapabilities, que representa la raíz del documento PrintCapabilities.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef035015e8024954b32d17dd87bab929221ac78
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883931"
---
# <a name="printcapabilities"></a>PrintCapabilities

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento PrintCapabilities representa la raíz del documento PrintCapabilities. El documento PrintCapabilities contiene toda la información necesaria para describir los atributos de dispositivo admitidos, dada una configuración de dispositivo determinada.

## <a name="element-tag"></a>Etiqueta de elemento

&lt;PrintCapabilities&gt;

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML      | Detalles                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| version<br/> | Especifica la versión del esquema que define los tipos de elemento y su estructura. El atributo version es de tipo integer. La versión del esquema actual se designa como "1". Este atributo es necesario. <br/> |



 

Para obtener más información, vea la [sección Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Detalles                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | Solo raíz del documento.<br/>                                                                                    |
| Elementos secundarios<br/>  | *Característica* (cero o más)<br/> *ParameterDef* (cero o más)<br/> *Propiedad* (cero o más)<br/> |
| Este elemento<br/>    | No se permiten datos de caracteres.<br/> No se permiten elementos secundarios duplicados del mismo nivel.<br/>                 |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Es posible que el elemento raíz no tenga dependencias de configuración.

## <a name="example"></a>Ejemplo

Vea [el ejemplo del documento PrintCapabilities](printcapabilities-document-example.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




