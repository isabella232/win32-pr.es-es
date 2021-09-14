---
description: Los reconocedores de Microsoft usan los siguientes GUID.
ms.assetid: dcf6bc5a-1b61-48f7-bc7a-f74ae6e2e57e
title: GUID de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2eb089a9b3b5c7863f2d57d9a635b9ab042ae6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247730"
---
# <a name="property-guids"></a>GUID de propiedad

Los reconocedores de Microsoft usan los siguientes GUID. Siempre que sea posible, las aplicaciones deben usar estos GUID. Sin embargo, se espera y se recomienda que otros reconocedores usen GUID adicionales para las propiedades que no son compatibles con los reconocedores de Microsoft.

Todas las funciones de propiedad se han desarrollado con la comprensión de que otros reconocedores pueden ampliar la lista de GUID. Estas funciones de propiedad incluyen:

-   [**GetContextPropertyList (Función)**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertylist)
-   [**GetContextPropertyValue (Función)**](/windows/desktop/api/recapis/nf-recapis-getcontextpropertyvalue)
-   [**GetResultPropertyList (Función)**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)
-   [**SetContextPropertyValue (Función)**](/windows/desktop/api/recapis/nf-recapis-setcontextpropertyvalue)

En la tabla siguiente se enumeran los GUID de propiedad de Tablet PC definidos en msplataforma.h (instalados en c: Archivos de programa Microsoft \\ Tablet PC Platform SDK Include de forma \\ \\ predeterminada).



| GUID                                                  | Definición                                                                                   |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------|
| INKRECOGNITIONPROPERTY \_ BOXNUMBER<br/>          | Índice de cuadro alternativo del reconocedor en modo de cuadro<br/>                                    |
| INKRECOGNITIONPROPERTY \_ LINENUMBER<br/>         | Número de línea<br/>                                                                   |
| SEGMENTACIÓN \_ INKRECOGNITIONPROPERTY<br/>       | Cómo el reconocedor segmenta palabras y caracteres<br/>                                  |
| INKRECOGNITIONPROPERTY \_ HOTPOINT<br/>           | Punto de acceso de gesto<br/>                                                             |
| INKRECOGNITIONPROPERTY \_ MAXIMUMSTROKECOUNT<br/> | Número máximo de trazos para un segmento<br/>                                           |
| INKRECOGNITIONPROPERTY \_ POINTSPERINCH<br/>      | Métrica de puntos por pulgada<br/>                                                        |
| INKRECOGNITIONPROPERTY \_ CONFIDENCELEVEL<br/>    | [**CONFIANZA \_ Enumeración LEVEL**](/windows/win32/api/rectypes/ne-rectypes-confidence_level)<br/>                         |
| INKRECOGNITIONPROPERTY \_ LINEMETRICS<br/>        | Información para calcular la línea base, la línea media o ambas, que se usa en el entramado<br/> |



 

 

 




