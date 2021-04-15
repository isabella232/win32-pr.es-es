---
title: Componentes de EAPHost
description: Obtenga información sobre los tres componentes de la autenticación de EAPHost. Ver recursos adicionales disponibles para usar la autenticación de EAPHost.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ede2fc6a705ec77fe982778239a92c7ffb10ef9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488294"
---
# <a name="components-of-eaphost"></a>Componentes de EAPHost

En este tema se describen los tres componentes de la autenticación de EAPHost.

## <a name="eaphost-components"></a>Componentes de EAPHost

La autenticación de EAPHost tiene los tres componentes siguientes.

-   El suplicante, que realiza las solicitudes de autenticación.
-   Los métodos EAP del mismo nivel (o cliente), que implementan los métodos EAP específicos y administran la sesión de autenticación en el lado cliente.
-   Los métodos EAP de autenticador (o servidor), que implementan el lado servidor del protocolo EAP.

Las API de suplicante se llaman directamente desde una aplicación que desea autenticarse a través de EAPHost. Sin embargo, las API del método del mismo nivel y del autenticador son prototipos de función que se deben implementar para un tipo de método de autenticación EAP específico, como la versión 2,0 del Protocolo de autenticación por desafío mutuo de Microsoft (MS-CHAPv2).

Si va a crear una aplicación que usará EAPHost para la autenticación, consulte la referencia de la [API de suplicante de EAPHost](eap-host-supplicant-api-reference.md).

Si va a crear un nuevo método de autenticación EAP para que lo administre EAPHost, consulte la [referencia de API de método del mismo nivel de EAPHost](eap-host-peer-method-api-reference.md) y las API del método de [autenticador de EAPHost](eaphost-authenticator-method-apis.md). Tenga en cuenta que creará implementaciones de estas API expuestas en un nuevo archivo DLL que EAPHost carga, en lugar de llamarlas directamente.

 

 




