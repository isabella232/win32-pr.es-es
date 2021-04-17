---
description: Los protocolos admitidos y los conjuntos de cifrado se pueden enumerar mediante llamadas a CryptGetProvParam con PP \_ ENUMALGS o PP \_ ENUMALGS \_ ex.
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Enumerar protocolos admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76976da7e3ab59e299d6ef0a8e9bcabce601c0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666950"
---
# <a name="enumerating-supported-protocols"></a><span data-ttu-id="bf8d6-103">Enumerar protocolos admitidos</span><span class="sxs-lookup"><span data-stu-id="bf8d6-103">Enumerating Supported Protocols</span></span>

<span data-ttu-id="bf8d6-104">Los protocolos admitidos y los conjuntos de cifrado se pueden enumerar mediante llamadas a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con PP \_ ENUMALGS o PP \_ ENUMALGS \_ ex.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-104">Supported protocols and cipher suites can be listed by calls to [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) with PP\_ENUMALGS or PP\_ENUMALGS\_EX.</span></span> <span data-ttu-id="bf8d6-105">El valor de PP \_ ENUMALGS \_ ex funciona como PP \_ ENUMALGS, pero devuelve una estructura [**Prov \_ ENUMALGS \_ ex**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) que contiene información más amplia sobre los algoritmos admitidos por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-105">The PP\_ENUMALGS\_EX value works like PP\_ENUMALGS but returns a [**PROV\_ENUMALGS\_EX**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) structure that holds more extensive information on the algorithms supported by the provider.</span></span>

<span data-ttu-id="bf8d6-106">Para obtener más información sobre las marcas de protocolo definidas y sus valores, vea [marcas de protocolo](protocol-flags.md).</span><span class="sxs-lookup"><span data-stu-id="bf8d6-106">For more information about defined protocol flags and their values, see [Protocol Flags](protocol-flags.md).</span></span>

<span data-ttu-id="bf8d6-107">Dado que el miembro **hCryptProv** es el [*identificador*](../secgloss/h-gly.md) de un [*contexto*](../secgloss/c-gly.md) criptográfico abierto adquirido mediante [**CRYPTACQUIRECONTEXT**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) con su parámetro *dwProvType* establecido en Prov \_ RSA \_ Schannel, en el ejemplo siguiente se enumeran los nombres de todos los algoritmos disponibles en el CSP.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-107">Given that the **hCryptProv** member is the [*handle*](../secgloss/h-gly.md) of an open cryptographic [*context*](../secgloss/c-gly.md) acquired by using [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) with its *dwProvType* parameter set to PROV\_RSA\_SCHANNEL, the following example lists the names of all algorithms available in the CSP.</span></span>


```C++
PROV_ENUMALGS_EX EnumAlgs;     //   Structure to hold information on 
                               //   a supported algorithm
DWORD dFlag = CRYPT_FIRST;     //   Flag indicating that the first
                               //   supported algorithm is to be
                               //   enumerated. Changed to 0 after the
                               //   first call to the function.
cbData = sizeof(PROV_ENUMALGS_EX);

while( CryptGetProvParam(
    hCryptProv,          // handle to an open cryptographic provider
    PP_ENUMALGS_EX, 
    (BYTE *)&EnumAlgs,  // information on the next algorithm
    &cbData,            // number of bytes in the PROV_ENUMALGS_EX
    dFlag))             // flag to indicate whether this is a first or
                        // subsequent algorithm supported by the
                        // CSP.
{
    printf("Supported Algorithm name %s\n", EnumAlgs.szName);
    dFlag = CRYPT_NEXT;          // Set to CRYPT_NEXT after the first call,
} //  end of while loop. When all of the supported algorithms have
  //  been enumerated, the function returns FALSE.
```



<span data-ttu-id="bf8d6-108">En la tabla siguiente se enumeran algunos de los algoritmos devueltos por un CSP de canal de provisión de RSA interno típico \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bf8d6-108">The following table lists some algorithms returned by a typical domestic PROV\_RSA\_SCHANNEL CSP.</span></span> <span data-ttu-id="bf8d6-109">Tenga en cuenta que el CSP no admite ni SSL2 SHA Mac ni cifrado DES SSL2 en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-109">Notice that neither SSL2 SHA MACs nor SSL2 DES encryption is supported by the CSP in this example.</span></span>



