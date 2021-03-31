---
title: Descripción de seguridad
description: Una descripción de seguridad se representa mediante una \_ \_ estructura de descripción de WS Security, y se proporciona una instancia de una descripción de seguridad al llamar a la función WsCreateChannel para crear un canal seguro o la función WsCreateListener para crear un agente de escucha.
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Servicios Web de descripción de seguridad para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c06e8553441b7eb813106213dbfa089810aad74c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104156980"
---
# <a name="security-description"></a>Descripción de seguridad

Una descripción de seguridad se representa mediante una estructura de [**\_ \_ Descripción de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) , y se proporciona una instancia de una descripción de seguridad al llamar a la función [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) para crear un canal seguro o la función [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) para crear un agente de escucha.


## <a name="structure-of-a-security-description"></a>Estructura de una descripción de seguridad

El modelo básico de seguridad del canal es que un canal está protegido con uno o varios tokens de seguridad. Al reflejar este modelo, la estructura de [**\_ \_ Descripción de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) contiene una lista de enlaces de seguridad, representados por las estructuras de [**\_ \_ enlace de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) , y cada enlace de seguridad describe cómo se obtiene y se utiliza un token de seguridad en el canal. La selección de subtipos de enlace de seguridad que se incluyen en la descripción de seguridad decide el tipo de seguridad que se usa en un canal.

La configuración de seguridad opcional que es específica de un enlace de seguridad se especifica como [configuración de enlace](security-binding-settings.md) de seguridad en la estructura de enlace de seguridad. sin embargo, la configuración de todo el canal independiente de los enlaces de seguridad se especifica directamente como [configuración del canal de seguridad](security-channel-settings.md) en el campo **propiedades** de la descripción de seguridad.

![Diagrama que muestra la estructura de una descripción de seguridad.](images/securitydescription.png)

Los siguientes elementos de API se usan con descripciones de seguridad.

| Estructura                                                    | Descripción                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Descripción de WS \_ Security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | La estructura de nivel superior que se usa para especificar los requisitos de seguridad para un canal (en el lado cliente) o un agente de escucha (en el lado servidor). |



 

 

 




