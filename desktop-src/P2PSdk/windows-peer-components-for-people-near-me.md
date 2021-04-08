---
description: Componentes del mismo nivel de Windows para People Near me
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Componentes del mismo nivel de Windows para People Near me
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c780ccad1abd5ce04c1672f66561285831e5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001988"
---
# <a name="windows-peer-components-for-people-near-me"></a>Componentes del mismo nivel de Windows para People Near me

Dentro del archivo ejecutable principal de redes del mismo nivel de Windows (P2phost.exe), la [arquitectura People Near me](people-near-me-architecture.md) usa los siguientes componentes:

### <a name="people-near-me"></a>People Near Me (Gente que esté cerca)

El componente equipos a mi alrededor (PNM) inicia la detección mediante el descubrimiento de servicios web en la subred local para los nombres de usuario de equipos compatibles con PNM.

### <a name="people-near-me-publisher"></a>Publicador de equipos a mi alrededor

El componente de publicador de equipos a mi alrededor publica los alias de los usuarios que han iniciado sesión para indicar la disponibilidad de otros equipos que usan PNM en la subred local. El usuario que ha iniciado sesión debe elegir publicar su alias antes de que se anuncie. El alias se publica en la subred mediante la detección de servicios Web. Además, también se pueden publicar objetos y aplicaciones. Sin embargo, el usuario debe especificar la publicación de objetos y aplicaciones para los ámbitos "equipos a **mi alrededor**" o "**todos**".

### <a name="people-near-me-enumerator"></a>Enumerador de equipos a mi alrededor

El componente de enumerador People Near me enumera la lista de usuarios de la subred local. Mediante esta lista, la detección de servicios Web envía una consulta de multidifusión y recibe las respuestas. Una vez obtenida la lista de sobrenombres, una aplicación puede usar la API para recuperar más datos publicados por el usuario (cifrado mediante [Schannel](windows-vista-components-for-people-near-me.md)), como la lista de aplicaciones registradas y los objetos que se van a publicar.

El proceso de búsqueda y enumeración no se lleva a cabo automáticamente, pero debe iniciarse explícitamente por un usuario o una aplicación mediante el inicio de sesión en PNM. Los resultados de la búsqueda son la lista de alias de otros usuarios de la misma subred que están anunciando sus sobrenombres mediante la API de PNM.

### <a name="publication-manager"></a>Administrador de publicaciones

El componente del administrador de publicaciones es responsable de publicar las actualizaciones de presencia, aplicación o objeto en contactos o equipos a mi alrededor que estén suscritos o sondeen los datos.

### <a name="peer-signaling"></a>Señalización del mismo nivel

El componente de señalización del mismo nivel controla la creación de conexiones entre pares para intercambiar datos. En el caso de equipos a mi alrededor, la señalización del mismo nivel se usa cuando un usuario o una aplicación envía la consulta de unidifusión a un equipo específico para su clave pública, aplicaciones y objetos.

### <a name="receive-invitation-handlerux"></a>Recibir identificador de invitación/UX

El componente de la experiencia de usuario/controlador de invitación de recepción recibe una invitación entrante de otra persona, pide al usuario que determine si desea iniciar la aplicación asociada a la invitación y, a continuación, inicia la aplicación en función del usuario que acepta la invitación. Una invitación es un mensaje de otra persona para iniciar la actividad de colaboración con una aplicación específica instalada en los equipos de los usuarios y anunciada por el usuario al que se va a invitar.

### <a name="peer-security"></a>Seguridad del mismo nivel

Cuando se envían la presencia, la aplicación y el objeto, la información se cifra mediante un canal SSL ([Schannel](windows-vista-components-for-people-near-me.md)). El equipo iniciador utiliza la clave pública del equipo invitado para negociar una clave secreta que se utiliza para cifrar los datos siguientes enviados entre los dos equipos del mismo nivel.

 

 



