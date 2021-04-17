---
description: Recupera la colección de certificados del archivo ejecutable firmado.
ms.assetid: ecc05117-8b98-4e49-9671-71829df24597
title: Propiedad SignedCode. Certificates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b24a07041dae1ea2387ced93d1d2ae541a806029
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690539"
---
# <a name="signedcodecertificates-property"></a><span data-ttu-id="08a68-103">Propiedad SignedCode. Certificates</span><span class="sxs-lookup"><span data-stu-id="08a68-103">SignedCode.Certificates property</span></span>

<span data-ttu-id="08a68-104">\[La propiedad **certificados** está disponible para su uso en los sistemas operativos especificados en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="08a68-104">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="08a68-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar el contenido con una firma digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="08a68-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="08a68-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="08a68-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="08a68-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="08a68-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="08a68-108">La propiedad **Certificates** recupera la colección de certificados del archivo ejecutable firmado.</span><span class="sxs-lookup"><span data-stu-id="08a68-108">The **Certificates** property retrieves the collection of certificates in the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a68-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08a68-109">Syntax</span></span>


```VB
SignedCode.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="08a68-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="08a68-110">Property value</span></span>

<span data-ttu-id="08a68-111">Colección de [**certificados**](certificates.md) que contiene todos los certificados del archivo ejecutable firmado.</span><span class="sxs-lookup"><span data-stu-id="08a68-111">The [**Certificates**](certificates.md) collection that contains all the certificates in the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a68-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08a68-112">Requirements</span></span>



| <span data-ttu-id="08a68-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="08a68-113">Requirement</span></span> | <span data-ttu-id="08a68-114">Value</span><span class="sxs-lookup"><span data-stu-id="08a68-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08a68-115">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="08a68-115">Redistributable</span></span><br/> | <span data-ttu-id="08a68-116">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="08a68-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="08a68-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08a68-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="08a68-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08a68-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a68-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="08a68-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a68-120">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="08a68-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
