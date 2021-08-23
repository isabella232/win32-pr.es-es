---
description: Obtenga información sobre el elemento Option. Este tema no está actual. Para obtener la información más reciente, vea Especificación del esquema de impresión.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Opción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f02f506c61353698bc4386541ea96dbf858790dd7c34c6d80b8dc2542c46a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098979"
---
# <a name="option"></a>Opción

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Un elemento Option contiene todos los elementos Property y ScoredProperty asociados a esta opción.

## <a name="element-tag"></a>Etiqueta de elemento

<Option>

## <a name="xml-attributes"></a>Atributos XML

En la tabla siguiente se enumeran los atributos XML que pueden pertenecer a este elemento.



| Atributo XML          | Detalles                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Limitada<br/> | Este atributo es opcional para un documento PrintCapabilities.<br/> Este atributo indica si la opción está disponible para su selección o uso. Este atributo XML se puede establecer en uno de los siguientes valores: None, PrintTicketSettings, AdminSetting o DeviceSettings. <br/> Consulte [Atributos XML.](xml-attributes.md)<br/> |
| name<br/>        | Contiene el nombre de la opción, ya sea una opción estándar o una opción definida de forma privada. El atributo XML se usa de esta manera para diferenciar entre las instancias de Option. <br/>                                                                                                                                                        |



 

Para más información, consulte la [sección Atributos XML.](xml-attributes.md)

## <a name="element-information"></a>Información de elemento

En la tabla siguiente se enumeran los elementos que pueden ser elementos primarios de este elemento, los elementos que pueden ser elementos secundarios de este elemento y cualquier restricción en el propio elemento.



| Category                   | Detalles                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elementos primarios<br/> | Característica <br/>                                                                                                                                                                                                                                                                              |
| Elementos secundarios<br/>  | *Propiedad* (cero o más)<br/> *ScoredProperty* (cero o más para Opciones con el atributo XML 'name'; una o varias para Opciones que no utilizan el atributo XML \* 'name')<br/> \* solo las opciones públicas definidas en el esquema de impresión no pueden tener ningún atributo 'name', como DocumentNUp)<br/> |
| Este elemento<br/>    | No se permiten datos de caracteres.<br/> No se permiten elementos secundarios duplicados relacionados.<br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a>Dependencias de configuración

Es posible que un elemento de definición option no tenga dependencias de configuración.

## <a name="element-usage"></a>Uso de elementos

El propósito del elemento Option es caracterizar uno de los estados que un atributo de configuración de dispositivo, representado por un elemento Feature, puede asumir. Cada definición de elemento Option contiene uno o varios elementos ScoredProperty que describen una característica intrínseca o esencial de esa opción. Para facilitar la portabilidad y la conservación de la intención, el esquema de impresión define muchos elementos de características comunes y una variedad de elementos Option para cada característica. Por lo tanto, es importante usar elementos Option definidos por el esquema de impresión, si es posible, antes de crear sus propias definiciones de opción. Comprender el proceso de definición de elementos Option proporciona información útil sobre la forma en que se usan el documento PrintCapabilities y PrintTickets en la versión 3.0 de Microsoft .NET Framework y la arquitectura de impresión Windows Vista.

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se define un nombre para la opción .

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




