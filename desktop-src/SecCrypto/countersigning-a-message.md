---
description: Explica cómo contrasignar un mensaje mediante CryptMsgCountersign.
ms.assetid: e1969b43-f50e-4c7d-a7e5-b22db4e05be2
title: Contrasignación de un mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02091d25e7ee22f986a26b8f07abff68ebb8c11c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259580"
---
# <a name="countersigning-a-message"></a>Contrasignación de un mensaje

**Para contrafirmar un mensaje firmado mediante CryptMsgCountersign**

1.  Llame [**a CryptMsgOpenToDecode para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) obtener un identificador del mensaje firmado.
2.  Inicialice [**una estructura CMSG \_ SIGNER \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) para el contrasignador.
3.  Agregue la [**estructura CMSG \_ SIGNER \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a una matriz de contrasignadores (actualmente solo se admite un contrasignador).
4.  Llame [**a CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) para agregar la contrasignature o countersignatures.

Si todas las llamadas de función se realiza correctamente, el mensaje original ahora tiene una [*contrasignature*](../secgloss/c-gly.md) incluida como atributo no autenticado.

**Para contrafirmar un mensaje firmado mediante CryptMsgCountersignEncoded**

1.  Llame [**a CryptMsgOpenToDecode para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) obtener un identificador del mensaje firmado.
2.  Llame [**a CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar la información del firmante codificada del mensaje firmado.
3.  Inicialice [**una estructura CMSG \_ SIGNER \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) para el contrasignador.
4.  Agregue la [**estructura CMSG \_ SIGNER \_ ENCODE \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a una matriz de contrasignadores (actualmente solo se admite un contrasignador).
5.  Llame [**a CryptMsgCountersignEncoded para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) crear el atributo countersignature codificado.
6.  Llame [**a CryptMsgControl para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) agregar el atributo countersignature al mensaje original como un atributo no autenticado.

Si todas las llamadas de función se realiza correctamente, se agrega un atributo [*countersignature*](../secgloss/c-gly.md) al mensaje original.

 

 
