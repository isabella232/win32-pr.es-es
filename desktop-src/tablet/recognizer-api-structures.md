---
description: En esta sección se describen las estructuras del reconocedor.
ms.assetid: 4c17391f-7af4-42ab-b77f-e3c39cadc0b6
title: Estructuras de reconocedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: addaccf3e69f35b99379710d681fe8ac45559ea1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467170"
---
# <a name="recognizer-structures"></a>Estructuras de reconocedor

En esta sección se describen las estructuras del reconocedor.

## <a name="in-this-section"></a>En esta sección



| Estructura                                                    | Descripción                                                                                                                                                   |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INTERVALO DE \_ CARACTERES**](/windows/win32/api/rectypes/ns-rectypes-character_range)                  | Especifica un intervalo de puntos Unicode (caracteres).<br/>                                                                                                  |
| [**MÉTRICAS DE \_ LATTICE**](/windows/win32/api/rectypes/ns-rectypes-lattice_metrics)                  | Describe la línea base y el alto de línea media.<br/>                                                                                                     |
| [**SEGMENTO \_ DE LÍNEA**](/windows/win32/api/rectypes/ns-rectypes-line_segment)                        | Describe los puntos inicial y final de un segmento de reconocimiento de línea, como la línea base o la línea media.<br/>                                                 |
| [**DESCRIPCIÓN DEL \_ PAQUETE**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)            | Describe el contenido del paquete para un contexto de tableta determinado.<br/>                                                                               |
| [**PROPIEDAD \_ PACKET**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property)                  | Describe una propiedad de paquete notificada por el controlador de tableta.<br/>                                                                                 |
| [**MÉTRICAS DE \_ PROPIEDADES**](/windows/desktop/api/tpcshrd/ns-tpcshrd-property_metrics)                | Define el intervalo y la resolución de una propiedad de paquete.<br/>                                                                                             |
| [**\_ATTRS DE RECO**](/windows/win32/api/rectypes/ns-rectypes-reco_attrs)                            | Recupera los atributos de un reconocedor o especifica qué atributos usar al buscar un reconocedor instalado.<br/>                         |
| [**GUÍA \_ DE RECO**](/windows/win32/api/rectypes/ns-rectypes-reco_guide)                            | Define los límites de la entrada de lápiz para el reconocedor.<br/>                                                                                               |
| [**RECO \_ LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)                        | Actúa como punto de entrada en un entramado.<br/>                                                                                                          |
| [**RECO \_ LATTICE \_ COLUMN**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)         | Representa una columna del entramado.<br/>                                                                                                                |
| [**RECO \_ LATTICE, \_ ELEMENTO**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)       | Corresponde a una palabra o a un carácter de Este de Asia, normalmente; sin embargo, un elemento también puede corresponder a un gesto, una forma o algún otro código.<br/> |
| [**PROPIEDADES \_ DE RECO LATTICE \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties) | Contiene una matriz de punteros a estructuras de propiedades.<br/>                                                                                              |
| [**RECO \_ LATTICE, \_ PROPIEDAD**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)     | Contiene una propiedad usada en el entramado.<br/>                                                                                                           |
| [**INTERVALO \_ DE RECO**](/windows/win32/api/rectypes/ns-rectypes-reco_range)                            | Identifica un intervalo de caracteres en la cadena de resultado.<br/>                                                                                             |
| [**INTERVALO DE \_ TRAZO**](/windows/win32/api/tpcshrd/ns-tpcshrd-stroke_range)                        | Especifica un intervalo de trazos en el [**objeto InkDisp.**](inkdisp-class.md)<br/>                                                                       |



 

 

 




