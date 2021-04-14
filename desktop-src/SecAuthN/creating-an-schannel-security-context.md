---
description: Explica cómo establecer un contexto de seguridad que protege las comunicaciones entre un cliente y un servidor.
ms.assetid: eb1eadb2-14b2-4265-994a-dcea4208e650
title: Crear un contexto de seguridad de Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e364e6319fbaddb50bffaf59541af9e8f43bfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648385"
---
# <a name="creating-an-schannel-security-context"></a>Crear un contexto de seguridad de Schannel

Para establecer un [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) que protegerá las comunicaciones entre un cliente y un servidor, ambos deben participar en el siguiente proceso de intercambio de información:

## <a name="client"></a>Remoto

1.  El cliente llama a la función [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .
2.  Schannel comienza a crear un contexto de seguridad de acuerdo con las reglas del Protocolo de seguridad seleccionado. El código de retorno de la función indica si el cliente debe volver a llamar a la función. [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) puede devolver un token que representa el contexto.
3.  Si se devolvió un token, el cliente lo envía al servidor.
4.  Cuando [**InitializeSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) devuelve sec \_ E \_ OK, se realiza el cliente. Si la función devuelve los segundos \_ que \_ continúan \_ necesarios, el cliente debe esperar a que el servidor lo envíe a un token. Cuando el cliente tiene el token del servidor, debe llamar de nuevo a la [*función*](/windows/desktop/SecGloss/c-gly) **InitializeSecurityContext (general)** . (Vuelva al paso 2).

## <a name="server"></a>Servidor

1.  El servidor espera a que un cliente envíe un mensaje que contiene un token de seguridad. El servidor pasa el token recibido del cliente a la función [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) .
2.  Schannel se basa en el contexto de seguridad parcial representado por el token. Schannel devuelve un token al servidor y un código de retorno que indica si el servidor debe volver a llamar a la función.
3.  Si se devolvió un token, el servidor lo envía al cliente.
4.  Cuando [**AcceptSecurityContext (general)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) devuelve sec \_ E \_ OK, el servidor se hace. Si la función devuelve los segundos \_ que \_ continúan siendo \_ necesarios, el servidor debe esperar a que el cliente lo envíe a un token. Cuando el servidor tiene el token del cliente, debe llamar de nuevo a la función **AcceptSecurityContext (general)** . (Vuelva al paso 2).

Si alguna de las funciones devuelve un valor distinto de SEC \_ e \_ \_ \_ \_ incompletos, es necesario que se requiera, o \_ un mensaje de s e \_ incompleta \_ (vea el párrafo siguiente), se ha producido un error. El cliente y el servidor deben llamar a la función [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) para eliminar el contexto de seguridad establecido parcialmente.

Un caso especial que puede modificar el procesamiento del cliente y del servidor es cuando se envía demasiado o demasiada información al cliente o al servidor de la otra parte. En el caso de que haya poca información, ambas funciones devuelven un \_ \_ mensaje incompleto de sec \_ . Para obtener información sobre cómo reconocer y controlar la información insuficiente o excesiva, consulte [búferes adicionales devueltos por Schannel](extra-buffers-returned-by-schannel.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Realizar la autenticación mediante Schannel](performing-authentication-using-schannel.md)
</dt> <dt>

[Asignación de certificados](mapping-certificates.md)
</dt> <dt>

[Validar manualmente las credenciales de Schannel](manually-validating-schannel-credentials.md)
</dt> </dl>

 

 
