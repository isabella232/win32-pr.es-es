---
description: Devuelve una cadena que contiene información de error adicional sobre la entrada indizada.
ms.assetid: 4f0d5289-c414-4e2b-b612-be8ce1d98b12
title: 'IChain2:: ExtendedErrorInfo (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ExtendedErrorInfo
- IChain2.ExtendedErrorInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f8a7840d0f54ea7e93ad9998d5e8772a2ae411f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690560"
---
# <a name="ichain2extendederrorinfo-method"></a><span data-ttu-id="3c607-103">IChain2:: ExtendedErrorInfo (método)</span><span class="sxs-lookup"><span data-stu-id="3c607-103">IChain2::ExtendedErrorInfo method</span></span>

<span data-ttu-id="3c607-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3c607-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3c607-105">En su lugar, use la [**clase X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="3c607-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3c607-106">El método **ExtendedErrorInfo** devuelve una cadena que contiene información de error adicional sobre la entrada indizada.</span><span class="sxs-lookup"><span data-stu-id="3c607-106">The **ExtendedErrorInfo** method returns a string that contains additional error information about the indexed entry.</span></span>

<span data-ttu-id="3c607-107">Este método se presenta en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="3c607-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c607-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3c607-108">Syntax</span></span>


```VB
Chain.ExtendedErrorInfo( _
  [ ByVal Index ] _
)
```



## <a name="parameters"></a><span data-ttu-id="3c607-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3c607-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c607-110">*Índice* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3c607-110">*Index* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3c607-111">Un **valor de tipo Long** que representa el índice de la entrada.</span><span class="sxs-lookup"><span data-stu-id="3c607-111">A **Long** representing the index of the entry.</span></span> <span data-ttu-id="3c607-112">El valor predeterminado es 1, que devuelve información de error para el certificado final de la cadena.</span><span class="sxs-lookup"><span data-stu-id="3c607-112">The default value is 1, which returns error information for the end certificate in the chain.</span></span> <span data-ttu-id="3c607-113">Certificates **. Count** devuelve información sobre el certificado raíz de la cadena.</span><span class="sxs-lookup"><span data-stu-id="3c607-113">**Certificates.Count** returns information about the root certificate of the chain.</span></span> <span data-ttu-id="3c607-114">0 devuelve información de error extendida para toda la cadena.</span><span class="sxs-lookup"><span data-stu-id="3c607-114">0 returns extended error information for the entire chain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c607-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3c607-115">Return value</span></span>

<span data-ttu-id="3c607-116">Cadena que contiene la información de error extendida.</span><span class="sxs-lookup"><span data-stu-id="3c607-116">A string that contains the extended error information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c607-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c607-117">Requirements</span></span>



| <span data-ttu-id="3c607-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c607-118">Requirement</span></span> | <span data-ttu-id="3c607-119">Value</span><span class="sxs-lookup"><span data-stu-id="3c607-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c607-120">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="3c607-120">End of client support</span></span><br/> | <span data-ttu-id="3c607-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c607-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3c607-122">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="3c607-122">End of server support</span></span><br/> | <span data-ttu-id="3c607-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c607-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3c607-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3c607-124">Redistributable</span></span><br/>       | <span data-ttu-id="3c607-125">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="3c607-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3c607-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3c607-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3c607-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c607-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c607-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c607-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c607-129">**IAM**</span><span class="sxs-lookup"><span data-stu-id="3c607-129">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
