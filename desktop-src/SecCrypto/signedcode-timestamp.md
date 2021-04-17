---
description: Crea una firma de marca de tiempo Authenticode en el archivo ejecutable firmado especificado en la propiedad SignedCode. FileName.
ms.assetid: 8f4c9901-b509-4e4c-82f9-a802b0896a11
title: SignedCode. timestamp (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Timestamp
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b0f4478e4ece5188a96257a8a1dcc9722caa140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690375"
---
# <a name="signedcodetimestamp-method"></a><span data-ttu-id="41c5d-103">SignedCode. timestamp (método)</span><span class="sxs-lookup"><span data-stu-id="41c5d-103">SignedCode.Timestamp method</span></span>

<span data-ttu-id="41c5d-104">\[El método **timestamp** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="41c5d-104">\[The **Timestamp** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="41c5d-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar el contenido con una firma digital Authenticode.</span><span class="sxs-lookup"><span data-stu-id="41c5d-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="41c5d-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="41c5d-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="41c5d-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="41c5d-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="41c5d-108">El método **timestamp** crea una firma de marca de tiempo Authenticode en el archivo ejecutable firmado especificado en la propiedad **SignedCode. FileName** .</span><span class="sxs-lookup"><span data-stu-id="41c5d-108">The **Timestamp** method creates an Authenticode time stamp signature on the signed executable file specified in the **SignedCode.FileName** property.</span></span> <span data-ttu-id="41c5d-109">Esta marca de tiempo es una firma de contador en el archivo ejecutable firmado que realiza una autoridad de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="41c5d-109">This time stamp is a counter signature on the signed executable file that is performed by a time stamp authority.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c5d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41c5d-110">Syntax</span></span>


```VB
SignedCode.Timestamp( _
  ByVal URL _
)
```



## <a name="parameters"></a><span data-ttu-id="41c5d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41c5d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41c5d-112">*Dirección URL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="41c5d-112">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41c5d-113">Cadena que contiene la dirección URL del servidor de marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="41c5d-113">A string that contains the URL of the time stamp server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41c5d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41c5d-114">Return value</span></span>

<span data-ttu-id="41c5d-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="41c5d-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41c5d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41c5d-116">Remarks</span></span>

<span data-ttu-id="41c5d-117">Una marca de tiempo amplía la validez de un certificado comprobando que el archivo ejecutable se firmó en el momento en que se realizó la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="41c5d-117">A time stamp extends the validity of a certificate by verifying that the executable file was signed at the time that it was time stamped.</span></span>

<span data-ttu-id="41c5d-118">Antes de que se pueda llamar a este método, se debe especificar el archivo ejecutable firmado para marca de tiempo en la propiedad **SignedCode. FileName** y se debe llamar al método [**SignedCode. Sign**](signedcode-sign.md) para firmar el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="41c5d-118">Before this method can be called, the signed executable file to be time stamped must be specified in the **SignedCode.FileName** property, and the [**SignedCode.Sign**](signedcode-sign.md) method must be called to sign the executable file.</span></span>

<span data-ttu-id="41c5d-119">Si el archivo ejecutable firmado ya tiene una marca de tiempo, este método sobrescribe la marca de tiempo existente.</span><span class="sxs-lookup"><span data-stu-id="41c5d-119">If the signed executable file is already time stamped, this method overwrites the existing time stamp.</span></span>

## <a name="requirements"></a><span data-ttu-id="41c5d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41c5d-120">Requirements</span></span>



| <span data-ttu-id="41c5d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="41c5d-121">Requirement</span></span> | <span data-ttu-id="41c5d-122">Value</span><span class="sxs-lookup"><span data-stu-id="41c5d-122">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41c5d-123">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="41c5d-123">Redistributable</span></span><br/> | <span data-ttu-id="41c5d-124">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="41c5d-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="41c5d-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="41c5d-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="41c5d-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41c5d-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c5d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="41c5d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c5d-128">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="41c5d-128">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
