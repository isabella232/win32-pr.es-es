---
description: Asignación de soluciones a la infraestructura de controles parentales
ms.assetid: 09677019-2cf9-43fe-b16c-e802767bef3a
title: Asignación de soluciones a la infraestructura de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea410663af2e3b2363b7026a6997da5c19a1077a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706311"
---
# <a name="mapping-solutions-onto-the-parental-controls-infrastructure"></a>Asignación de soluciones a la infraestructura de controles parentales

Cinco categorías de ofertas comunes de ISV y ISP/el portal de control parental son evidentes:

-   Aplicación cliente independiente. Algunos ejemplos son los clientes de correo electrónico y los reproductores multimedia. Aunque los reproductores multimedia tienen un riesgo orientado a Internet y algunos tienen servicios específicos, los controles parentales de Windows solo fomentan el registro y las restricciones en las actividades de reproducción para minimizar el impacto de la biblioteca y el registro de ruido en los administradores.
-   Soluciones cliente/servidor. Los ejemplos más destacados son las soluciones de mensajería instantánea.
-   Conjuntos de servicios de Internet. Se trata de colecciones de soluciones cliente/servidor y aplicaciones cliente, que a menudo están integradas en una sola interfaz de usuario de cliente. Tenga en cuenta que la mayoría de estos también proporcionan la mayoría o todas las funciones mediante el acceso al explorador, pasando por las soluciones solo en Web.
-   Soluciones solo Web. Se obtiene acceso a través del explorador. Algunos ejemplos son la funcionalidad de correo electrónico y mensajería instantánea basada en Web. El acceso a estos pueden estar bloqueados por categorías de filtro Web debidamente rellenadas.
-   Soluciones de tipo Firewall. Proporciona filtrado en el nivel de pila de red y, potencialmente, otras restricciones del sistema operativo.

En la tabla siguiente se especifican recomendaciones para implementar soluciones compatibles para cada categoría.



| Category                           | Registro                                                  | Configuración de restricciones                                    | Cumplimiento de restricciones                                 | Reemplazo de filtro de contenido web                                                        | Uso del vínculo de extensibilidad para el acceso de registro y configuración               |
|------------------------------------|----------------------------------------------------------|----------------------------------------------------------|----------------------------------------------------------|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Cliente "independiente"<br/>    | Requerido en el cliente<br/>                            | Requerido en el cliente<br/>                            | Requerido en el cliente<br/>                            | N/D<br/>                                                                        | Requerido, será exe. Puede simplemente invocar la navegación de la IU de la aplicación<br/>   |
| Solución cliente/servidor<br/>  | Requerido en el cliente si no lo realiza el servidor<br/> | Requerido en el cliente si no lo realiza el servidor<br/> | Requerido en el cliente si no lo realiza el servidor<br/> | N/D<br/>                                                                        | Requerido, será exe<br/>                                        |
| Conjunto de servicios de Internet<br/>               | Requerido en el cliente si no lo realiza el servidor<br/> | Requerido en el cliente si no lo realiza el servidor<br/> | Requerido en el cliente si no lo realiza el servidor<br/> | Se recomienda usar el filtro WPC, pero permitir el reemplazo si es sólido para varios usuarios<br/> | Requerido, será exe<br/>                                        |
| Solución solo Web<br/>       | Recomendar rendimiento en el servidor<br/>                | Recomendar rendimiento en el servidor<br/>                | Recomendar rendimiento en el servidor<br/>                | N/D<br/>                                                                        | Se recomienda su uso. Exponer la configuración y el registro del servidor mediante el uso de exe<br/> |
| Soluciones similares a Firewall<br/> | Requerido en el cliente<br/>                            | Requerido en el cliente<br/>                            | Requerido en el cliente<br/>                            | Se recomienda usar el filtro WPC, pero permitir el reemplazo si es sólido para varios usuarios<br/> | Requerido, será exe<br/>                                        |



 

 

 




