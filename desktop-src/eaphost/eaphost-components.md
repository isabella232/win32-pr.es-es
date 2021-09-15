---
title: Componentes de EAPHost
description: Obtenga información sobre los tres componentes de la autenticación EAPHost. Vea recursos adicionales disponibles para usar la autenticación EAPHost.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ede2fc6a705ec77fe982778239a92c7ffb10ef9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465740"
---
# <a name="components-of-eaphost"></a>Componentes de EAPHost

En este tema se describen los tres componentes de la autenticación EAPHost.

## <a name="eaphost-components"></a>Componentes de EAPHost

La autenticación EAPHost tiene los tres componentes siguientes.

-   El suplicante, que realiza las solicitudes de autenticación.
-   Los métodos EAP del mismo nivel (o cliente), que implementan los métodos de EAP específicos y administran la sesión de autenticación en el lado cliente.
-   Métodos EAP autenticador (o servidor), que implementan el lado servidor del protocolo EAP.

Las API suplicantes se llaman directamente desde una aplicación que desea autenticarse a través de EAPHost. Sin embargo, las API del método del mismo nivel y del método autenticador son prototipos de función que se deben implementar para un tipo de método de autenticación EAP específico, como el protocolo de autenticación de protocolo de enlace de desafío de Microsoft versión 2.0 (MS-CHAPv2).

Si va a crear una aplicación que usará EAPHost para la autenticación, consulte la referencia de API de [EAPHost Supplicant](eap-host-supplicant-api-reference.md).

Si va a crear un nuevo método de autenticación de EAP para que lo administra EAPHost, consulte la referencia de API del método del mismo nivel de [EAPHost](eap-host-peer-method-api-reference.md) y las API del método Authenticator [EAPHost](eaphost-authenticator-method-apis.md). Tenga en cuenta que va a crear implementaciones de estas API expuestas en un nuevo archivo DLL que carga EAPHost, en lugar de llamarlas directamente.

 

 




