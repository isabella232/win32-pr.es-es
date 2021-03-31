---
title: Funciones Run-Time del método del mismo nivel
description: Obtenga información sobre las funciones en tiempo de ejecución de la API de método del mismo nivel de EAPHost. Vea una lista de funciones y vea más recursos disponibles.
ms.assetid: fdfa595d-acf7-4489-88a8-113093567fe5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfde4adc8d509fcd5d67f9a33bd0617d605716db
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904821"
---
# <a name="eaphost-peer-method-run-time-functions"></a>Funciones Run-Time del método del mismo nivel

Las funciones de tiempo de ejecución de la API del método EAP del mismo nivel son las siguientes.



| Función                                                                   | Descripción                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)                         | Inicia una nueva sesión de autenticación en EAPHost del mismo nivel.                                                                                                                                                                    |
| [**EapPeerEndSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession)                             | Finaliza una sesión de autenticación EAP actual entre EAPHost y el elemento del mismo nivel.                                                                                                                                               |
| [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) | Permite a los desarrolladores de métodos EAP proporcionar las distintas propiedades de conexión y propiedades de usuario que admite el método. EAPHost invoca esta función para crear la propiedad de conexión y la propiedad de usuario del método EAP. |
| [**EapPeerGetIdentity**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetidentity)                           | Obtiene la identidad para el método EAP al que llama.                                                                                                                                                                    |
| [**EapPeerGetInfo**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetinfo)                                   | Obtiene un conjunto de punteros de función para una implementación del método cargado EAP del mismo nivel.                                                                                                                                     |
| [**EapPeerGetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponseattributes)       | Obtiene una matriz de atributos EAP del método EAP.                                                                                                                                                                     |
| [**EapPeerGetResponsePacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresponsepacket)               | Obtiene un paquete de respuesta del método EAP.                                                                                                                                                                              |
| [**EapPeerGetResult**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetresult)                               | Obtiene el resultado de una sesión de autenticación desde el método EAP.                                                                                                                                                        |
| [**EapPeerGetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetuicontext)                         | Obtiene el contexto de la interfaz de usuario del método EAP.                                                                                                                                                                     |
| [**EapPeerInitialize**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerinitialize)                             | Inicializa EAPHost para el método del mismo nivel.                                                                                                                                                                                    |
| [**EapPeerProcessRequestPacket**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerprocessrequestpacket)         | Procesa un paquete recibido por EAPHost desde un suplicante.                                                                                                                                                                   |
| [**EapPeerSetCredentials**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetcredentials)                     | Proporciona credenciales de usuario nuevas o actualizadas para el método EAP.                                                                                                                                                                 |
| [**EapPeerSetResponseAttributes**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetresponseattributes)       | Proporciona una matriz actualizada de atributos EAP para el método EAP.                                                                                                                                                              |
| [**EapPeerSetUIContext**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeersetuicontext)                         | Proporciona un contexto de la interfaz de usuario para el método EAP.                                                                                                                                                                        |
| [**EapPeerShutdown**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeershutdown)                                 | Cierra el método EAP y se prepara para descargar el archivo DLL correspondiente.                                                                                                                                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de configuración del método del mismo nivel de EAPHost](eaphost-peer-method-run-time-functions.md)
</dt> </dl>

 

 




