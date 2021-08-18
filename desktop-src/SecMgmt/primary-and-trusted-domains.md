---
description: Los términos siguientes describen los dominios que existen en sistemas remotos.
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: Dominios principales y de confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d80f1bd4983a17725de1bac9c55aae0f7d64e85bc2768bfaea2ca1469ed3d3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005073"
---
# <a name="primary-and-trusted-domains"></a>Dominios principales y de confianza

Los términos siguientes describen los dominios que existen en sistemas remotos.

-   [Dominio principal](#primary-domain)
-   [Dominio de confianza](#primary-and-trusted-domains)

## <a name="primary-domain"></a>Dominio principal

Un dominio principal es el dominio responsable de establecer relaciones de confianza y realizar la autenticación (o de pasar una solicitud de autenticación a un dominio de confianza adecuado). Los controladores de dominio del identificador de dominio principal o pasan las solicitudes de autenticación que se originan en la estación de trabajo.

Cuando se produce el inicio de sesión, el LSA comprueba la información de autenticación de los dominios integrados y de cuenta. Si la cuenta en la que se ha iniciado sesión no está en ninguno de estos dominios, la solicitud de inicio de sesión se entrega al dominio principal del sistema.

## <a name="trusted-domain"></a>Dominio de confianza

Un dominio de confianza es un dominio en el que el sistema local confía para autenticar a los usuarios. En otras palabras, si un usuario o aplicación está autenticado por un dominio de confianza, todos los dominios que confían en el dominio de autenticación aceptan esta autenticación.

Cada dominio subordinado tiene automáticamente una relación de confianza de dos vías con el dominio principal. De forma predeterminada, esta confianza es transitiva, lo que significa que si un sistema confía en el dominio A, también confía en todos los dominios en los que confía el dominio A. Las confianzas unitivas también se admiten para sistemas operativos anteriores a Windows 2000, que no admiten confianzas transitivas y dos vías.

La entidad de seguridad [*local*](/windows/desktop/SecGloss/l-gly) (LSA) tiene un tipo de [**objeto, TrustedDomain**](the-trusteddomain-object-type.md), que se usa para almacenar información sobre las relaciones de confianza, incluidos el nombre y el identificador de seguridad (SID) del dominio de confianza, la cuenta del dominio que se va a usar para las solicitudes de autenticación, las solicitudes de traducción de nombres y SID y los nombres de los controladores de dominio del dominio de confianza. [](/windows/desktop/SecGloss/s-gly)

En los controladores de dominio, el LSA crea una instancia de un [**objeto TrustedDomain**](the-trusteddomain-object-type.md) para cada dominio de confianza para el sistema local.

Por ejemplo, si una estación de trabajo de Windows XP confía en un controlador de dominio de Windows 2000 que, a su vez, confía en otros cuatro sistemas, la estación de trabajo, conectada mediante confianza transitiva, tendrá cinco objetos [**TrustedDomain**](the-trusteddomain-object-type.md) en su sistema local.

 

 
