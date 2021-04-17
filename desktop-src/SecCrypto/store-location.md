---
description: Recupera la ubicación del almacén de certificados que este objeto representa.
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Store. Location (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Location
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42afe40dffde5a0375928d355508ec75a4076f17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650175"
---
# <a name="storelocation-property"></a><span data-ttu-id="8da4d-103">Store. Location (propiedad)</span><span class="sxs-lookup"><span data-stu-id="8da4d-103">Store.Location property</span></span>

<span data-ttu-id="8da4d-104">\[La propiedad **Ubicación** está disponible para su uso en los sistemas operativos especificados en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="8da4d-104">\[The **Location** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8da4d-105">En su lugar, use la [**clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="8da4d-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="8da4d-106">La propiedad **Location** recupera la ubicación del almacén de certificados que este objeto representa.</span><span class="sxs-lookup"><span data-stu-id="8da4d-106">The **Location** property retrieves the location of the certificate store that this object represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="8da4d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8da4d-107">Syntax</span></span>


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="8da4d-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8da4d-108">Property value</span></span>

<span data-ttu-id="8da4d-109">Valor [**de \_ \_ Ubicación del almacén de CAPICOM**](capicom-store-location.md) que representa la ubicación del almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="8da4d-109">The [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) value that represents the location of the certificate store.</span></span>

## <a name="remarks"></a><span data-ttu-id="8da4d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8da4d-110">Remarks</span></span>

<span data-ttu-id="8da4d-111">El valor de la propiedad **Location** es el mismo que el valor proporcionado para el parámetro *StoreLocation* del método [**Open**](store-open.md) cuando se abre el almacén.</span><span class="sxs-lookup"><span data-stu-id="8da4d-111">The value of the **Location** property is the same as the value supplied for the *StoreLocation* parameter of the [**Open**](store-open.md) method when the store was opened.</span></span>

## <a name="requirements"></a><span data-ttu-id="8da4d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8da4d-112">Requirements</span></span>



| <span data-ttu-id="8da4d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8da4d-113">Requirement</span></span> | <span data-ttu-id="8da4d-114">Value</span><span class="sxs-lookup"><span data-stu-id="8da4d-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8da4d-115">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="8da4d-115">Redistributable</span></span><br/> | <span data-ttu-id="8da4d-116">CAPICOM 2,1 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="8da4d-116">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8da4d-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8da4d-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="8da4d-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8da4d-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8da4d-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="8da4d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da4d-120">**Store**</span><span class="sxs-lookup"><span data-stu-id="8da4d-120">**Store**</span></span>](store.md)
</dt> </dl>

 

 
