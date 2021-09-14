---
description: Asignación de certificados
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Asignación de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a9ef8822d4f191ae37cdb998166fa54c2b12d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173489"
---
# <a name="mapping-certificates"></a>Asignación de certificados

> [!Note]  
> La información de este tema solo es válida para los servidores que requieren autenticación de cliente.

 

Si una aplicación de servidor requiere autenticación de cliente, SChannel intenta asignar automáticamente el certificado que el cliente ha suministrado a una cuenta de usuario.

Una vez establecido [*el contexto*](../secgloss/s-gly.md) de seguridad, la aplicación de servidor puede usar la función [](../secgloss/c-gly.md) [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) para obtener un [*token*](../secgloss/a-gly.md) de acceso para la cuenta de usuario a la que se asignó el certificado de cliente. Además, el servidor puede usar la [**función ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) para suplantar al cliente.

Para obtener más información sobre la autenticación, vea [Realizar la autenticación mediante Schannel.](performing-authentication-using-schannel.md)

 

 
