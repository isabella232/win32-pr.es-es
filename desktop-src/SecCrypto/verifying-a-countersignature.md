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
# <a name="verifying-a-countersignature"></a><span data-ttu-id="f5e8b-103">Comprobar una contrafirma</span><span class="sxs-lookup"><span data-stu-id="f5e8b-103">Verifying a Countersignature</span></span>

<span data-ttu-id="f5e8b-104">**Para comprobar una contrafirma**</span><span class="sxs-lookup"><span data-stu-id="f5e8b-104">**To verify a countersignature**</span></span>

1.  <span data-ttu-id="f5e8b-105">Llame a [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) para obtener un identificador para el mensaje firmado.</span><span class="sxs-lookup"><span data-stu-id="f5e8b-105">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="f5e8b-106">Obtiene un puntero al certificado del comfirmador ( [**\_ información de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).</span><span class="sxs-lookup"><span data-stu-id="f5e8b-106">Get a pointer to the countersigner's certificate ( [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info)).</span></span>
3.  <span data-ttu-id="f5e8b-107">Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar la información del firmante del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f5e8b-107">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the signer information from the message.</span></span>
4.  <span data-ttu-id="f5e8b-108">Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar la [*contrafirma*](../secgloss/c-gly.md) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="f5e8b-108">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the [*countersignature*](../secgloss/c-gly.md) from the message.</span></span>
5.  <span data-ttu-id="f5e8b-109">Llame a [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) para comprobar la contrafirma.</span><span class="sxs-lookup"><span data-stu-id="f5e8b-109">Call [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) to verify the countersignature.</span></span>

<span data-ttu-id="f5e8b-110">Si la llamada a la función [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) se realiza correctamente, se comprueba la [*contrafirma*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f5e8b-110">If the [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded) function call succeeds, the [*countersignature*](../secgloss/c-gly.md) is verified.</span></span>

 

 
