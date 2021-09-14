---
description: Para que el protocolo del proveedor de compatibilidad de seguridad de credenciales (CredSSP) delegue las credenciales, debe especificar a qué servidores se puede delegar.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: CredSSP directiva de grupo Configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a159b7a162df3eda692462a3d3972159e61797e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361873"
---
# <a name="credssp-group-policy-settings"></a>CredSSP directiva de grupo Configuración

Para que el protocolo del proveedor de compatibilidad de seguridad de [credenciales (CredSSP)](credential-security-support-provider.md) delegue las credenciales, debe especificar a qué servidores se puede delegar. Para especificar esos servidores, modifique la configuración del complemento directiva de grupo Editor de Microsoft Management Console (MMC). La configuración de GPE que controla la delegación se encuentra en Configuración del **equipo Plantillas administrativas delegación de credenciales del \| \| \| sistema**.

> [!Caution]  
> No se trata de una delegación restringida. CredSSP pasa las credenciales completa del usuario al servidor sin ninguna restricción.

 

La configuración de directiva de grupo controla la delegación de los siguientes tipos de credenciales.



| Tipo de credenciales                                                                                                                                 | Descripción                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Credenciales predeterminadas<br/> | Las credenciales obtenidas cuando el usuario inicia sesión por primera vez en Windows.<br/>                   |
| <span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Credenciales nuevas<br/>         | Credenciales que se solicitan al usuario al ejecutar una aplicación.<br/>       |
| <span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Credenciales guardadas<br/>         | Credenciales que se guardan mediante [Administrador de credenciales](credential-manager.md).<br/> |



 

Para incluir un servidor en la categoría asociada a [](/windows/desktop/SecGloss/s-gly) una configuración de directiva de grupo determinada, agregue el nombre de entidad de seguridad de servicio (SPN) de ese servidor a la lista de servidores para esa configuración de directiva de grupo. El SPN puede contener un único carácter comodín.

 

