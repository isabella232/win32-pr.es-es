---
description: Establece o recupera la descripción del archivo ejecutable firmado.
ms.assetid: 39ce37bd-fe3e-4195-a132-93f3743f7370
title: SignedCode. Description (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Description
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b5783dd5e662aed33722a1c587bfcdc3cab76c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671093"
---
# <a name="signedcodedescription-property"></a><span data-ttu-id="0d2e0-103">SignedCode. Description (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0d2e0-103">SignedCode.Description property</span></span>

<span data-ttu-id="0d2e0-104">\[La propiedad **Description** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-104">\[The **Description** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0d2e0-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar el contenido con una firma digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="0d2e0-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="0d2e0-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="0d2e0-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="0d2e0-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="0d2e0-108">La propiedad **Description** establece o recupera la descripción del archivo ejecutable firmado.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-108">The **Description** property sets or retrieves the description of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d2e0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d2e0-109">Syntax</span></span>


```VB
SignedCode.Description As String
```



## <a name="property-value"></a><span data-ttu-id="0d2e0-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0d2e0-110">Property value</span></span>

<span data-ttu-id="0d2e0-111">La descripción del archivo ejecutable firmado.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-111">The description of the signed executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d2e0-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d2e0-112">Remarks</span></span>

<span data-ttu-id="0d2e0-113">La descripción es el texto que aparece en el cuadro de diálogo Comprobación de Authenticode.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-113">The description is the text that appears in the Authenticode verification dialog box.</span></span> <span data-ttu-id="0d2e0-114">El texto debe describir el archivo ejecutable firmado.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-114">The text should describe the signed executable file.</span></span> <span data-ttu-id="0d2e0-115">Si esta propiedad es **null**, el cuadro de diálogo muestra el nombre del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="0d2e0-115">If this property is **NULL**, the dialog box displays the name of the executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d2e0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d2e0-116">Requirements</span></span>



| <span data-ttu-id="0d2e0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d2e0-117">Requirement</span></span> | <span data-ttu-id="0d2e0-118">Value</span><span class="sxs-lookup"><span data-stu-id="0d2e0-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d2e0-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0d2e0-119">Redistributable</span></span><br/> | <span data-ttu-id="0d2e0-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="0d2e0-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0d2e0-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d2e0-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="0d2e0-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d2e0-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d2e0-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d2e0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d2e0-124">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="0d2e0-124">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
