---
description: Windows Componentes del mismo nivel para Equipos a mi alrededor
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Windows Componentes del mismo nivel para Equipos a mi alrededor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762ea58aa9738bfe01e23844dd146e4de8a6a5f76433ef969b60b30fb5886db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011503"
---
# <a name="windows-peer-components-for-people-near-me"></a>Windows Componentes del mismo nivel para Equipos a mi alrededor

Dentro del archivo ejecutable Windows redes del mismo nivel (P2phost.exe), la arquitectura de Equipos a mi alrededor [usa](people-near-me-architecture.md) los siguientes componentes:

### <a name="people-near-me"></a>People Near Me (Gente que esté cerca)

El Equipos a mi alrededor (PNM) inicia la detección mediante la detección de servicios web en la subred local para los nombres de usuario de equipos compatibles con PNM.

### <a name="people-near-me-publisher"></a>Equipos a mi alrededor Publisher

El Equipos a mi alrededor Publisher publica los alias de los usuarios que han iniciado sesión para indicar la disponibilidad en otros equipos mediante PNM en la subred local. El usuario que inició sesión debe elegir publicar su alias antes de anunciarlo. El alias se publica en la subred mediante la detección de servicios web. Además, también se pueden publicar objetos y aplicaciones. Sin embargo, el usuario debe especificar la publicación de objetos y aplicaciones **para los** ámbitos Equipos a mi alrededor ' o '**All**'.

### <a name="people-near-me-enumerator"></a>Equipos a mi alrededor enumerador

El Equipos a mi alrededor de enumeración enumera la lista de usuarios de la subred local. Con esta lista, la detección de servicios web envía una consulta de multidifusión y recibe las respuestas. Una vez obtenida la lista de alias, una aplicación puede usar la API para recuperar más datos publicados por el usuario (que se cifran mediante [SChannel),](windows-vista-components-for-people-near-me.md)como la lista de aplicaciones registradas y cualquier objeto que se publique.

El proceso de búsqueda y enumeración no se realiza automáticamente, pero debe iniciarse explícitamente por un usuario o una aplicación iniciando sesión en PNM. Los resultados de la búsqueda son la lista de alias de otros usuarios de la misma subred que anuncian sus alias mediante la API PNM.

### <a name="publication-manager"></a>Administrador de publicaciones

El componente Administrador de publicaciones es responsable de publicar actualizaciones de presencia, aplicación u objeto a contactos o personas cercanas que están suscritas o sondean los datos.

### <a name="peer-signaling"></a>Señalización del mismo nivel

El componente Peer Signaling controla la creación de conexiones entre pares para intercambiar datos. Por Equipos a mi alrededor, la señalización del mismo nivel se usa cuando un usuario o una aplicación envía la consulta de unidifusión a un equipo específico para su clave pública, aplicaciones y objetos.

### <a name="receive-invitation-handlerux"></a>Controlador de invitación de recepción/experiencia de usuario

El componente Receive Invitation Handler/UX (Controlador de invitación de recepción/experiencia de usuario) recibe una invitación entrante de otra persona, solicita al usuario que determine si quiere iniciar la aplicación asociada a la invitación y, a continuación, inicia la aplicación en función del usuario que acepte la invitación. Una invitación es un mensaje de otra persona para iniciar la actividad de colaboración mediante una aplicación específica instalada en los equipos de ambos usuarios y anunciada por el usuario invitado.

### <a name="peer-security"></a>Seguridad del mismo nivel

Cuando se envían presencia, aplicación y objeto, la información se cifra mediante un canal SSL[(Schannel).](windows-vista-components-for-people-near-me.md) El equipo de inicio usa la clave pública del equipo invitado para negociar una clave secreta que se usa para cifrar los datos subsiguientes enviados entre los dos elementos del mismo nivel.

 

 



