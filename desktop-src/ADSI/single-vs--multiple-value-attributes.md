---
title: Atributos de valor único frente a varios valores
description: Los atributos que pueden existir en un directorio se definen normalmente en el esquema para el directorio.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- ADSI en comparación con los atributos de valor múltiple
- atributos ADSI, atributos de valor único frente a varios valores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfabd985be3446e4f104d300d75f891ef0ce60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075059"
---
# <a name="single-vs-multiple-value-attributes"></a>Atributos de valor único frente a varios valores

Los atributos que pueden existir en un directorio se definen normalmente en el esquema para el directorio. La definición de esquema de un atributo especifica varias características del atributo, como el tipo de datos y si una instancia del atributo puede tener varios valores.

Una instancia de un atributo de un solo valor puede contener un valor único. Una instancia de un atributo multivalor puede contener un solo valor o varios valores. Active Directory no crea atributos con valores vacíos, o bien el atributo contiene un valor válido o no existe en el objeto.

> [!Note]  
> En Active Directory y la mayoría de los demás servidores LDAP, el orden de los valores de un atributo con varios valores es indefinido. Además, cada valor de un atributo con varios valores debe ser único.

 

Normalmente, ADSI carga los datos del esquema si el directorio admite un esquema, como hace Active Directory. Dado que ADSI conoce la sintaxis de los atributos en el esquema, no es necesario especificar el tipo de atributo cuando se tiene acceso a él. ADSI calcula las referencias de los valores de atributo en el tipo de datos adecuado, tal y como se define en el esquema.

Si el directorio no tiene ningún esquema, proporcione el tipo de datos al tener acceso a un atributo.

> [!Note]  
> Active Directory, Exchange, Windows NT 4,0 y el servidor de sitio tienen un esquema. Además, Active Directory tiene un esquema extensible.

 

 

 




