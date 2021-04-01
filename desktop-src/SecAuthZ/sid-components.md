---
description: Componentes SID
ms.assetid: 528412e7-c2b6-4ddd-86de-999252972421
title: Componentes SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd44d0534cc56c6ef998c150810f14b3eda289d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082221"
---
# <a name="sid-components"></a>Componentes SID

Un valor de SID incluye componentes que proporcionan información sobre la estructura de [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) y los componentes que identifican de forma única a un administrador de confianza. Un SID consta de los siguientes componentes:

-   El nivel de revisión de la estructura de [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid)
-   Un valor de autoridad de identificador de 48 bits que identifica la autoridad que emitió el SID.
-   Un número variable de valores de subautoridad o de [*identificador relativo*](/windows/desktop/SecGloss/r-gly) (RID) que identifican de forma única el administrador de confianza con respecto a la autoridad que emitió el SID.

La combinación del valor de autoridad de identificador y los valores de subautor garantiza que no habrá dos SID serán el mismo, incluso si dos entidades emisoras de SID diferentes emiten la misma combinación de valores de RID. Cada autoridad emisora de SID emite un RID determinado solo una vez.

Los SID se almacenan en formato binario en una estructura de [**SID**](/windows/desktop/api/Winnt/ns-winnt-sid) . Para mostrar un SID, puede llamar a la función [**ConvertSidToStringSid**](/windows/desktop/api/Sddl/nf-sddl-convertsidtostringsida) para convertir un SID binario en formato de cadena. Para volver a convertir una cadena SID en un SID funcional válido, llame a la función [**ConvertStringSidToSid**](/windows/desktop/api/Sddl/nf-sddl-convertstringsidtosida) .

Estas funciones utilizan la siguiente notación de cadena normalizada para SID, lo que facilita la visualización de sus componentes:

s-*R* - *I* - ...

En esta notación, el carácter literal "S" identifica la serie de dígitos como un SID, *R* es el nivel de revisión, *I* es el valor de la autoridad de identificador y *S*... es uno o varios valores de subautoridad.

En el ejemplo siguiente se usa esta notación para mostrar el SID relativo al dominio conocido del grupo de administradores locales:

S-1-5-32-544

En este ejemplo, el SID tiene los siguientes componentes. Las constantes entre paréntesis son los valores conocidos de autoridad de identificador conocido y [*RID*](/windows/desktop/SecGloss/r-gly) definidos en Winnt. h:

-   Un nivel de revisión de 1
-   Un valor de autoridad de identificador de 5 (entidad de seguridad de \_ NT \_ )
-   Primer valor de subautoridad de 32 (seguridad, \_ \_ RID de dominio \_ )
-   Un segundo valor de subautoridad de 544 ( \_ administradores de RID de alias de dominio \_ \_ )

 

 
