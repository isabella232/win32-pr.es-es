---
title: Componentes de EAPHost
description: Obtenga información sobre los tres componentes de la autenticación eaphost. Ver recursos adicionales disponibles para usar la autenticación EAPHost.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aa86f09473b14df6dbcc8bbc667dc4a1cc1badf9e0b6dd67ac95f8d11f2bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086419"
---
# <a name="components-of-eaphost"></a>Componentes de EAPHost

En este tema se describen los tres componentes de la autenticación eaphost.

## <a name="eaphost-components"></a>Componentes de EAPHost

La autenticación eaphost tiene los tres componentes siguientes.

-   El suplicante, que realiza las solicitudes de autenticación.
-   Los métodos EAP del mismo nivel (o cliente), que implementan los métodos de EAP específicos y administran la sesión de autenticación en el lado cliente.
-   Métodos EAP de autenticador (o servidor), que implementan el lado servidor del protocolo EAP.

Las API de suplicación se llaman directamente desde una aplicación que quiere autenticarse a través de EAPHost. Sin embargo, las API del método del mismo nivel y del método autenticador son prototipos de función que se deben implementar para un tipo de método de autenticación EAP específico, como microsoft Challenge Handshake Authentication Protocol versión 2.0 (MS-CHAPv2).

Si va a crear una aplicación que usará EAPHost para la autenticación, consulte la referencia de LA API de [suplicación de EAPHost.](eap-host-supplicant-api-reference.md)

Si va a crear un nuevo método de autenticación eap para administrarlo mediante EAPHost, consulte la referencia de LA API del método del mismo nivel de [EAPHost](eap-host-peer-method-api-reference.md) y las API de método de Authenticator [EAPHost](eaphost-authenticator-method-apis.md). Tenga en cuenta que va a crear implementaciones de estas API expuestas en un nuevo archivo DLL que EAPHost carga, en lugar de llamarlas directamente.

 

 




