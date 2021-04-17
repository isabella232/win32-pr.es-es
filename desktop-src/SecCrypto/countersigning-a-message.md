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
# <a name="countersigning-a-message"></a><span data-ttu-id="29d41-103">Contrafirmar un mensaje</span><span class="sxs-lookup"><span data-stu-id="29d41-103">Countersigning a Message</span></span>

<span data-ttu-id="29d41-104">**Para contrafirmar un mensaje firmado mediante CryptMsgCountersign**</span><span class="sxs-lookup"><span data-stu-id="29d41-104">**To countersign a signed message by using CryptMsgCountersign**</span></span>

1.  <span data-ttu-id="29d41-105">Llame a [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) para obtener un identificador para el mensaje firmado.</span><span class="sxs-lookup"><span data-stu-id="29d41-105">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="29d41-106">Inicialice una estructura de [**\_ información de \_ codificación \_ del firmante CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) para el contrafirmante.</span><span class="sxs-lookup"><span data-stu-id="29d41-106">Initialize a [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure for the countersigner.</span></span>
3.  <span data-ttu-id="29d41-107">Agregue la estructura de [**\_ \_ \_ información del firmante CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a una matriz de contrafirmadores (actualmente se admite un solo contrafirmante).</span><span class="sxs-lookup"><span data-stu-id="29d41-107">Add the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure to an array of countersigners (only one countersigner is currently supported).</span></span>
4.  <span data-ttu-id="29d41-108">Llame a [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) para agregar la contrafirma o las Contrafirmas.</span><span class="sxs-lookup"><span data-stu-id="29d41-108">Call [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) to add the countersignature or countersignatures.</span></span>

<span data-ttu-id="29d41-109">Si todas las llamadas de función se realizan correctamente, el mensaje original tiene ahora una [*contrafirma*](../secgloss/c-gly.md) incluida como atributo no autenticado.</span><span class="sxs-lookup"><span data-stu-id="29d41-109">If all of the function calls succeed, the original message now has a [*countersignature*](../secgloss/c-gly.md) included as an unauthenticated attribute.</span></span>

<span data-ttu-id="29d41-110">**Para contrafirmar un mensaje firmado mediante CryptMsgCountersignEncoded**</span><span class="sxs-lookup"><span data-stu-id="29d41-110">**To countersign a signed message by using CryptMsgCountersignEncoded**</span></span>

1.  <span data-ttu-id="29d41-111">Llame a [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) para obtener un identificador para el mensaje firmado.</span><span class="sxs-lookup"><span data-stu-id="29d41-111">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="29d41-112">Llame a [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) para recuperar la información de firmante codificada del mensaje firmado.</span><span class="sxs-lookup"><span data-stu-id="29d41-112">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the encoded signer information of the signed message.</span></span>
3.  <span data-ttu-id="29d41-113">Inicialice una estructura de [**\_ información de \_ codificación \_ del firmante CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) para el contrafirmante.</span><span class="sxs-lookup"><span data-stu-id="29d41-113">Initialize a [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure for the countersigner.</span></span>
4.  <span data-ttu-id="29d41-114">Agregue la estructura de [**\_ \_ \_ información del firmante CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) a una matriz de contrafirmadores (actualmente se admite un solo contrafirmante).</span><span class="sxs-lookup"><span data-stu-id="29d41-114">Add the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure to an array of countersigners (only one countersigner is currently supported).</span></span>
5.  <span data-ttu-id="29d41-115">Llame a [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) para crear el atributo de contrafirma codificado.</span><span class="sxs-lookup"><span data-stu-id="29d41-115">Call [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) to create the encoded countersignature attribute.</span></span>
6.  <span data-ttu-id="29d41-116">Llame a [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) para agregar el atributo de contrafirma al mensaje original como atributo no autenticado.</span><span class="sxs-lookup"><span data-stu-id="29d41-116">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) to add the countersignature attribute to the original message as an unauthenticated attribute.</span></span>

<span data-ttu-id="29d41-117">Si todas las llamadas de función se realizan correctamente, se agrega un atributo de [*contrafirma*](../secgloss/c-gly.md) al mensaje original.</span><span class="sxs-lookup"><span data-stu-id="29d41-117">If all of the function calls succeed, a [*countersignature*](../secgloss/c-gly.md) attribute is added to the original message.</span></span>

 

 
