---
description: Requisitos de equipos a mi alrededor
ms.assetid: c7ab73fc-56a6-4b6c-820a-3f8e4a97cfaf
title: Requisitos de equipos a mi alrededor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6afb97800041e0fcd9a10a6d95334b832fb363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909766"
---
# <a name="people-near-me-requirements"></a>Requisitos de equipos a mi alrededor

Para que los equipos a [mi alrededor](about-people-near-me.md) ofrezcan una conectividad sin problemas y una colaboración sencilla a los usuarios de aplicaciones de red del mismo nivel de Windows, se consigue lo siguiente:

### <a name="people-discovery"></a>Detección de personas

La detección de personas permite que un usuario detecte y muestre el conjunto de elementos del mismo nivel que se encuentran en la subred local. Cualquier equipo de la subred local debe anunciar los nombres de los equipos del mismo nivel que han iniciado sesión. Los elementos del mismo nivel enumerados después de una consulta de detección son el conjunto de usuarios que ejecutan Windows Vista y que están configurados para anunciar un alias a otros usuarios mediante [People Near me](about-people-near-me.md). Esta funcionalidad está deshabilitada de forma predeterminada y debe habilitarla el usuario que ha iniciado sesión.

> [!Note]  
> Los equipos de mismo nivel remotos detectados durante el proceso de detección "equipos a mi alrededor" no son necesariamente los usuarios previstos asociados a los pares detectados.

 

### <a name="extended-data-discovery"></a>Detección de datos extendidos

La detección extendida de datos permite realizar búsquedas de usuarios que tienen intereses específicos. También es posible que los usuarios especifiquen que quieren anunciar datos adicionales sobre ellos mismos. Por ejemplo, los datos podrían describir intereses profesionales específicos en una conferencia del sector, además del alias del usuario que ha iniciado sesión.

### <a name="application-discovery"></a>Detección de aplicaciones

La naturaleza exacta de la colaboración ad hoc habilitada por People Near me es específica de las aplicaciones. Por ejemplo, la colaboración podría estar chateando o compartiendo fotos, lo que requiere aplicaciones específicas. Para que los equipos a mi alrededor puedan habilitar las actividades de colaboración, el conjunto de aplicaciones que están disponibles para los escenarios de equipos a mi alrededor también debe anunciarse y detectarse.

### <a name="subscription"></a>Subscription

Mediante una suscripción, las aplicaciones se pueden suscribir para realizar el seguimiento de los cambios de la presencia, las aplicaciones y los objetos de una persona.

### <a name="invitation"></a>Invitación

Una vez que se han descubierto personas, intereses y aplicaciones, la colaboración del mismo nivel con una aplicación de equipos a mi alrededor puede comenzar una invitación y el intercambio de aceptación. El elemento del mismo nivel de inicio envía un mensaje de invitación a otros elementos del mismo nivel o del mismo nivel. Los usuarios que reciben la invitación pueden aceptar o rechazar la invitación. Cuando se acepta la invitación, se inicia la aplicación del mismo nivel adecuada para la actividad solicitada.

### <a name="add-as-a-contact"></a>Agregar como contacto

Si los usuarios establecen una actividad de colaboración a través de People Near me y quieren mantener el contacto a lo largo del tiempo, pueden agregarse entre sí como contacto. Una vez hecho esto, pueden observar el estado de presencia de un usuario (por ejemplo, en línea, sin conexión o fuera) e invitarlos a una actividad de colaboración en cualquier momento a través de Internet. Cualquier actividad que fuera posible con la persona que se encontraba cerca también es posible con un contacto a través de Internet.

### <a name="security"></a>Seguridad

Para proteger los usuarios y los datos que se intercambian en una actividad de colaboración del mismo nivel, los usuarios tienen control de la configuración de lo que se está anunciando. Los usuarios también deben aceptar una invitación para que pueda comenzar la colaboración del mismo nivel. La actividad de colaboración se cifra con un canal cifrado de Capa de sockets seguros (SSL) (también conocido como Schannel). SSL es un protocolo criptográfico para proteger las comunicaciones basadas en TCP. Para obtener más información, vea [Schannel](windows-vista-components-for-people-near-me.md). Estos requisitos se admiten en un nuevo conjunto de componentes de la arquitectura de [red del mismo nivel de Windows](what-is-peer-networking-.md)en Windows Vista.

 

 



