---
title: Dependencia de configuración de PrintCapabilities
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 9b1f3f49-2a4a-4413-9708-a430011314e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e7f376d8bd0dab823adb3a2e0665db27508b1d7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "103914258"
---
# <a name="configuration-dependency-in-the-printcapabilities-schema"></a>Dependencia de configuración en el esquema de PrintCapabilities

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema de PrintCapabilities es muy similar al marco del esquema de impresión, en términos de los elementos usados y la estructura general expresada por los elementos primarios y secundarios. Las dependencias de configuración, que pertenecen específicamente a PrintCapabilities, se enumeran aquí como una extensión del marco de trabajo general. Las dependencias de configuración hacen referencia al hecho de que algunos elementos, incluido su contenido, se pueden modificar o incluso eliminar de un documento de PrintCapabilities al siguiente, como resultado de las dependencias de la configuración. Incluso si se requiere que un elemento primario sea independiente de la configuración, sus elementos secundarios pueden tener dependencias. Estas dependencias se expresan mediante \* construcciones switch/ \* Case en archivos GPD.

Como ejemplo de una dependencia de configuración, tenga en cuenta los valores asociados a cada propiedad en el documento de PrintCapabilities. Cada documento de PrintCapabilities puede diferir en las instancias de propiedad que se definen y en las instancias de valor asignadas a esas instancias de propiedad.



| Tipo de elemento                                                                                                                                                                             | Dependencia de configuración                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Característica <br/> Opción<br/> ParameterInit<br/> ParameterRef<br/> PrintCapabilities<br/> PrintTicket<br/> Propiedad<br/> ScoredProperty<br/> | Estos elementos no deben tener dependencias de configuración.<br/>                                                                                                                                                           |
| ParameterDef <br/>                                                                                                                                                                 | Los elementos y elementos de ParameterDef contenidos en ellos en cualquier nivel de anidamiento no deben tener ninguna dependencia de configuración.<br/>                                                                                        |
| Propiedad <br/>                                                                                                                                                                     | Los elementos de propiedad pueden tener dependencias de configuración, excepto cuando aparecen en elementos ParameterDef.<br/>                                                                                                       |
| Value <br/>                                                                                                                                                                        | Los elementos de valor que aparecen dentro de los elementos ScoredProperty no deben tener ninguna dependencia de configuración. Los elementos de valor que aparecen dentro de un elemento de propiedad pueden tener dependencias arbitrarias en la configuración.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




