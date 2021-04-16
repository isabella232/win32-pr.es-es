---
description: Crea una cadena de comprobación de certificados desde un certificado final al certificado raíz de confianza y devuelve un valor booleano que indica la validez global de la cadena.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: 'IChain2:: Build (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.Build
- IChain2.Build
- IChain.Build
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66ad51d94fdbd361a34e25b4b76289139abb87f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670298"
---
# <a name="ichain2build-method"></a><span data-ttu-id="40f18-103">IChain2:: Build (método)</span><span class="sxs-lookup"><span data-stu-id="40f18-103">IChain2::Build method</span></span>

<span data-ttu-id="40f18-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="40f18-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="40f18-105">En su lugar, use la [**clase X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="40f18-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="40f18-106">El método **Build** crea una cadena de comprobación de certificados desde un certificado final al [*certificado raíz*](../secgloss/r-gly.md) de confianza y devuelve un valor booleano que indica la validez global de la cadena.</span><span class="sxs-lookup"><span data-stu-id="40f18-106">The **Build** method builds a certificate verification chain from an end certificate to the trusted [*root certificate*](../secgloss/r-gly.md) and returns a Boolean value that indicates the overall validity of the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="40f18-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40f18-107">Syntax</span></span>


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="40f18-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40f18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40f18-109">*Certificado* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="40f18-109">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40f18-110">Objeto de [**certificado**](certificate.md) que representa el certificado final en el que se va a compilar la cadena de comprobación.</span><span class="sxs-lookup"><span data-stu-id="40f18-110">A [**Certificate**](certificate.md) object that represents the end certificate upon which the verification chain is to be built.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40f18-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40f18-111">Return value</span></span>

<span data-ttu-id="40f18-112">Valor booleano que indica la validez global de la cadena.</span><span class="sxs-lookup"><span data-stu-id="40f18-112">A Boolean value that indicates the overall validity of the chain.</span></span> <span data-ttu-id="40f18-113">La validez general se basa en la Directiva de comprobación de validez vigente.</span><span class="sxs-lookup"><span data-stu-id="40f18-113">Overall validity is based on the validity checking policy in place.</span></span>

## <a name="remarks"></a><span data-ttu-id="40f18-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40f18-114">Remarks</span></span>

<span data-ttu-id="40f18-115">La cadena se genera mediante la propiedad [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) , así como las directivas de aplicación y de certificado especificadas por un objeto [**CertificateStatus**](certificatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="40f18-115">The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property as well as application and certificate policies specified by a [**CertificateStatus**](certificatestatus.md) object.</span></span> <span data-ttu-id="40f18-116">La colección devuelta está ordenada; el primer certificado de la colección, Certificates **. Item**(1), es el certificado final de la cadena.</span><span class="sxs-lookup"><span data-stu-id="40f18-116">The returned collection is ordered; the first certificate in the collection, **Certificates.Item**(1), is the end certificate of the chain.</span></span> <span data-ttu-id="40f18-117">El último certificado de la colección, Certificates **. Item**(**Certificates. Count**), es el [*certificado raíz*](../secgloss/r-gly.md) de la cadena.</span><span class="sxs-lookup"><span data-stu-id="40f18-117">The last certificate in the collection, **Certificates.Item**(**Certificates.Count**), is the [*root certificate*](../secgloss/r-gly.md) of the chain.</span></span> <span data-ttu-id="40f18-118">**Certificates. Item**(0) representa la cadena completa.</span><span class="sxs-lookup"><span data-stu-id="40f18-118">**Certificates.Item**(0) represents the entire chain.</span></span>

<span data-ttu-id="40f18-119">Cada vez que se llama al método **Chain. Build** , se restablece el [*Estado*](../secgloss/s-gly.md) del objeto de [**cadena**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="40f18-119">Each time the **Chain.Build** method is called, the [*state*](../secgloss/s-gly.md) of the [**Chain**](chain.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="40f18-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40f18-120">Requirements</span></span>



| <span data-ttu-id="40f18-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="40f18-121">Requirement</span></span> | <span data-ttu-id="40f18-122">Value</span><span class="sxs-lookup"><span data-stu-id="40f18-122">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="40f18-123">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="40f18-123">End of client support</span></span><br/> | <span data-ttu-id="40f18-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40f18-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="40f18-125">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="40f18-125">End of server support</span></span><br/> | <span data-ttu-id="40f18-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40f18-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="40f18-127">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="40f18-127">Redistributable</span></span><br/>       | <span data-ttu-id="40f18-128">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="40f18-128">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="40f18-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="40f18-129">DLL</span></span><br/>                   | <dl> <span data-ttu-id="40f18-130"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40f18-130"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40f18-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="40f18-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f18-132">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="40f18-132">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="40f18-133">**IAM**</span><span class="sxs-lookup"><span data-stu-id="40f18-133">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
