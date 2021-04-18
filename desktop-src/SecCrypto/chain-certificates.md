---
description: La propiedad Certificates recupera una colección de certificados que representa los certificados de la cadena. Esta es la propiedad predeterminada.
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: 'IChain2:: Certificates (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Certificates
- IChain2.get_Certificates
- IChain.Certificates
- IChain.get_Certificates
- Chain.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a166f1d0dfa7f027058be65c3371d5c055cdb7bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670714"
---
# <a name="ichain2certificates-property"></a><span data-ttu-id="c6e40-104">IChain2:: Certificates (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c6e40-104">IChain2::Certificates property</span></span>

<span data-ttu-id="c6e40-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c6e40-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c6e40-106">En su lugar, use la [**clase X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c6e40-106">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c6e40-107">La propiedad **Certificates** recupera una colección de [**certificados**](certificates.md) que representa los certificados de la cadena.</span><span class="sxs-lookup"><span data-stu-id="c6e40-107">The **Certificates** property retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain.</span></span> <span data-ttu-id="c6e40-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c6e40-108">This is the default property.</span></span>

<span data-ttu-id="c6e40-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c6e40-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6e40-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6e40-110">Syntax</span></span>


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="c6e40-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c6e40-111">Property value</span></span>

<span data-ttu-id="c6e40-112">Colección de [**certificados**](certificates.md) que se usa para recuperar información sobre cada certificado de la cadena.</span><span class="sxs-lookup"><span data-stu-id="c6e40-112">A [**Certificates**](certificates.md) collection that is used to retrieve information about each certificate in the chain.</span></span> <span data-ttu-id="c6e40-113">El primer certificado de la colección devuelta, **Certificates. Item**(1), es el certificado final de la cadena.</span><span class="sxs-lookup"><span data-stu-id="c6e40-113">The first certificate in the returned collection, **Certificates.Item**(1), is the end certificate of the chain.</span></span> <span data-ttu-id="c6e40-114">El último certificado de la colección, Certificates **. Item**(**Certificates. Count**), es el [*certificado raíz*](../secgloss/r-gly.md) de la cadena.</span><span class="sxs-lookup"><span data-stu-id="c6e40-114">The last certificate in the collection, **Certificates.Item**(**Certificates.Count**), is the [*root certificate*](../secgloss/r-gly.md) of the chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e40-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6e40-115">Requirements</span></span>



| <span data-ttu-id="c6e40-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6e40-116">Requirement</span></span> | <span data-ttu-id="c6e40-117">Value</span><span class="sxs-lookup"><span data-stu-id="c6e40-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e40-118">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c6e40-118">End of client support</span></span><br/> | <span data-ttu-id="c6e40-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c6e40-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c6e40-120">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="c6e40-120">End of server support</span></span><br/> | <span data-ttu-id="c6e40-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6e40-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c6e40-122">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="c6e40-122">Redistributable</span></span><br/>       | <span data-ttu-id="c6e40-123">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="c6e40-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c6e40-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c6e40-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c6e40-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6e40-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
