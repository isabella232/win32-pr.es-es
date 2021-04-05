---
title: Atributos (AD DS)
description: Cada objeto de Active Directory Domain Services contiene un conjunto de atributos que definen las características del objeto.
ms.assetid: 9efa7ae1-b6a9-4b95-b031-b502772c536c
ms.tgt_platform: multiple
keywords:
- AD de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56579494cdc12c2d0ad6fadbb6395d07eaec80d2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077566"
---
# <a name="attributes-ad-ds"></a>Atributos (AD DS)

Cada objeto de Active Directory Domain Services contiene un conjunto de atributos que definen las características del objeto. Cada atributo se describe mediante un objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) en el contenedor de esquemas que define el atributo. La definición del atributo incluye una variedad de datos, por ejemplo, los tipos de objetos a los que se aplica el atributo y el tipo de sintaxis del atributo. Para obtener más información acerca de las definiciones de esquema de atributo, vea [características de los atributos](characteristics-of-attributes.md).

En la lista siguiente se enumeran los tipos de atributos que se almacenan en Active Directory Domain Services.

<dl> <dt>

<span id="Domain-replicated__stored_attributes"></span><span id="domain-replicated__stored_attributes"></span><span id="DOMAIN-REPLICATED__STORED_ATTRIBUTES"></span>Atributos almacenados de dominio replicado
</dt> <dd>

Algunos atributos se almacenan en el directorio (por ejemplo, [**CN**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)y [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)) y se replican en todos los controladores de dominio de un dominio. Un subconjunto de estos atributos también se replica en el catálogo global. Si se enumeran los atributos de un objeto desde el catálogo global, solo se devuelven los atributos replicados en el catálogo global. Algunos atributos también se indizan porque al incluir una propiedad indizada en una consulta, se mejora el rendimiento de las consultas.

</dd> <dt>

<span id="Non-replicated__locally_stored_attributes"></span><span id="non-replicated__locally_stored_attributes"></span><span id="NON-REPLICATED__LOCALLY_STORED_ATTRIBUTES"></span>Atributos almacenados localmente y no replicados
</dt> <dd>

Los atributos no replicados, como [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**último inicio de sesión**](/windows/desktop/ADSchema/a-lastlogon)y [**último cierre**](/windows/desktop/ADSchema/a-lastlogoff) de sesión se almacenan en cada controlador de dominio, pero no se replican. Los atributos no replicados son atributos que pertenecen a un controlador de dominio determinado. Por ejemplo, el atributo **Last-Logon** es la última fecha y hora en que el inicio de sesión de red del usuario fue validado por el controlador de dominio concreto que devolvió la propiedad. Estos atributos se pueden recuperar de la misma manera que los atributos de todo el dominio descritos anteriormente. Sin embargo, para estos atributos, cada controlador de dominio solo almacena los valores pertenecientes a ese controlador de dominio en particular. Por ejemplo, para obtener la última vez que un usuario inició sesión en el dominio, recupere el último atributo de **Inicio de sesión** del usuario de cada controlador de dominio en el dominio y busque la última fecha y hora.

</dd> <dt>

<span id="Non-stored__constructed_attributes"></span><span id="non-stored__constructed_attributes"></span><span id="NON-STORED__CONSTRUCTED_ATTRIBUTES"></span>Atributos no almacenados y construidos
</dt> <dd>

Un objeto de usuario también ha construido atributos que no están almacenados en el directorio, pero se calculan mediante el controlador de dominio, como [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) y [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes).

</dd> </dl>

 

 