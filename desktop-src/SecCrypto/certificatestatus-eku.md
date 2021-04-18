---
description: Devuelve el objeto EKU utilizado para generar el objeto de cadena.
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: CertificateStatus. EKU, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d386251c6d7f674d3850de275559bcb87ea6d61e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670432"
---
# <a name="certificatestatuseku-method"></a><span data-ttu-id="91a5d-103">CertificateStatus. EKU, método</span><span class="sxs-lookup"><span data-stu-id="91a5d-103">CertificateStatus.EKU method</span></span>

<span data-ttu-id="91a5d-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="91a5d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="91a5d-105">En su lugar, use la [**estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="91a5d-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="91a5d-106">El método **EKU** devuelve el objeto [**EKU**](eku.md) usado para generar el objeto de [**cadena**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="91a5d-106">The **EKU** method returns the [**EKU**](eku.md) object used to build the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="91a5d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91a5d-107">Syntax</span></span>


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a><span data-ttu-id="91a5d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91a5d-108">Parameters</span></span>

<span data-ttu-id="91a5d-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="91a5d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="91a5d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91a5d-110">Return value</span></span>

<span data-ttu-id="91a5d-111">Este método devuelve un objeto [**EKU**](eku.md) que indica la configuración de uso mejorado de clave del [*certificado*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="91a5d-111">This method returns an [**EKU**](eku.md) object that indicates the extended key usage setting of the [*certificate*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="91a5d-112">La configuración de EKU establece el uso válido de un certificado.</span><span class="sxs-lookup"><span data-stu-id="91a5d-112">The EKU setting establishes a certificate's valid use.</span></span> <span data-ttu-id="91a5d-113">Solo se puede establecer un objeto **EKU** para cada certificado.</span><span class="sxs-lookup"><span data-stu-id="91a5d-113">Only a single **EKU** object can be set for each certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="91a5d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91a5d-114">Remarks</span></span>

<span data-ttu-id="91a5d-115">El método [**CertificateStatus. ApplicationPolicies**](certificatestatus-applicationpolicies.md) proporciona la misma funcionalidad que este método, pero permite especificar muchas configuraciones en lugar de solo una.</span><span class="sxs-lookup"><span data-stu-id="91a5d-115">The [**CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md) method provides the same functionality as this method but allows many settings to be specified instead of only one.</span></span> <span data-ttu-id="91a5d-116">Si la colección [**OID**](oids.md) devuelta por el método **ApplicationPolicies** contiene uno o más objetos [**OID**](oid.md) , se omite el objeto [**EKU**](eku.md) devuelto por este método.</span><span class="sxs-lookup"><span data-stu-id="91a5d-116">If the [**OIDs**](oids.md) collection returned by the **ApplicationPolicies** method contains one or more [**OID**](oid.md) objects, the [**EKU**](eku.md) object returned by this method is ignored.</span></span> <span data-ttu-id="91a5d-117">Use el método **ApplicationPolicies** en lugar de este método.</span><span class="sxs-lookup"><span data-stu-id="91a5d-117">Use the **ApplicationPolicies** method instead of this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="91a5d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91a5d-118">Requirements</span></span>



| <span data-ttu-id="91a5d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="91a5d-119">Requirement</span></span> | <span data-ttu-id="91a5d-120">Value</span><span class="sxs-lookup"><span data-stu-id="91a5d-120">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91a5d-121">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="91a5d-121">End of client support</span></span><br/> | <span data-ttu-id="91a5d-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91a5d-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="91a5d-123">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="91a5d-123">End of server support</span></span><br/> | <span data-ttu-id="91a5d-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91a5d-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="91a5d-125">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="91a5d-125">Redistributable</span></span><br/>       | <span data-ttu-id="91a5d-126">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="91a5d-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="91a5d-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="91a5d-127">DLL</span></span><br/>                   | <dl> <span data-ttu-id="91a5d-128"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91a5d-128"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91a5d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="91a5d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91a5d-130">**CertificateStatus**</span><span class="sxs-lookup"><span data-stu-id="91a5d-130">**CertificateStatus**</span></span>](certificatestatus.md)
</dt> <dt>

[<span data-ttu-id="91a5d-131">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="91a5d-131">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="91a5d-132">**EKU**</span><span class="sxs-lookup"><span data-stu-id="91a5d-132">**EKU**</span></span>](eku.md)
</dt> </dl>

 

 
