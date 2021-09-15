---
description: Explica cómo comprobar una contrasignature mediante CryptMsgVerifyCountersignatureEncoded.
ms.assetid: b7be0d4c-338f-4319-bd82-5cf3d158d6fe
title: Comprobación de una contrasignación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711e15388144fbf674cbb0c42ff41883edbb5af0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476353"
---
# <a name="verifying-a-countersignature"></a>Comprobación de una contrasignación

**Para comprobar una contrasignature**

1.  Llame [**a CryptMsgOpenToDecode para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) obtener un identificador del mensaje firmado.
2.  Obtenga un puntero al certificado del contrafirmado [**(CERT \_ INFO).**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)
3.  Llame [**a CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar la información del firmante del mensaje.
4.  Llame [**a CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar la [*contrasignature*](../secgloss/c-gly.md) del mensaje.
5.  Llame [**a CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) para comprobar la contrasignature.

Si la llamada a la función [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) se realiza correctamente, se comprueba la [*contrasignature.*](../secgloss/c-gly.md)

 

 
