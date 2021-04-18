---
description: La propiedad FileName establece o recupera la ruta de acceso al archivo ejecutable. Esta es la propiedad predeterminada.
ms.assetid: 2d2ea87b-86db-40b4-b052-8503beafa08c
title: Propiedad SignedCode. FileName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.FileName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e6e31e57376f987b2b5cb47e5e6bd8a0d5e85fba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671785"
---
# <a name="signedcodefilename-property"></a><span data-ttu-id="89839-104">Propiedad SignedCode. FileName</span><span class="sxs-lookup"><span data-stu-id="89839-104">SignedCode.FileName property</span></span>

<span data-ttu-id="89839-105">\[La propiedad **filename** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="89839-105">\[The **FileName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="89839-106">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar el contenido con una firma digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="89839-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="89839-107">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="89839-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="89839-108">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="89839-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="89839-109">La propiedad **filename** establece o recupera la ruta de acceso al archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="89839-109">The **FileName** property sets or retrieves the path to the executable file.</span></span> <span data-ttu-id="89839-110">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="89839-110">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="89839-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89839-111">Syntax</span></span>


```VB
SignedCode.FileName As String
```



## <a name="property-value"></a><span data-ttu-id="89839-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="89839-112">Property value</span></span>

<span data-ttu-id="89839-113">Ruta de acceso al archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="89839-113">The path to the executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="89839-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89839-114">Remarks</span></span>

<span data-ttu-id="89839-115">Si se modifica el valor de la propiedad **filename** , se restablece el estado de todo el objeto [**SignedCode**](signedcode.md) .</span><span class="sxs-lookup"><span data-stu-id="89839-115">If the value of the **FileName** property is modified, the state of the entire [**SignedCode**](signedcode.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="89839-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89839-116">Requirements</span></span>



| <span data-ttu-id="89839-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="89839-117">Requirement</span></span> | <span data-ttu-id="89839-118">Value</span><span class="sxs-lookup"><span data-stu-id="89839-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89839-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="89839-119">Redistributable</span></span><br/> | <span data-ttu-id="89839-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="89839-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="89839-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="89839-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="89839-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89839-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89839-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="89839-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89839-124">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="89839-124">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
