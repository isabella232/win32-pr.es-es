---
description: Una de las ventajas de usar listas de confianza de certificados (CTL) es que se pueden diseñar aplicaciones que puedan comprobar automáticamente los mensajes firmados en certificados de confianza sin preocuparse del usuario por cuadros de diálogo.
ms.assetid: e45ea3ae-52bc-49d3-8144-f3becc254f53
title: Comprobación de mensajes firmados mediante CCL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1624a132ed976800d1c8a8ab0dcd878f533f0d0b947879e87e3e8dc21ccff51a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896236"
---
# <a name="verifying-signed-messages-by-using-ctls"></a>Comprobación de mensajes firmados mediante CCL

Una de las [](../secgloss/c-gly.md) ventajas de usar listas de confianza de certificados (CTL) es que se pueden diseñar aplicaciones que puedan comprobar automáticamente los mensajes firmados en certificados de confianza sin preocuparse del usuario por cuadros de diálogo. También proporciona a un administrador de red orígenes de control de confianza.

El siguiente procedimiento se puede usar para comprobar la firma de un mensaje firmado mediante una CTL.

**Para comprobar un mensaje firmado mediante una CTL**

1.  Descodifique el mensaje como se indica a continuación:

    1.  Obtenga un puntero al mensaje recibido (blob [*codificado).*](../secgloss/b-gly.md)
    2.  Llame [**a CryptMsgOpenToDecode y**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)pase los argumentos necesarios.
    3.  Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una vez, pasando el identificador recuperado en el paso b y un puntero a los datos que se va a descodificar. Esto hace que se tome las acciones adecuadas en el mensaje, dependiendo del tipo de mensaje.

2.  Compruebe la firma del mensaje descodificado y firmado y obtenga un puntero al CONTEXTO DE CERT del [**\_ firmante.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

    Para ello, llame a [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner)y pase el identificador de mensaje recuperado en el paso 1c como parámetro *hCryptMsg.* Si la llamada de función devuelve **TRUE**, se comprobó la firma y se devuelve un puntero al [**CONTEXTO DE PCCERT \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del firmante en el *parámetro ppSigner.*

3.  Confirme que el firmante es un origen de confianza como se muestra a continuación:

    1.  Abra el almacén de certificados que contiene la CTL adecuada.
    2.  Obtenga un puntero a [**CTL \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) mediante una llamada [**a CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).
    3.  Para confirmar que el firmante es un origen de confianza, llame a [**CertFindSubjectInCTL,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl)pasando el puntero recuperado en el paso anterior en el parámetro *pCtlContext,* CTL CERT SUBJECT TYPE en el parámetro dwSubjectType y el puntero al CONTEXTO DE CERT recuperado en el paso 2 en el \_ \_ parámetro \_ *pvSubject.* [**\_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)  Si la llamada de función devuelve **TRUE**, **el CONTEXTO DE CERT \_ pasado** a la función es un origen de confianza en la CTL.

 

 
