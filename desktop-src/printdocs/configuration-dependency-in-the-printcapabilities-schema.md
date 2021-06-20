---
title: Dependencia de configuración de PrintCapabilities
description: Las dependencias de configuración hacen referencia al hecho de que algunos elementos se pueden modificar o incluso eliminar de un documento PrintCapabilities al siguiente.
ms.assetid: 9b1f3f49-2a4a-4413-9708-a430011314e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20f01c8e7bd9a036a53048996ec5a38246471f67
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409668"
---
# <a name="configuration-dependency-in-the-printcapabilities-schema"></a>Dependencia de configuración en el esquema PrintCapabilities

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema PrintCapabilities está estrechamente en paralelo con el marco de esquema de impresión, en términos de los elementos utilizados y la estructura general expresada por elementos primarios y secundarios. Las dependencias de configuración, que pertenecen específicamente a PrintCapabilities, se enumeran aquí como una extensión para el marco general. Las dependencias de configuración hacen referencia al hecho de que algunos elementos, incluido su contenido, se pueden modificar o incluso eliminar de un documento PrintCapabilities al siguiente, como resultado de las dependencias de la configuración. Incluso si es necesario que un elemento primario sea independiente de la configuración, sus elementos secundarios pueden tener dependencias. Estas dependencias se expresan \* mediante construcciones Switch/Case \* en archivos GPD.

Como ejemplo de una dependencia de configuración, tenga en cuenta los valores asociados a cada propiedad en el documento PrintCapabilities. Cada documento PrintCapabilities puede diferir en las instancias de propiedad definidas y en las instancias de valor asignadas a esas instancias de propiedad.



| Tipo de elemento                                                                                                                                                                             | Dependencia de configuración                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Característica <br/> Opción<br/> ParameterInit<br/> ParameterRef<br/> PrintCapabilities<br/> PrintTicket<br/> Propiedad<br/> ScoredProperty<br/> | Estos elementos no deben tener dependencias de configuración.<br/>                                                                                                                                                           |
| ParameterDef <br/>                                                                                                                                                                 | Los elementos ParameterDef y los elementos contenidos en ellos en cualquier nivel de anidamiento no deben tener dependencias de configuración.<br/>                                                                                        |
| Propiedad <br/>                                                                                                                                                                     | Los elementos de propiedad pueden tener dependencias de configuración, excepto cuando aparecen dentro de elementos ParameterDef.<br/>                                                                                                       |
| Valor <br/>                                                                                                                                                                        | Los elementos value que aparecen dentro de los elementos ScoredProperty no deben tener dependencias de configuración. Los elementos de valor que aparecen dentro de un elemento Property pueden tener dependencias arbitrarias en la configuración.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




