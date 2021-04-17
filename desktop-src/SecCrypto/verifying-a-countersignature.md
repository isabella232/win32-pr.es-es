---
description: Explica cómo comprobar una contrafirma mediante CryptMsgVerifyCountersignatureEncoded.
ms.assetid: b7be0d4c-338f-4319-bd82-5cf3d158d6fe
title: Comprobar una contrafirma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711e15388144fbf674cbb0c42ff41883edbb5af0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687070"
---
# <a name="verifying-a-countersignature"></a>Comprobar una contrafirma

**Para comprobar una contrafirma**

1.  Llame a [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) para obtener un identificador para el mensaje firmado.
2.  Obtiene un puntero al certificado del comfirmador ( [**\_ información de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).
3.  Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar la información del firmante del mensaje.
4.  Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar la [*contrafirma*](../secgloss/c-gly.md) del mensaje.
5.  Llame a [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) para comprobar la contrafirma.

Si la llamada a la función [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) se realiza correctamente, se comprueba la [*contrafirma*](../secgloss/c-gly.md) .

 

 
