---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Opción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379834d12cd01847c95783d727be5dcdc6c575bf
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105717429"
---
# <a name="option"></a>Opción

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento OPTION contiene todos los elementos Property y ScoredProperty asociados a esta opción.

## <a name="element-tag"></a>Etiqueta de elemento

<Option>

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML          | Detalles                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| restringida<br/> | Este atributo es opcional para un documento de PrintCapabilities.<br/> Este atributo indica si la opción está disponible para la selección o el uso. Este atributo XML se puede establecer en uno de los siguientes valores: None, PrintTicketSettings, AdminSetting o DeviceSettings. <br/> Vea [atributos XML](xml-attributes.md)<br/> |
| name<br/>        | Contiene el nombre de la opción, ya sea una opción estándar o una opción definida de forma privada. El atributo XML se utiliza de esta manera para diferenciar entre las instancias de opción. <br/>                                                                                                                                                        |



 

Para obtener más información, consulte la sección [atributos XML](xml-attributes.md) .

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Detalles                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | Característica <br/>                                                                                                                                                                                                                                                                              |
| Elementos secundarios<br/>  | *Propiedad* (cero o más)<br/> *ScoredProperty* (cero o más para las opciones con el atributo XML ' name '; una o más para las opciones que no usan el atributo XML ' name ' \* )<br/> \* solo las opciones públicas definidas en el esquema de impresión no pueden tener ningún atributo ' name ', como DocumentNUp)<br/> |
| Este elemento<br/>    | No se permiten datos de caracteres.<br/> No se permiten nodos secundarios duplicados.<br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Un elemento de definición de opción no puede tener ninguna dependencia de configuración.

## <a name="element-usage"></a>Uso de elementos

El propósito del elemento OPTION es caracterizar uno de los Estados que puede asumir un atributo de configuración de dispositivo, representado por un elemento de característica. Cada definición de elemento de opción contiene uno o más elementos ScoredProperty que describen la característica intrínseca o esencial de esa opción. Para facilitar la portabilidad y la preservación de la intención, el esquema de impresión define muchos elementos de características comunes y una variedad de elementos de opción para cada característica. Por lo tanto, es importante usar elementos de opción de impresión definidos por el esquema, si es posible, antes de crear sus propias definiciones de opciones. Entender el proceso de definición de los elementos de opción proporciona información útil sobre la manera en que se usan el documento y elementos PrintTicket de PrintCapabilities en la arquitectura de impresión de Microsoft .NET Framework 3,0 y Windows Vista.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se define un nombre para la opción.

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




