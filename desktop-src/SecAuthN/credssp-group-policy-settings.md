---
description: Para que el protocolo de proveedor de compatibilidad para seguridad de credenciales (CredSSP) delegue las credenciales, debe especificar a qué servidores se puede delegar.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: Configuración de directiva de grupo CredSSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a159b7a162df3eda692462a3d3972159e61797e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652769"
---
# <a name="credssp-group-policy-settings"></a>Configuración de directiva de grupo CredSSP

Para que el [Protocolo de proveedor de compatibilidad para seguridad de credenciales (CredSSP)](credential-security-support-provider.md) delegue las credenciales, debe especificar a qué servidores se puede delegar. Para especificar esos servidores, modifique la configuración en el complemento Microsoft Management Console (MMC) del editor de directiva de grupo (GPE). La configuración de GPE que controla la delegación se encuentran en **configuración \| del equipo Plantillas administrativas \| delegación de \| credenciales del sistema**.

> [!Caution]  
> Esta no es una delegación restringida. CredSSP pasa las credenciales completas del usuario al servidor sin ninguna restricción.

 

La configuración de directiva de grupo controla la delegación de los siguientes tipos de credenciales.



| Tipo de credenciales                                                                                                                                 | Descripción                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Credenciales predeterminadas<br/> | Las credenciales obtenidas cuando el usuario inicia sesión por primera vez en Windows.<br/>                   |
| <span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Nuevas credenciales<br/>         | Las credenciales que se solicita al usuario al ejecutar una aplicación.<br/>       |
| <span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Credenciales guardadas<br/>         | Las credenciales que se guardan con el [Administrador de credenciales](credential-manager.md).<br/> |



 

Para incluir un servidor en la categoría asociado a una configuración de directiva de grupo determinada, agregue el [*nombre de entidad*](/windows/desktop/SecGloss/s-gly) de seguridad de servicio (SPN) de ese servidor a la lista de servidores de esa configuración de directiva de grupo. El SPN puede contener un solo carácter comodín.

 

