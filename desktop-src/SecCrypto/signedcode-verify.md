---
description: Comprueba la firma Authenticode en el código firmado.
ms.assetid: eecd692d-6b20-4644-a3d9-fba07ee667d7
title: SignedCode. verify (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ad9ad2cdbf9c8b7970f50446bba0da7a3afdcd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690957"
---
# <a name="signedcodeverify-method"></a><span data-ttu-id="70f24-103">SignedCode. verify (método)</span><span class="sxs-lookup"><span data-stu-id="70f24-103">SignedCode.Verify method</span></span>

<span data-ttu-id="70f24-104">\[El método **Verify** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="70f24-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="70f24-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar el contenido con una firma digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="70f24-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="70f24-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="70f24-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="70f24-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="70f24-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="70f24-108">El método **Verify** comprueba la firma Authenticode en el código firmado.</span><span class="sxs-lookup"><span data-stu-id="70f24-108">The **Verify** method verifies the Authenticode signature on the signed code.</span></span>

## <a name="syntax"></a><span data-ttu-id="70f24-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70f24-109">Syntax</span></span>


```VB
SignedCode.Verify( _
  [ ByVal bUIAllowed ] _
)
```



## <a name="parameters"></a><span data-ttu-id="70f24-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70f24-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70f24-111">*bUIAllowed* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="70f24-111">*bUIAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70f24-112">Valor booleano que especifica si se usa un cuadro de diálogo para comprobar la firma.</span><span class="sxs-lookup"><span data-stu-id="70f24-112">A Boolean value that specifies whether a dialog box is used to verify the signature.</span></span> <span data-ttu-id="70f24-113">Si es true, se genera un cuadro de diálogo para determinar si el código es de confianza.</span><span class="sxs-lookup"><span data-stu-id="70f24-113">If true, a dialog box is generated to determine whether the code is trusted.</span></span> <span data-ttu-id="70f24-114">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="70f24-114">The default value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70f24-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70f24-115">Return value</span></span>

<span data-ttu-id="70f24-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="70f24-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="70f24-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70f24-117">Requirements</span></span>



| <span data-ttu-id="70f24-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="70f24-118">Requirement</span></span> | <span data-ttu-id="70f24-119">Value</span><span class="sxs-lookup"><span data-stu-id="70f24-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="70f24-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="70f24-120">Redistributable</span></span><br/> | <span data-ttu-id="70f24-121">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="70f24-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="70f24-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="70f24-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="70f24-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70f24-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70f24-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="70f24-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70f24-125">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="70f24-125">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
