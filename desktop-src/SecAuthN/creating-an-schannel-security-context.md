---
description: Explica cómo establecer un contexto de seguridad que proteja las comunicaciones entre un cliente y un servidor.
ms.assetid: eb1eadb2-14b2-4265-994a-dcea4208e650
title: Creación de un contexto de seguridad de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7373d2ed4f8cc385a2245e6971f8233aad052930d4995225abfda8eab0191aaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008863"
---
# <a name="creating-an-schannel-security-context"></a>Creación de un contexto de seguridad de Schannel

Para establecer un [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) que proteja las comunicaciones entre un cliente y un servidor, ambos deben participar en el siguiente proceso de intercambio de información:

## <a name="client"></a>Cliente

1.  El cliente llama a [**la función InitializeSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
2.  Schannel comienza a crear un contexto de seguridad según las reglas del protocolo de seguridad seleccionado. El código de retorno de la función indica si el cliente debe volver a llamar a la función. [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) puede devolver un token que representa el contexto.
3.  Si se devolvió un token, el cliente lo envía al servidor.
4.  Cuando [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) devuelve SEC \_ E \_ OK, el cliente está listo. Si la función devuelve SEC I CONTINUE NEEDED, el cliente debe esperar a \_ que el servidor le envíe un \_ \_ token. Cuando el cliente tiene el token del servidor, debe llamar de nuevo a **la función InitializeSecurityContext (General).** [](/windows/desktop/SecGloss/c-gly) (Vuelva al paso 2).

## <a name="server"></a>Servidor

1.  El servidor espera a que un cliente envíe un mensaje que contiene un token de seguridad. El servidor pasa el token recibido del cliente a la [**función AcceptSecurityContext (General).**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)
2.  Schannel se basa en el contexto de seguridad parcial representado por el token. Schannel devuelve un token al servidor y un código de retorno que indica si el servidor debe volver a llamar a la función.
3.  Si se devolvió un token, el servidor lo envía al cliente.
4.  Cuando [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) devuelve SEC \_ E \_ OK, el servidor se realiza. Si la función devuelve SEC I CONTINUE NEEDED, el servidor debe esperar a \_ que el cliente le envíe un \_ \_ token. Cuando el servidor tiene el token del cliente, debe llamar de nuevo a **la función AcceptSecurityContext (General).** (Vuelva al paso 2).

Si alguna de las funciones devuelve un valor distinto de SEC E OK, SEC I CONTINUE NEEDED o \_ SEC E INCOMPLETE MESSAGE \_ \_ \_ \_ \_ \_ \_ (vea el párrafo siguiente), se ha producido un error. El cliente y el servidor deben llamar a [**la función DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) para eliminar el contexto de seguridad establecido parcialmente.

Un caso especial que puede modificar el procesamiento de cliente y servidor es cuando se envía demasiada información al cliente o servidor desde la otra parte. En el caso de poca información, ambas funciones devuelven SEC \_ E \_ INCOMPLETE \_ MESSAGE. Para obtener información sobre cómo reconocer y controlar información insuficiente o excesiva, vea Búferes adicionales [devueltos por Schannel.](extra-buffers-returned-by-schannel.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Realizar la autenticación mediante Schannel](performing-authentication-using-schannel.md)
</dt> <dt>

[Asignación de certificados](mapping-certificates.md)
</dt> <dt>

[Validación manual de credenciales de Schannel](manually-validating-schannel-credentials.md)
</dt> </dl>

 

 
