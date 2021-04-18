---
description: Una de las ventajas de usar listas de certificados de confianza (CTL) es que se pueden diseñar aplicaciones que pueden comprobar automáticamente los mensajes firmados con respecto a los certificados de confianza sin molestar al usuario con cuadros de diálogo.
ms.assetid: e45ea3ae-52bc-49d3-8144-f3becc254f53
title: Comprobar mensajes firmados mediante CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a660bcd7e17a168b25048e61684aabc2d3ef3124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687584"
---
# <a name="verifying-signed-messages-by-using-ctls"></a>Comprobar mensajes firmados mediante CTL

Una de las ventajas de usar [*listas de certificados de confianza*](../secgloss/c-gly.md) (CTL) es que se pueden diseñar aplicaciones que pueden comprobar automáticamente los mensajes firmados con respecto a los certificados de confianza sin molestar al usuario con cuadros de diálogo. También proporciona a un administrador de red orígenes de control de confianza.

El siguiente procedimiento se puede usar para comprobar la firma de un mensaje firmado mediante una CTL.

**Para comprobar un mensaje firmado mediante una CTL**

1.  Descodifique el mensaje de la manera siguiente:

    1.  Obtiene un puntero al mensaje recibido (el [*BLOB*](../secgloss/b-gly.md)codificado).
    2.  Llame a [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), pasando los argumentos necesarios.
    3.  Llame a [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) una vez, pasando el identificador recuperado en el paso b y un puntero a los datos que se van a descodificar. Esto hace que se realicen las acciones adecuadas en el mensaje, en función del tipo de mensaje.

2.  Compruebe la firma del mensaje descodificado y firmado y obtenga un puntero al [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)del firmante.

    Esto se puede hacer llamando a [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), pasando el identificador de mensaje recuperado en el paso 1C como el parámetro *hCryptMsg* . Si la llamada a la función devuelve **true**, se comprobó la firma y se devuelve un puntero al [**\_ contexto PCCERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del firmante en el parámetro *ppSigner* .

3.  Confirme que el firmante es una fuente de confianza de la siguiente manera:

    1.  Abra el almacén de certificados que contiene la CTL adecuada.
    2.  Obtiene un puntero al [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) llamando a [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).
    3.  Para confirmar que el firmante es un origen de confianza, llame a [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl), pasando el puntero recuperado en el paso anterior en el parámetro *pCtlContext* , el \_ \_ \_ tipo de sujeto de certificado de CTL en el parámetro *dwSubjectType* y el puntero al [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) recuperado en el paso 2 en el parámetro *pvSubject* . Si la llamada de función devuelve **true**, **el \_ contexto de certificado** que se pasa a la función es un origen de confianza en la CTL.

 

 
