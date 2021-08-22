---
description: Equipos a mi alrededor requisitos
ms.assetid: c7ab73fc-56a6-4b6c-820a-3f8e4a97cfaf
title: Equipos a mi alrededor requisitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ebbb904175184b6e9d06c807aa4b4ed645c93633114d6b9b64085e34dfa3683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518355"
---
# <a name="people-near-me-requirements"></a>Equipos a mi alrededor requisitos

Para que [Equipos a mi alrededor](about-people-near-me.md) conectividad sin problemas y una colaboración sencilla para los usuarios Windows aplicaciones de redes del mismo nivel, se consigue lo siguiente:

### <a name="people-discovery"></a>Detección de personas

La detección de personas permite a un usuario detectar y mostrar el conjunto de pares que se encuentran en la subred local. Los equipos de la subred local deben anunciar los nombres de los equipos del mismo nivel que han iniciado sesión. Los elementos del mismo nivel enumerados después de una consulta de detección son el conjunto de usuarios que ejecutan Windows Vista que están configurados para anunciar un alias a otros usuarios [mediante Equipos a mi alrededor](about-people-near-me.md). Esta funcionalidad está deshabilitada de forma predeterminada y el usuario que ha iniciado sesión debe habilitarla.

> [!Note]  
> Los pares remotos detectados durante el proceso de detección Equipos a mi alrededor", no son necesariamente los usuarios previstos asociados a los pares detectados.

 

### <a name="extended-data-discovery"></a>Detección de datos extendida

La detección de datos extendida permite buscar usuarios que tienen intereses específicos. También es posible que los usuarios especifiquen que quieren anunciar datos adicionales sobre sí mismos. Por ejemplo, los datos podrían describir intereses profesionales específicos en una conferencia del sector, además del alias del usuario que ha iniciado sesión.

### <a name="application-discovery"></a>Detección de aplicaciones

La naturaleza exacta de la colaboración ad hoc habilitada por Equipos a mi alrededor es específica de las aplicaciones. Por ejemplo, la colaboración podría estar chateando o compartiendo fotos, y ambas requieren aplicaciones específicas. Para que Equipos a mi alrededor habilitar actividades de colaboración, el conjunto de aplicaciones que están disponibles para escenarios Equipos a mi alrededor también se debe anunciar y detectar.

### <a name="subscription"></a>Suscripción

Mediante una suscripción, las aplicaciones pueden suscribirse para realizar un seguimiento de la presencia, las aplicaciones y los cambios de objetos de una persona.

### <a name="invitation"></a>Invitación

Una vez que se han detectado las personas, los intereses y las aplicaciones, la colaboración del mismo nivel, mediante una aplicación de Equipos a mi alrededor, puede iniciar un intercambio de invitación y aceptación. El elemento del mismo nivel que inicia envía un mensaje de invitación a otro elemento del mismo nivel o del mismo nivel. Los usuarios que reciben la invitación pueden aceptar o rechazar la invitación. Cuando se acepta la invitación, se inicia la aplicación del mismo nivel adecuada para la actividad solicitada.

### <a name="add-as-a-contact"></a>Agregar como contacto

Si los usuarios establecen una actividad de colaboración Equipos a mi alrededor y desean mantener el contacto a lo largo del tiempo, pueden agregarse entre sí como contacto. Una vez hecho esto, pueden observar el estado de presencia de un usuario (por ejemplo, en línea, sin conexión o fuera) e invitarlos a una actividad de colaboración en cualquier momento a través de Internet. Cualquier actividad que fuera posible con la persona cuando se encontraba cerca también es posible con un contacto a través de Internet.

### <a name="security"></a>Seguridad

Para proteger a los usuarios y los datos que se intercambian en una actividad de colaboración del mismo nivel, los usuarios tienen control de configuración sobre lo que se anuncia. Los usuarios también deben aceptar una invitación antes de que pueda comenzar la colaboración del mismo nivel. La actividad de colaboración se cifra con un canal Capa de sockets seguros (SSL) cifrado (también conocido como Schannel). SSL es un protocolo criptográfico para proteger las comunicaciones basadas en TCP. Para obtener más información, vea [SChannel](windows-vista-components-for-people-near-me.md). Estos requisitos son compatibles con un nuevo conjunto de componentes de la arquitectura Windows [redes](what-is-peer-networking-.md)del mismo nivel en Windows Vista.

 

 



