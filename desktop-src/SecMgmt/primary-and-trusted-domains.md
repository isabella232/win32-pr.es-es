---
description: En los siguientes términos se describen los dominios que existen en los sistemas remotos.
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: Dominios principales y de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d69a8bf5f5a8363f8de726c6183fd4de820665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540982"
---
# <a name="primary-and-trusted-domains"></a>Dominios principales y de confianza

En los siguientes términos se describen los dominios que existen en los sistemas remotos.

-   [Dominio principal](#primary-domain)
-   [Dominio de confianza](#primary-and-trusted-domains)

## <a name="primary-domain"></a>Dominio principal

Un dominio principal es el dominio responsable del establecimiento de relaciones de confianza adicionales y la realización de la autenticación (o para pasar una solicitud de autenticación a un dominio de confianza adecuado). Los controladores de dominio del controlador de dominio principal o pasan las solicitudes de autenticación que se originan en la estación de trabajo.

Cuando se produce el inicio de sesión, LSA comprueba la información de autenticación de los dominios integrados y de cuenta. Si la cuenta en la que se inicia sesión no se encuentra en ninguno de estos dominios, la solicitud de inicio de sesión se entrega en el dominio principal del sistema.

## <a name="trusted-domain"></a>Dominio de confianza

Un dominio de confianza es un dominio en el que confía el sistema local para autenticar a los usuarios. En otras palabras, si un dominio de confianza autentica a un usuario o una aplicación, esta autenticación la aceptan todos los dominios que confían en el dominio de autenticación.

Cada dominio subordinado tiene automáticamente una relación de confianza bidireccional con el dominio principal. De forma predeterminada, esta confianza es transitiva, lo que significa que si un sistema confía en el dominio A, también confía en todos los dominios en los que confía el dominio A. Las confianzas unidireccionales también se admiten en sistemas operativos anteriores a Windows 2000, que no admiten confianzas transitivas bidireccionales.

La [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) tiene un tipo de objeto, [**TrustedDomain**](the-trusteddomain-object-type.md), que se usa para almacenar información sobre las relaciones de confianza, incluido el nombre y el [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) del dominio de confianza, la cuenta del dominio que se utilizará para las solicitudes de autenticación, las solicitudes de traducción de nombres y SID y los nombres de los controladores de dominio del dominio de confianza.

En los controladores de dominio, el LSA crea una instancia de un objeto [**TrustedDomain**](the-trusteddomain-object-type.md) para cada dominio de confianza del sistema local.

Por ejemplo, si una estación de trabajo de Windows XP confía en un controlador de dominio de Windows 2000 que, a su vez, confía en otros cuatro sistemas, la estación de trabajo, conectada mediante confianza transitiva, tendrá cinco objetos [**TrustedDomain**](the-trusteddomain-object-type.md) en su sistema local.

 

 