| <span data-ttu-id="bf8d6-110">Identificador de algoritmo</span><span class="sxs-lookup"><span data-stu-id="bf8d6-110">Algorithm identifier</span></span>                                                                        | <span data-ttu-id="bf8d6-111">Longitud de clave mínima</span><span class="sxs-lookup"><span data-stu-id="bf8d6-111">Minimum key length</span></span> | <span data-ttu-id="bf8d6-112">Longitud máxima de la clave</span><span class="sxs-lookup"><span data-stu-id="bf8d6-112">Maximum key length</span></span> | <span data-ttu-id="bf8d6-113">Protocolos</span><span class="sxs-lookup"><span data-stu-id="bf8d6-113">Protocols</span></span> | <span data-ttu-id="bf8d6-114">Nombre del algoritmo</span><span class="sxs-lookup"><span data-stu-id="bf8d6-114">Algorithm name</span></span> |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [<span data-ttu-id="bf8d6-115">*CALG \_ RSA \_ KEYX*</span><span class="sxs-lookup"><span data-stu-id="bf8d6-115">*CALG\_RSA\_KEYX*</span></span>](../secgloss/c-gly.md) | <span data-ttu-id="bf8d6-116">512</span><span class="sxs-lookup"><span data-stu-id="bf8d6-116">512</span></span>                | <span data-ttu-id="bf8d6-117">2048</span><span class="sxs-lookup"><span data-stu-id="bf8d6-117">2048</span></span>               | <span data-ttu-id="bf8d6-118">0x0007</span><span class="sxs-lookup"><span data-stu-id="bf8d6-118">0x0007</span></span>    | <span data-ttu-id="bf8d6-119">"RSA \_ KEYX"</span><span class="sxs-lookup"><span data-stu-id="bf8d6-119">"RSA\_KEYX"</span></span>    |
| [<span data-ttu-id="bf8d6-120">*CALG \_ MD5*</span><span class="sxs-lookup"><span data-stu-id="bf8d6-120">*CALG\_MD5*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="bf8d6-121">128</span><span class="sxs-lookup"><span data-stu-id="bf8d6-121">128</span></span>                | <span data-ttu-id="bf8d6-122">128</span><span class="sxs-lookup"><span data-stu-id="bf8d6-122">128</span></span>                | <span data-ttu-id="bf8d6-123">0x0007</span><span class="sxs-lookup"><span data-stu-id="bf8d6-123">0x0007</span></span>    | <span data-ttu-id="bf8d6-124">MD5</span><span class="sxs-lookup"><span data-stu-id="bf8d6-124">"MD5"</span></span>          |
| [<span data-ttu-id="bf8d6-125">*CALG \_ Sha*</span><span class="sxs-lookup"><span data-stu-id="bf8d6-125">*CALG\_SHA*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="bf8d6-126">160</span><span class="sxs-lookup"><span data-stu-id="bf8d6-126">160</span></span>                | <span data-ttu-id="bf8d6-127">160</span><span class="sxs-lookup"><span data-stu-id="bf8d6-127">160</span></span>                | <span data-ttu-id="bf8d6-128">0x0005</span><span class="sxs-lookup"><span data-stu-id="bf8d6-128">0x0005</span></span>    | <span data-ttu-id="bf8d6-129">Sha</span><span class="sxs-lookup"><span data-stu-id="bf8d6-129">"SHA"</span></span>          |
| [<span data-ttu-id="bf8d6-130">*CALG \_ RC4*</span><span class="sxs-lookup"><span data-stu-id="bf8d6-130">*CALG\_RC4*</span></span>](../secgloss/c-gly.md)                 | <span data-ttu-id="bf8d6-131">40</span><span class="sxs-lookup"><span data-stu-id="bf8d6-131">40</span></span>                 | <span data-ttu-id="bf8d6-132">128</span><span class="sxs-lookup"><span data-stu-id="bf8d6-132">128</span></span>                | <span data-ttu-id="bf8d6-133">0x0007</span><span class="sxs-lookup"><span data-stu-id="bf8d6-133">0x0007</span></span>    | <span data-ttu-id="bf8d6-134">RC4</span><span class="sxs-lookup"><span data-stu-id="bf8d6-134">"RC4"</span></span>          |
| <span data-ttu-id="bf8d6-135">CALG \_ des</span><span class="sxs-lookup"><span data-stu-id="bf8d6-135">CALG\_DES</span></span>                                                                                   | <span data-ttu-id="bf8d6-136">56</span><span class="sxs-lookup"><span data-stu-id="bf8d6-136">56</span></span>                 | <span data-ttu-id="bf8d6-137">56</span><span class="sxs-lookup"><span data-stu-id="bf8d6-137">56</span></span>                 | <span data-ttu-id="bf8d6-138">0x0005</span><span class="sxs-lookup"><span data-stu-id="bf8d6-138">0x0005</span></span>    | <span data-ttu-id="bf8d6-139">DES</span><span class="sxs-lookup"><span data-stu-id="bf8d6-139">"DES"</span></span>          |



 

<span data-ttu-id="bf8d6-140">Para prepararse para enviar mensajes ClientHello o ServerHello, el motor de protocolo [*Schannel*](../secgloss/s-gly.md) enumera los algoritmos y los tamaños de clave admitidos por el CSP y crea una lista internamente de los conjuntos de cifrado admitidos.</span><span class="sxs-lookup"><span data-stu-id="bf8d6-140">To prepare to send ClientHello or ServerHello messages, the [*Schannel*](../secgloss/s-gly.md) protocol engine enumerates the algorithms and key sizes supported by the CSP and builds a list internally of supported cipher suites.</span></span>

 

 
