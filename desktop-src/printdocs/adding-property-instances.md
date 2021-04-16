---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: Agregar instancias de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08e3df1b6c271c37c080968cc775ac11eba2e3ce
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424143"
---
# <a name="adding-property-instances"></a>Agregar instancias de propiedad

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema de impresión permite que las instancias de la propiedad estén presentes en una instancia de opción. Las instancias de propiedad definidas en el documento de PrintCapabilities no se propagan a las instancias de opción guardadas en el PrintTicket. Los elementos de propiedad no afectan al resultado del proceso de puntuación cuando se comparan dos instancias de opción, pero las instancias de ScoredProperty afectan a este proceso. Todos los controladores de dispositivos que implementan un algoritmo de puntuación deben observar esta Convención. Los proveedores de PrintCapabilities pueden agregar instancias de propiedad a una opción si estas instancias son específicas de esa opción concreta y no otras, o si el proveedor intenta que aparezca el valor de esta propiedad para cada opción de la característica. Por ejemplo, supongamos que la propiedad PrintRate depende de la opción seleccionada para la característica PageResolution. Si la propiedad PrintRate se colocó en el nivel raíz del documento de PrintCapabilities, tendría un solo valor y reflejaría solo la tasa de impresión para la resolución seleccionada actualmente. Sin embargo, si la propiedad PrintRate se colocó dentro de cada opción PageResolution, cada instancia de la propiedad PrintRate podría reflejar la tasa de impresión de la opción PageResolution que la contenía. El documento PrintCapabilities incluiría varias definiciones para PrintRate, una correspondiente a cada opción PageResolution. Con una representación abreviada, la PrintCapabilities contendría:

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

En algunas situaciones, la colocación de una propiedad de velocidad de impresión dentro de cada opción de resolución es más conveniente para el cliente, ya que el cliente puede determinar de un vistazo el efecto que tiene cada opción de resolución en la tasa de impresión, sin necesidad de obtener un nuevo documento de PrintCapabilities para cada configuración de resolución.

Tenga en cuenta también que las instancias de propiedad también se pueden agregar como elementos secundarios de los elementos de característica. Esto resulta útil si hay instancias de propiedad o valores de instancias de propiedad que son específicos de cada característica. Por ejemplo, puede haber una propiedad que especifique si solo se permite seleccionar una opción al mismo tiempo para una característica o si se pueden seleccionar varias opciones. Este es el PICKing \_ , seleccione \_ muchas propiedades que se usan en los archivos PPD y GPD. Dado que es posible que algunas instancias de características se identifiquen como seleccione \_ una, mientras que otras podrían identificarse como picking \_ many, esta propiedad debe definirse para cada característica. La búsqueda de la propiedad como un elemento secundario de la característica produce la asociación entre la propiedad y la característica.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



