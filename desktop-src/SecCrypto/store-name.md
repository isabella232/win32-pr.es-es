---
description: Recupera el nombre del almacén de certificados que este objeto representa.
ms.assetid: db61b464-0e8e-4b19-be12-04e00d6bba53
title: Propiedad Store.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85679bb594bdb59c41773b7f956deea95021381f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650199"
---
# <a name="storename-property"></a><span data-ttu-id="fc0a8-103">Propiedad Store.Name</span><span class="sxs-lookup"><span data-stu-id="fc0a8-103">Store.Name property</span></span>

<span data-ttu-id="fc0a8-104">\[La propiedad [**nombre**](store-location.md) está disponible para su uso en los sistemas operativos especificados en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="fc0a8-104">\[The [**Name**](store-location.md) property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fc0a8-105">En su lugar, use la [**clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="fc0a8-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="fc0a8-106">La propiedad [**Name**](store-location.md) recupera el nombre del almacén de certificados que este objeto representa.</span><span class="sxs-lookup"><span data-stu-id="fc0a8-106">The [**Name**](store-location.md) property retrieves the name of the certificate store that this object represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc0a8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc0a8-107">Syntax</span></span>


```VB
Store.Name As String
```



## <a name="property-value"></a><span data-ttu-id="fc0a8-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fc0a8-108">Property value</span></span>

<span data-ttu-id="fc0a8-109">Valor de **cadena** que representa el nombre del almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="fc0a8-109">The **String** value that represents the name of the certificate store.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc0a8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc0a8-110">Remarks</span></span>

<span data-ttu-id="fc0a8-111">Algunos ejemplos de nombres de almacenes de certificados son My y root.</span><span class="sxs-lookup"><span data-stu-id="fc0a8-111">Examples of certificate store names include My and Root.</span></span>

<span data-ttu-id="fc0a8-112">El valor de la propiedad [**Name**](store-location.md) es el mismo que el valor proporcionado para el parámetro *StoreName* del método [**Open**](store-open.md) cuando se abrió el almacén.</span><span class="sxs-lookup"><span data-stu-id="fc0a8-112">The value of the [**Name**](store-location.md) property is the same as the value supplied for the *StoreName* parameter of the [**Open**](store-open.md) method when the store was opened.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc0a8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc0a8-113">Requirements</span></span>



| <span data-ttu-id="fc0a8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc0a8-114">Requirement</span></span> | <span data-ttu-id="fc0a8-115">Value</span><span class="sxs-lookup"><span data-stu-id="fc0a8-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc0a8-116">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="fc0a8-116">Redistributable</span></span><br/> | <span data-ttu-id="fc0a8-117">CAPICOM 2,1 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="fc0a8-117">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fc0a8-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fc0a8-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="fc0a8-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc0a8-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc0a8-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc0a8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc0a8-121">**Store**</span><span class="sxs-lookup"><span data-stu-id="fc0a8-121">**Store**</span></span>](store.md)
</dt> </dl>

 

 
