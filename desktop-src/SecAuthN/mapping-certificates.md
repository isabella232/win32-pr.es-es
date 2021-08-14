---
description: Asignación de certificados
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Asignación de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f671afa6278da49427d0f7b49f78895198333e24d135383207b359846216638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921844"
---
# <a name="mapping-certificates"></a>Asignación de certificados

> [!Note]  
> La información de este tema solo es válida para servidores que requieren autenticación de cliente.

 

Si una aplicación de servidor requiere autenticación de cliente, SChannel intenta asignar automáticamente el certificado que el cliente ha suministrado a una cuenta de usuario.

Una vez establecido [*el contexto*](../secgloss/s-gly.md) de seguridad, la aplicación de servidor puede usar la función [](../secgloss/c-gly.md) [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) para obtener un [*token*](../secgloss/a-gly.md) de acceso para la cuenta de usuario a la que se asignó el certificado de cliente. Además, el servidor puede usar la [**función ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) para suplantar al cliente.

Para obtener más información sobre la autenticación, vea [Realizar la autenticación mediante Schannel.](performing-authentication-using-schannel.md)

 

 
