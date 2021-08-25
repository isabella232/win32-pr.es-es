---
description: Asignación de soluciones a la infraestructura de controles parentales
ms.assetid: 09677019-2cf9-43fe-b16c-e802767bef3a
title: Asignación de soluciones a la infraestructura de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dcf16ec2d656828921ccd6992f2811dcf4590ab06731d1ac6474fd8d7625c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951975"
---
# <a name="mapping-solutions-onto-the-parental-controls-infrastructure"></a>Asignación de soluciones a la infraestructura de controles parentales

Hay cinco categorías de ofertas comunes que tienen en cuenta los controles parentales de ISV e ISP/portal:

-   Aplicación cliente independiente. Algunos ejemplos son los clientes de correo electrónico y los reproductores multimedia. Aunque los reproductores multimedia tienen riesgos orientados a Internet y algunos tienen servicios específicos, los controles parentales de Windows promueven principalmente el registro y las restricciones en las actividades de reproducción solo para minimizar los impactos de la biblioteca y el ruido de registro para los administradores.
-   Soluciones cliente/servidor. Los ejemplos más destacados son las soluciones de mensajería instantánea.
-   Conjuntos de ISP. Se trata de colecciones de soluciones cliente/servidor y aplicaciones cliente, a menudo integradas en una única interfaz de usuario de cliente. Tenga en cuenta que la mayoría de ellas también proporcionan la mayoría o toda la funcionalidad mediante el acceso al explorador, y se cruzan en soluciones solo web.
-   Soluciones solo web. Se accede a través del explorador. Algunos ejemplos son el correo electrónico basado en web y la funcionalidad de mensajería instantánea. El acceso a estos puede bloquearse mediante categorías de filtros web rellenadas adecuadamente.
-   Soluciones de tipo firewall. Proporciona filtrado en el nivel de pila de red y posiblemente otras restricciones del sistema operativo.

Recomendaciones para implementar soluciones compatibles para cada categoría se especifican en la tabla siguiente.



| Category                           | Registro                                                  | Configuración de restricciones                                    | Aplicación de restricciones                                 | Reemplazo del filtro de contenido web                                                        | Uso del vínculo de extensibilidad para el acceso de registro y configuración               |
|------------------------------------|----------------------------------------------------------|----------------------------------------------------------|----------------------------------------------------------|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Cliente "independiente"<br/>    | Obligatorio en el cliente<br/>                            | Obligatorio en el cliente<br/>                            | Obligatorio en el cliente<br/>                            | N/D<br/>                                                                        | Obligatorio, será exe. Puede invocar simplemente la navegación de la interfaz de usuario de la aplicación<br/>   |
| Solución cliente/servidor<br/>  | Obligatorio en el cliente si no lo realiza el servidor<br/> | Obligatorio en el cliente si no lo realiza el servidor<br/> | Obligatorio en el cliente si no lo realiza el servidor<br/> | N/D<br/>                                                                        | Obligatorio, será exe<br/>                                        |
| Conjunto de isp<br/>               | Obligatorio en el cliente si no lo realiza el servidor<br/> | Obligatorio en el cliente si no lo realiza el servidor<br/> | Obligatorio en el cliente si no lo realiza el servidor<br/> | Se recomienda usar el filtro WPC, pero permitir el reemplazo si es sólido para varios usuarios<br/> | Obligatorio, será exe<br/>                                        |
| Solución solo web<br/>       | Se recomienda realizar en el servidor<br/>                | Se recomienda realizar en el servidor<br/>                | Se recomienda realizar en el servidor<br/>                | N/D<br/>                                                                        | Se recomienda su uso. Exposición del registro y la configuración del servidor mediante exe<br/> |
| Soluciones de firewall<br/> | Obligatorio en el cliente<br/>                            | Obligatorio en el cliente<br/>                            | Obligatorio en el cliente<br/>                            | Se recomienda usar el filtro WPC, pero permitir el reemplazo si es sólido para varios usuarios<br/> | Obligatorio, será exe<br/>                                        |



 

 

 




