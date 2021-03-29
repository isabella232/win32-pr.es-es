---
description: Todos los protocolos de Schannel requieren que el servidor proporcione un certificado de una entidad de certificación (CA) de confianza como prueba de su identidad.
ms.assetid: 060981e0-b52a-4cc2-bfd2-4cf24f921f16
title: Realizar la autenticación mediante Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a37b8dedf07680286288234c7ca4422f44c2c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652696"
---
# <a name="performing-authentication-using-schannel"></a>Realizar la autenticación mediante Schannel

Todos los protocolos de Schannel requieren que el servidor proporcione un [*certificado*](../secgloss/c-gly.md) de una [*entidad de certificación*](../secgloss/c-gly.md) (CA) de confianza como prueba de su identidad. Este proceso se denomina autenticación de servidor. La autenticación del cliente, donde el cliente proporciona la prueba de su identidad, es opcional y puede ser solicitada por el servidor en cualquier momento.

## <a name="authenticating-the-server"></a>Autenticación del servidor

El comportamiento predeterminado de Schannel es usar la función [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) para comprobar la [*integridad*](../secgloss/i-gly.md) y la propiedad del [*certificado de servidor*](../secgloss/s-gly.md). Para deshabilitar esta característica, especifique \_ \_ \_ \_ la validación de credenciales manuales de REQ de ISC al llamar a la función [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) . Para obtener más información, vea [validar manualmente las credenciales de Schannel](manually-validating-schannel-credentials.md).

## <a name="authenticating-the-client"></a>Autenticación del cliente

Schannel no valida los certificados del cliente; el servidor debe realizar esta autenticación manualmente. Normalmente, el servidor comprobará la identidad del cliente en una base de datos que contenga información de la cuenta de usuario. Para los servidores que necesitan obtener una cuenta de cliente mediante un certificado, consulte [asignación de certificados](mapping-certificates.md).

Cuando el servidor solicita la autenticación del cliente, el cliente debe enviar al servidor uno de sus certificados. De forma predeterminada, Schannel no enviará ninguna notificación al cliente, intentará localizar un [*certificado de cliente*](../secgloss/c-gly.md) y enviarlo al servidor. Para deshabilitar esta característica, los clientes especifican \_ \_ \_ \_ las credenciales de uso de la solicitud de ISC proporcionadas al llamar a la función [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) . Cuando se especifica esta marca, Schannel devolverá \_ \_ \_ las CREDENCIALes de s incompletas al cliente cuando el servidor solicite autenticación y el cliente no haya proporcionado previamente un certificado.

 

 
