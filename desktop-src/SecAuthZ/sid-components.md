---
description: Componentes de SID
ms.assetid: 528412e7-c2b6-4ddd-86de-999252972421
title: Componentes de SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9286f29015d96aef6a48726229812ad6fe73c23c59cb27aa553188cf2e9fc322
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907155"
---
# <a name="sid-components"></a>Componentes de SID

Un valor SID incluye componentes que proporcionan información sobre la [**estructura del SID**](/windows/desktop/api/Winnt/ns-winnt-sid) y los componentes que identifican de forma única a un administrador de confianza. Un SID consta de los siguientes componentes:

-   Nivel de revisión de la [**estructura de SID**](/windows/desktop/api/Winnt/ns-winnt-sid)
-   Valor de autoridad de identificador de 48 bits que identifica la autoridad que emitió el SID
-   Número variable de valores de [](/windows/desktop/SecGloss/r-gly) subautoridad o identificador relativo (RID) que identifican de forma única al administrador de confianza con respecto a la autoridad que emitió el SID.

La combinación del valor de autoridad del identificador y los valores de subautoridad garantiza que no haya dos SID iguales, incluso si dos autoridades emisoras de SID diferentes emiten la misma combinación de valores rid. Cada entidad emisora de SID emite un RID determinado solo una vez.

Los SID se almacenan en formato binario en una [**estructura SID.**](/windows/desktop/api/Winnt/ns-winnt-sid) Para mostrar un SID, puede llamar a la [**función ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) para convertir un SID binario en formato de cadena. Para volver a convertir una cadena SID en un SID funcional válido, llame a la [**función ConvertStringSidToSid.**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida)

Estas funciones usan la siguiente notación de cadena estandarizada para los SID, lo que facilita la visualización de sus componentes:

S-*R* - *I* - *S*...

En esta notación, el carácter literal "S" identifica la serie de dígitos como SID, *R* es el nivel de revisión, *I* es el valor de la entidad de identificador y *S*... es uno o varios valores de subautoridad.

En el ejemplo siguiente se usa esta notación para mostrar el SID conocido relativo al dominio del grupo de administradores local:

S-1-5-32-544

En este ejemplo, el SID tiene los siguientes componentes. Las constantes entre paréntesis son valores de [*RID*](/windows/desktop/SecGloss/r-gly) y autoridad de identificador conocidos definidos en Winnt.h:

-   Un nivel de revisión de 1
-   Un valor de identificador-autoridad de 5 (SECURITY \_ NT \_ AUTHORITY)
-   Primer valor de subautoridad de 32 (SECURITY \_ BUILTIN \_ DOMAIN \_ RID)
-   Un segundo valor de subautoridad de 544 \_ (ADMINISTRADORES DE RID DE ALIAS DE \_ \_ DOMINIO)

 

 
