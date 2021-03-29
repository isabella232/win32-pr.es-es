---
description: Asignación de certificados
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Asignación de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a9ef8822d4f191ae37cdb998166fa54c2b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816035"
---
# <a name="mapping-certificates"></a>Asignación de certificados

> [!Note]  
> La información de este tema solo es válida para los servidores que requieren autenticación del cliente.

 

Si una aplicación de servidor requiere autenticación de cliente, SChannel intenta asignar automáticamente el certificado que el cliente ha suministrado a una cuenta de usuario.

Una vez establecido el [*contexto de seguridad*](../secgloss/s-gly.md) , la aplicación de servidor puede usar la función [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) para obtener un [*token de acceso*](../secgloss/a-gly.md) para la cuenta de usuario a la que se asignó el certificado de [*cliente*](../secgloss/c-gly.md) . Además, el servidor puede usar la función [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) para suplantar al cliente.

Para obtener más información sobre la autenticación, vea [realizar la autenticación con Schannel](performing-authentication-using-schannel.md).

 

 
