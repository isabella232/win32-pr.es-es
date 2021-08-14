---
description: Todos los protocolos Schannel requieren que el servidor proporcione un certificado de una entidad de certificación (CA) de confianza como prueba de su identidad.
ms.assetid: 060981e0-b52a-4cc2-bfd2-4cf24f921f16
title: Realizar la autenticación mediante Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c2a5099dd29d6b3b342b583e37e2dc98187f5011c7cc75b75432924fba9ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921024"
---
# <a name="performing-authentication-using-schannel"></a>Realizar la autenticación mediante Schannel

Todos los protocolos Schannel requieren que el servidor proporcione [*un*](../secgloss/c-gly.md) certificado de una entidad de [*certificación*](../secgloss/c-gly.md) (CA) de confianza como prueba de su identidad. Este proceso se denomina autenticación de servidor. La autenticación de cliente, donde el cliente proporciona una prueba de su identidad, es opcional y el servidor puede solicitarla en cualquier momento.

## <a name="authenticating-the-server"></a>Autenticación del servidor

El comportamiento predeterminado de Schannel es usar la [**función WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) para comprobar la integridad [*y*](../secgloss/i-gly.md) propiedad del certificado de [*servidor*](../secgloss/s-gly.md). Para deshabilitar esta característica, especifique ISC \_ REQ MANUAL CRED VALIDATION al llamar a \_ la función \_ \_ [**InitializeSecurityContext (Schannel).**](./initializesecuritycontext--schannel.md) Para obtener más información, [vea Validación manual de credenciales de Schannel.](manually-validating-schannel-credentials.md)

## <a name="authenticating-the-client"></a>Autenticación del cliente

Schannel no valida los certificados del cliente; el servidor debe realizar esta autenticación manualmente. Normalmente, el servidor comprobará la identidad del cliente en una base de datos que contiene información de la cuenta de usuario. Para los servidores que necesitan obtener la cuenta de un cliente mediante un certificado, vea [Asignación de certificados](mapping-certificates.md).

Cuando el servidor solicita la autenticación de cliente, el cliente debe enviar al servidor uno de sus certificados. De forma predeterminada, Schannel intentará, sin notificación al cliente, buscar un certificado [*de*](../secgloss/c-gly.md) cliente y enviarlo al servidor. Para deshabilitar esta característica, los clientes especifican ISC REQ USE SUPPLIED CREDS al llamar a \_ \_ la función \_ \_ [**InitializeSecurityContext (Schannel).**](./initializesecuritycontext--schannel.md) Cuando se especifica esta marca, Schannel devolverá LAS CREDENCIALES INCOMPLETAS DE SEC I al cliente cuando el servidor solicite la autenticación y el cliente no haya proporcionado \_ \_ \_ previamente un certificado.

 

 
