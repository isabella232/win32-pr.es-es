---
description: Para que sea más difícil que un interloper sustituya una lista de confianza de certificados (CTL) por una existente, compruebe la firma en la CTL cada vez que se usa la CTL.
ms.assetid: 24ba6955-f6d1-4123-ab39-50385f6e03a0
title: Comprobación de una CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac88362c96d5b419a7c16731e31456b569079d7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170837"
---
# <a name="verifying-a-ctl"></a>Comprobación de una CTL

Para que sea más difícil que un interloper sustituya una lista de confianza de certificados [](../secgloss/c-gly.md) (CTL) por una existente, compruebe la firma en la CTL cada vez que se usa la CTL. No use una CTL que no contenga una firma de confianza.

**Para comprobar una firma CTL**

1.  Abra el [*almacén de certificados*](../secgloss/c-gly.md) que contiene la CTL deseada.
2.  Obtenga un identificador para [**un contexto de CTL \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) para la CTL. Para ello, llame a cualquiera de las funciones que devuelven un identificador a **CTL \_ CONTEXT,** como [**CertFindCTLInStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
3.  Llame a [**CryptMsgGetAndVerifySigner,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner)pasando el contexto de [**CTL \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) recuperado en el paso 2 en el parámetro *hCryptMsg,* un identificador al almacén de certificados que contiene el certificado del origen de confianza para las CTL en el parámetro *rghSignerStore* y la MARCA DE FIRMAR DE CONFIANZA de CMSG en el \_ parámetro \_ \_ *dwFlags.* Si la función devuelve **TRUE**, se comprobó la firma y se devuelve un puntero al [**contexto de PCCERT \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del firmante de CTL en el *parámetro ppSigner.*

 

 
