---
description: Establece o recupera la \_ \_ Ubicación del almacén de CAPICOM de un almacén de certificados.
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: 'ICertStore:: StoreLocation (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreLocation
- ICertStore.get_StoreLocation
- ICertStore.put_StoreLocation
- CertStore.StoreLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 97bca7ed9dae20c129d202910b40f7c26d54a576
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670919"
---
# <a name="icertstorestorelocation-property"></a><span data-ttu-id="480f7-103">ICertStore:: StoreLocation (propiedad)</span><span class="sxs-lookup"><span data-stu-id="480f7-103">ICertStore::StoreLocation property</span></span>

<span data-ttu-id="480f7-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="480f7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="480f7-105">La propiedad **StoreLocation** establece o recupera la [**\_ \_ Ubicación del almacén de CAPICOM**](capicom-store-location.md) de un almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="480f7-105">The **StoreLocation** property sets or retrieves the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) of a certificate store.</span></span>

<span data-ttu-id="480f7-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="480f7-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="480f7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="480f7-107">Syntax</span></span>


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="480f7-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="480f7-108">Property value</span></span>

<span data-ttu-id="480f7-109">Ubicación del almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="480f7-109">The location of the certificate store.</span></span>

## <a name="error-codes"></a><span data-ttu-id="480f7-110">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="480f7-110">Error codes</span></span>

<span data-ttu-id="480f7-111">Si los métodos de acceso de propiedad **colocan \_ StoreLocation** y **Get \_ StoreLocation** se ejecutan correctamente, devuelven los valores \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="480f7-111">If the property access methods **put\_StoreLocation** and **get\_StoreLocation** succeed, they return S\_OK.</span></span>

<span data-ttu-id="480f7-112">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="480f7-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="480f7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="480f7-113">Requirements</span></span>



| <span data-ttu-id="480f7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="480f7-114">Requirement</span></span> | <span data-ttu-id="480f7-115">Value</span><span class="sxs-lookup"><span data-stu-id="480f7-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="480f7-116">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="480f7-116">Redistributable</span></span><br/> | <span data-ttu-id="480f7-117">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="480f7-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="480f7-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="480f7-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="480f7-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="480f7-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="480f7-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="480f7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="480f7-121">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="480f7-121">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




