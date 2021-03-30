---
description: Los reconocedores de Microsoft usan los siguientes GUID.
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: GUID de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2eb089a9b3b5c7863f2d57d9a635b9ab042ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156873"
---
# <a name="property-guids"></a>GUID de propiedad

Los reconocedores de Microsoft usan los siguientes GUID. Siempre que sea posible, las aplicaciones deben usar estos GUID. Sin embargo, se espera y se recomienda que otros reconocedores usen GUID adicionales para las propiedades que no son compatibles con los reconocedores de Microsoft.

Todas las funciones de propiedad se han desarrollado con la comprensión de que otros reconocedores pueden extender la lista de GUID. Estas funciones de propiedad incluyen:

-   [**GetContextPropertyList función)**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [**GetContextPropertyValue función)**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [**GetResultPropertyList función)**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [**SetContextPropertyValue función)**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

En la tabla siguiente se enumeran los GUID de propiedades de Tablet PC definidos en msinkaut. h (instalado en c: \\ archivos de programa \\ Microsoft Tablet PC Platform SDK \\ incluir de forma predeterminada).



| GUID                                                  | Definición                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| INKRECOGNITIONPROPERTY \_ BOXNUMBER<br/>          | Índice de cuadro alternativo del reconocedor en modo de cuadro<br/>                                    |
| INKRECOGNITIONPROPERTY \_ LINENUMBER<br/>         | El número de línea<br/>                                                                   |
| \_segmentación INKRECOGNITIONPROPERTY<br/>       | Cómo el reconocedor segmenta las palabras y los caracteres<br/>                                  |
| INKRECOGNITIONPROPERTY \_ Hotpoint<br/>           | El punto de acceso directo del gesto<br/>                                                             |
| INKRECOGNITIONPROPERTY \_ MAXIMUMSTROKECOUNT<br/> | Número máximo de trazos para un segmento<br/>                                           |
| INKRECOGNITIONPROPERTY \_ POINTSPERINCH<br/>      | La métrica de puntos por pulgada<br/>                                                        |
| INKRECOGNITIONPROPERTY \_ CONFIDENCELEVEL<br/>    | [**Confianza \_**](/windows/win32/api/rectypes/ne-rectypes-confidence_level) Enumeración de nivel<br/>                         |
| INKRECOGNITIONPROPERTY \_ LINEMETRICS<br/>        | Información sobre el cálculo de la línea base, la línea media o ambas, que se usa en el Lattice<br/> |



 

 

 




