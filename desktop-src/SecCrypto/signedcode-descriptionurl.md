---
description: Establece o recupera la dirección URL de una descripción del archivo ejecutable firmado.
ms.assetid: 854c76fb-5cb3-4200-bab0-fa3fa5bd3abe
title: Propiedad SignedCode. DescriptionURL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.DescriptionURL
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 628d176595031f2b87b9fcb5f58ff81838d49be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690093"
---
# <a name="signedcodedescriptionurl-property"></a><span data-ttu-id="65630-103">Propiedad SignedCode. DescriptionURL</span><span class="sxs-lookup"><span data-stu-id="65630-103">SignedCode.DescriptionURL property</span></span>

<span data-ttu-id="65630-104">\[La propiedad **DescriptionURL** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="65630-104">\[The **DescriptionURL** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="65630-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar el contenido con una firma digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="65630-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="65630-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="65630-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="65630-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="65630-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="65630-108">La propiedad **DescriptionURL** establece o recupera la dirección URL de una descripción del archivo ejecutable firmado.</span><span class="sxs-lookup"><span data-stu-id="65630-108">The **DescriptionURL** property sets or retrieves the URL of a description of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="65630-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65630-109">Syntax</span></span>


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a><span data-ttu-id="65630-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="65630-110">Property value</span></span>

<span data-ttu-id="65630-111">Dirección URL de una descripción del archivo ejecutable firmado.</span><span class="sxs-lookup"><span data-stu-id="65630-111">The URL of a description of the signed executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="65630-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65630-112">Remarks</span></span>

<span data-ttu-id="65630-113">**DescriptionURL** es la dirección URL a la que se vincula la [**Descripción**](signedcode-description.md) que aparece en el cuadro de diálogo de comprobación de Authenticode.</span><span class="sxs-lookup"><span data-stu-id="65630-113">The **DescriptionURL** is the URL to which the [**Description**](signedcode-description.md) that appears in the Authenticode verification dialog box links.</span></span> <span data-ttu-id="65630-114">Si esta propiedad es **null**, la **Descripción** no funciona como un vínculo.</span><span class="sxs-lookup"><span data-stu-id="65630-114">If this property is **NULL**, the **Description** does not function as a link.</span></span>

## <a name="requirements"></a><span data-ttu-id="65630-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65630-115">Requirements</span></span>



| <span data-ttu-id="65630-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="65630-116">Requirement</span></span> | <span data-ttu-id="65630-117">Value</span><span class="sxs-lookup"><span data-stu-id="65630-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65630-118">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="65630-118">Redistributable</span></span><br/> | <span data-ttu-id="65630-119">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="65630-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="65630-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65630-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="65630-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65630-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65630-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="65630-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65630-123">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="65630-123">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
