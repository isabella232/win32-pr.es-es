---
title: Descripción de seguridad
description: Una desadición de seguridad se representa mediante una estructura de descripción de seguridad de WS y se proporciona una instancia de una descripción de seguridad cuando se llama a la función WsCreateChannel para crear un canal seguro o la función \_ WsCreateListener para crear un agente de \_ escucha.
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Descripción de seguridad Servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c06e8553441b7eb813106213dbfa089810aad74c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467025"
---
# <a name="security-description"></a>Descripción de seguridad

Una desvocación de seguridad se representa mediante una estructura DE DESCRIPCIÓN DE SEGURIDAD de [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) y se proporciona una instancia de una descripción de seguridad cuando se llama a la función [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) para crear un canal seguro o la función [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) para crear un agente de escucha.


## <a name="structure-of-a-security-description"></a>Estructura de una descripción de seguridad

El modelo básico de seguridad del canal es que un canal está protegido con uno o varios tokens de seguridad. Al reflejar este modelo, la estructura DESCRIPCIÓN DE SEGURIDAD de [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) contiene una lista de enlaces de seguridad, representados por estructuras [**\_ WS SECURITY \_ BINDING,**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) y cada enlace de seguridad describe cómo se obtiene y usa un token de seguridad en el canal. El tipo de seguridad que se usa en un canal se decide mediante la selección de subtipos de enlace de seguridad que se incluyen en la descripción de seguridad.

La configuración de seguridad opcional específica de un enlace de seguridad se especifica como configuración de enlace [de seguridad](security-binding-settings.md) en la estructura de enlace de seguridad; sin embargo, la configuración de todo el canal [](security-channel-settings.md) independiente de  los enlaces de seguridad se especifica directamente como configuración del canal de seguridad en el campo de propiedades de la propia descripción de seguridad.

![Diagrama que muestra la estructura de una descripción de seguridad.](images/securitydescription.png)

Los siguientes elementos de API se usan con descripciones de seguridad.

| Estructura                                                    | Descripción                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**DESCRIPCIÓN DE SEGURIDAD DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | Estructura de nivel superior utilizada para especificar los requisitos de seguridad para un canal (en el lado cliente) o un agente de escucha (en el lado servidor). |



 

 

 




