---
title: Funciones del método del mismo nivel eaphost Run-Time
description: Obtenga información sobre las funciones en tiempo de ejecución de EAPHost Peer Method API. Consulte una lista de funciones y vea los recursos disponibles adicionales.
ms.assetid: fdfa595d-acf7-4489-88a8-113093567fe5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfde4adc8d509fcd5d67f9a33bd0617d605716db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241293"
---
# <a name="eaphost-peer-method-run-time-functions"></a>Funciones del método del mismo nivel eaphost Run-Time

Las funciones en tiempo de ejecución de EAP Peer Method API son las siguientes.



| Función                                                                   | Descripción                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                         | Inicia una nueva sesión de autenticación en el EAPHost del mismo nivel.                                                                                                                                                                    |
| [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession)                             | Finaliza una sesión de autenticación eap actual entre EAPHost y el par.                                                                                                                                               |
| [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) | Permite a los desarrolladores de métodos EAP proporcionar las distintas propiedades de conexión y propiedades de usuario compatibles con el método . EAPHost invoca esta función para crear la propiedad de conexión y la propiedad de usuario del método EAP. |
| [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity)                           | Obtiene la identidad del método EAP que está llamando.                                                                                                                                                                    |
| [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo)                                   | Obtiene un conjunto de punteros de función para una implementación del método del mismo nivel EAP cargado.                                                                                                                                     |
| [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes)       | Obtiene una matriz de atributos de EAP del método EAP.                                                                                                                                                                     |
| [**EapPeerGetResponsePacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponsepacket)               | Obtiene un paquete de respuesta del método EAP.                                                                                                                                                                              |
| [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult)                               | Obtiene el resultado de una sesión de autenticación del método EAP.                                                                                                                                                        |
| [**EapPeerGetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext)                         | Obtiene el contexto de la interfaz de usuario del método EAP.                                                                                                                                                                     |
| [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize)                             | Inicializa EAPHost para el método del mismo nivel.                                                                                                                                                                                    |
| [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)         | Procesa un paquete recibido por EAPHost desde un suplicante.                                                                                                                                                                   |
| [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials)                     | Proporciona credenciales de usuario nuevas o actualizadas al método EAP.                                                                                                                                                                 |
| [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)       | Proporciona una matriz actualizada de atributos de EAP para el método EAP.                                                                                                                                                              |
| [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)                         | Proporciona un contexto de interfaz de usuario para el método EAP.                                                                                                                                                                        |
| [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown)                                 | Cierra el método EAP y se prepara para descargar el archivo DLL correspondiente.                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de configuración del método del mismo nivel eaphost](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




