---
description: Obtenga información sobre cómo agregar instancias de propiedad. El esquema de impresión permite que las instancias de propiedad se presenten en una instancia de Option.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Agregar instancias de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af1a84435ec67c3f27615693e153c6a764e4451d93cb7ff5c73970a39587296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950805"
---
# <a name="adding-property-instances"></a>Agregar instancias de propiedad

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema de impresión permite que las instancias de propiedad se presenten en una instancia de Option. Las instancias de propiedad definidas en el documento PrintCapabilities no se propagan a las instancias de Option guardadas en PrintTicket. Los elementos property no afectan al resultado del proceso de puntuación cuando se comparan dos instancias de Option, pero las instancias scoredProperty afectan a este proceso. Todos los controladores de dispositivo que implementan un algoritmo de puntuación deben cumplir esta convención. Los proveedores de PrintCapabilities pueden agregar instancias de propiedad a una opción si estas instancias son específicas de esa opción concreta y ninguna otra, o si el proveedor pretende que el valor de esta propiedad aparezca para cada opción de la característica. Por ejemplo, suponga que la propiedad PrintRate depende de la opción seleccionada para la característica PageResolution. Si la propiedad PrintRate se colocara en el nivel raíz del documento PrintCapabilities, sería de un solo valor y reflejaría solo la velocidad de impresión de la resolución seleccionada actualmente. Sin embargo, si la propiedad PrintRate se colocara dentro de cada opción PageResolution, cada instancia de la propiedad PrintRate podría reflejar la velocidad de impresión de la opción PageResolution que la contenía. El documento PrintCapabilities contendrá varias definiciones para PrintRate, una correspondiente a cada opción PageResolution. Con una representación abreviada, PrintCapabilities contendrá:

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:string">800dpi</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:string">600dpi</psf:Value>
    </psf:ScoredProperty>
    <!-- Note: The following Property is not part of the Print Schema Framework -->
    <!-- It is included for illustration purposes. -->
    <!-- It is shown as a privately defined implementation-->
    <Property name="FabrikamES500:PrintRate">
      <Value xsi:type="string">20ppm</Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

En algunas situaciones, colocar una propiedad de velocidad de impresión dentro de cada opción de resolución es más conveniente para el cliente, ya que el cliente puede determinar de un vistazo el efecto que cada opción de resolución tiene en la velocidad de impresión, sin necesidad de obtener un nuevo documento PrintCapabilities para cada configuración de resolución.

Tenga en cuenta también que las instancias de propiedad también se pueden agregar como elementos secundarios de elementos Feature. Esto resulta útil si hay instancias de propiedad o valores de instancias de propiedad que son específicos de cada característica. Por ejemplo, puede haber una propiedad que especifique si solo se permite seleccionar una opción a la vez para una característica o si se pueden seleccionar varias opciones. Esta es la propiedad PICK \_ ONE, PICK \_ MANY que se usa en los archivos PPD y GPD. Dado que algunas instancias de característica se podrían identificar como PICK ONE, mientras que otras se podrían identificar como PICK MANY, esta propiedad debe definirse \_ \_ para cada característica. La búsqueda de la propiedad como un elemento secundario de la característica genera la asociación entre la propiedad y la característica.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



