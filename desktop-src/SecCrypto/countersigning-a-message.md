---
description: Explica cómo contrasignar un mensaje mediante CryptMsgCountersign.
ms.assetid: e1969b43-f50e-4c7d-a7e5-b22db4e05be2
title: Contrasignar un mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b34d93d6879135c8611e3ab50a2278506be434b25556b64c13862456a004931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876685"
---
# <a name="countersigning-a-message"></a>Contrasignar un mensaje

**Para contrafirmar un mensaje firmado mediante CryptMsgCountersign**

1.  Llame [**a CryptMsgOpenToDecode para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) obtener un identificador del mensaje firmado.
2.  Inicialice [**una estructura CMSG \_ SIGNER \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) para el contrasignador.
3.  Agregue la [**estructura CMSG \_ SIGNER \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a una matriz de contrasignadores (actualmente solo se admite un contador).
4.  Llame [**a CryptMsgCountersign para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) agregar la contrasignature o countersignatures.

Si todas las llamadas de función se realiza correctamente, el mensaje original ahora tiene una [*contrasignature*](../secgloss/c-gly.md) incluida como atributo no autenticado.

**Para contrafirmar un mensaje firmado mediante CryptMsgCountersignEncoded**

1.  Llame [**a CryptMsgOpenToDecode para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) obtener un identificador del mensaje firmado.
2.  Llame [**a CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar la información del firmante codificada del mensaje firmado.
3.  Inicialice [**una estructura CMSG \_ SIGNER \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) para el contrasignador.
4.  Agregue la [**estructura CMSG \_ SIGNER \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a una matriz de contrasignadores (actualmente solo se admite un contador).
5.  Llame [**a CryptMsgCountersignEncoded para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) crear el atributo countersignature codificado.
6.  Llame [**a CryptMsgControl para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) agregar el atributo countersignature al mensaje original como un atributo no autenticado.

Si todas las llamadas de función se realiza correctamente, se agrega un atributo [*countersignature*](../secgloss/c-gly.md) al mensaje original.

 

 
