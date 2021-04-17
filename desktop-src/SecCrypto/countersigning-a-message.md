---
description: Explica cómo contrafirmar un mensaje mediante CryptMsgCountersign.
ms.assetid: e1969b43-f50e-4c7d-a7e5-b22db4e05be2
title: Contrafirmar un mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02091d25e7ee22f986a26b8f07abff68ebb8c11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667718"
---
# <a name="countersigning-a-message"></a>Contrafirmar un mensaje

**Para contrafirmar un mensaje firmado mediante CryptMsgCountersign**

1.  Llame a [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) para obtener un identificador para el mensaje firmado.
2.  Inicialice una estructura de [**\_ información de \_ codificación \_ del firmante CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) para el contrafirmante.
3.  Agregue la estructura de [**\_ \_ \_ información del firmante CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a una matriz de contrafirmadores (actualmente se admite un solo contrafirmante).
4.  Llame a [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) para agregar la contrafirma o las Contrafirmas.

Si todas las llamadas de función se realizan correctamente, el mensaje original tiene ahora una [*contrafirma*](../secgloss/c-gly.md) incluida como atributo no autenticado.

**Para contrafirmar un mensaje firmado mediante CryptMsgCountersignEncoded**

1.  Llame a [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) para obtener un identificador para el mensaje firmado.
2.  Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar la información de firmante codificada del mensaje firmado.
3.  Inicialice una estructura de [**\_ información de \_ codificación \_ del firmante CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) para el contrafirmante.
4.  Agregue la estructura de [**\_ \_ \_ información del firmante CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a una matriz de contrafirmadores (actualmente se admite un solo contrafirmante).
5.  Llame a [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) para crear el atributo de contrafirma codificado.
6.  Llame a [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) para agregar el atributo de contrafirma al mensaje original como atributo no autenticado.

Si todas las llamadas de función se realizan correctamente, se agrega un atributo de [*contrafirma*](../secgloss/c-gly.md) al mensaje original.

 

 
