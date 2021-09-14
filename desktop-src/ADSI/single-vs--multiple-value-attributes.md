---
title: Atributos de valor único frente a varios
description: Los atributos que pueden existir en un directorio se definen normalmente en el esquema del directorio.
ms.assetid: ea06ca66-6407-448f-8238-c8de5353663b
ms.tgt_platform: multiple
keywords:
- ADSI de atributos de valor único frente a varios
- atributos ADSI, atributos de valor único frente a varios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfabd985be3446e4f104d300d75f891ef0ce60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172129"
---
# <a name="single-vs-multiple-value-attributes"></a>Atributos de valor único frente a varios

Los atributos que pueden existir en un directorio se definen normalmente en el esquema del directorio. La definición de esquema de un atributo especifica una serie de características del atributo, como el tipo de datos y si una instancia del atributo puede tener varios valores.

Una instancia de un atributo con un solo valor puede contener un solo valor. Una instancia de un atributo de varios valores puede contener un valor único o varios valores. Active Directory no crea atributos con valores vacíos: el atributo contiene un valor válido o no existe en el objeto.

> [!Note]  
> En Active Directory y la mayoría de los demás servidores LDAP, el orden de los valores de un atributo con varios valores es indefinido. Además, cada valor de un atributo de varios valores debe ser único.

 

ADSI normalmente carga datos de esquema si el directorio admite un esquema, como Active Directory hace. Dado que ADSI conoce la sintaxis de los atributos del esquema, no es necesario especificar el tipo de atributo al acceder a él. ADSI serializa los valores de atributo al tipo de datos adecuado, tal como se define en el esquema.

Si el directorio no tiene ningún esquema, proporcione el tipo de datos al acceder a un atributo.

> [!Note]  
> Active Directory, Exchange, Windows NT 4.0 y Servidor de sitio tienen un esquema. Además, Active Directory un esquema extensible.

 

 

 




