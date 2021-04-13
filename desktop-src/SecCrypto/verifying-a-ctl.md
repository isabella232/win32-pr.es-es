---
description: Para que un interloper sea más difícil de sustituir una lista de certificados de confianza (CTL) ficticia de una existente, Compruebe la firma en la CTL cada vez que se use la CTL.
ms.assetid: 24ba6955-f6d1-4123-ab39-50385f6e03a0
title: Comprobar una CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac88362c96d5b419a7c16731e31456b569079d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543510"
---
# <a name="verifying-a-ctl"></a>Comprobar una CTL

Para que un interloper sea más difícil de sustituir una lista de [*certificados de confianza*](../secgloss/c-gly.md) (CTL) ficticia de una existente, Compruebe la firma en la CTL cada vez que se use la CTL. No use una CTL que no contenga una firma de confianza.

**Para comprobar una firma de CTL**

1.  Abra el [*almacén de certificados*](../secgloss/c-gly.md) que contiene la CTL deseada.
2.  Obtiene un identificador de un [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) para la CTL. Para ello, puede llamar a cualquiera de las funciones que devuelven un identificador **al \_ contexto CTL**, como [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).
3.  Llame a [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner), pasando [**el \_ contexto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) recuperado en el paso 2 en el parámetro *hCryptMsg* , un identificador para el almacén de certificados que contiene el certificado de la fuente de confianza para las CTL en el parámetro *rghSignerStore* y la \_ marca CMSG Trusted \_ Signer \_ en el parámetro *dwFlags* . Si la función devuelve **true**, se comprobó la firma y se devuelve un puntero al [**\_ contexto PCCERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del firmante CTL en el parámetro *ppSigner* .

 

 
