---
description: Cree una lista de certificados de confianza (CTL) firmada y guárdela en un almacén de certificados.
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: Crear, firmar y almacenar una CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da66ce5acb882d36451118700178519455a4ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686692"
---
# <a name="creating-signing-and-storing-a-ctl"></a><span data-ttu-id="0ecd7-103">Crear, firmar y almacenar una CTL</span><span class="sxs-lookup"><span data-stu-id="0ecd7-103">Creating, Signing, and Storing a CTL</span></span>

<span data-ttu-id="0ecd7-104">En los procedimientos siguientes se crea una [*lista de certificados de confianza*](../secgloss/c-gly.md) (CTL) firmada y se guarda en un almacén de [*certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0ecd7-104">The following procedures create a signed [*certificate trust list*](../secgloss/c-gly.md) (CTL) and save it to a [*certificate store*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="0ecd7-105">**Para crear y firmar una CTL**</span><span class="sxs-lookup"><span data-stu-id="0ecd7-105">**To create and sign a CTL**</span></span>

1.  <span data-ttu-id="0ecd7-106">Cree una matriz de elementos que se almacenará en la [*CTL*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0ecd7-106">Create an array of items to be stored in the [*CTL*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="0ecd7-107">En el caso de los certificados de confianza, debe ser el hash SHA1 o MD5 de los certificados de confianza.</span><span class="sxs-lookup"><span data-stu-id="0ecd7-107">In the case of trusted certificates, this must be the SHA1 or MD5 hashes of the trusted certificates.</span></span>
2.  <span data-ttu-id="0ecd7-108">Inicialice una estructura [**CTL \_ info**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) que incluya la matriz de elementos que acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="0ecd7-108">Initialize a [**CTL\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) structure that includes the array of items just created.</span></span>
3.  <span data-ttu-id="0ecd7-109">Inicializa una estructura de [**\_ \_ \_ información de codificación firmada de CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) .</span><span class="sxs-lookup"><span data-stu-id="0ecd7-109">Initialize a [**CMSG\_SIGNED\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) structure.</span></span>
4.  <span data-ttu-id="0ecd7-110">Llame a [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl).</span><span class="sxs-lookup"><span data-stu-id="0ecd7-110">Call [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl).</span></span> <span data-ttu-id="0ecd7-111">Esta llamada de función devuelve un puntero a una CTL codificada y firmada (en \# formato PKCS 7) que contiene la lista de elementos creados en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="0ecd7-111">This function call returns a pointer to a signed, encoded CTL (in PKCS \#7 format) that contains the list of items created in step 1.</span></span>

<span data-ttu-id="0ecd7-112">**Para agregar una CTL a un almacén de certificados**</span><span class="sxs-lookup"><span data-stu-id="0ecd7-112">**To add a CTL to a certificate store**</span></span>

1.  <span data-ttu-id="0ecd7-113">Obtiene un puntero a una CTL con signo y codificada.</span><span class="sxs-lookup"><span data-stu-id="0ecd7-113">Get a pointer to a signed and encoded CTL.</span></span>
2.  <span data-ttu-id="0ecd7-114">Abra el almacén de certificados de destino con una llamada a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span><span class="sxs-lookup"><span data-stu-id="0ecd7-114">Open the target certificate store with a call to [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
3.  <span data-ttu-id="0ecd7-115">Llame a [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).</span><span class="sxs-lookup"><span data-stu-id="0ecd7-115">Call [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore).</span></span>

 

 
