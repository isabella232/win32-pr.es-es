---
title: Estructura LSKeyPack
description: Contiene información sobre un paquete de claves de licencias de Servicios de Escritorio remoto específico.
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la estructura LSKeyPack
- Puntero de estructura LPLSKeyPack Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b1ac1f51e66a0a3c15c33f2535bc02f1fd3528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996983"
---
# <a name="lskeypack-structure"></a><span data-ttu-id="10c63-105">Estructura LSKeyPack</span><span class="sxs-lookup"><span data-stu-id="10c63-105">LSKeyPack structure</span></span>

<span data-ttu-id="10c63-106">Contiene información sobre un paquete de claves de licencias de Servicios de Escritorio remoto específico.</span><span class="sxs-lookup"><span data-stu-id="10c63-106">Contains information about a specific Remote Desktop Services licensing key pack.</span></span>

> [!Note]  
> <span data-ttu-id="10c63-107">Esta estructura no está definida en ningún archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="10c63-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="10c63-108">Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.</span><span class="sxs-lookup"><span data-stu-id="10c63-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="10c63-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10c63-109">Syntax</span></span>


```C++
typedef struct _LSKeyPack {
  DWORD dwVersion;
  UCHAR ucKeyPackType;
  TCHAR szCompanyName[256];
  TCHAR szKeyPackId[256];
  TCHAR szProductName[256];
  TCHAR szProductId[256];
  TCHAR szProductDesc[256];
  WORD  wMajorVersion;
  WORD  wMinorVersion;
  DWORD dwPlatformType;
  UCHAR ucLicenseType;
  DWORD dwLanguageId;
  UCHAR ucChannelOfPurchase;
  TCHAR szBeginSerialNumber[256];
  DWORD dwTotalLicenseInKeyPack;
  DWORD dwProductFlags;
  DWORD dwKeyPackId;
  UCHAR ucKeyPackStatus;
  DWORD dwActivateDate;
  DWORD dwExpirationDate;
  DWORD dwNumberOfLicenses;
} LSKeyPack, *LPLSKeyPack;
```



## <a name="members"></a><span data-ttu-id="10c63-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="10c63-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="10c63-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="10c63-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-112">Versión del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-112">Version of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-113">**ucKeyPackType**</span><span class="sxs-lookup"><span data-stu-id="10c63-113">**ucKeyPackType**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-114">Tipo de paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-114">Type of key pack.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-115">**szCompanyName**</span><span class="sxs-lookup"><span data-stu-id="10c63-115">**szCompanyName**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-116">Nombre de la compañía que emitió el paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-116">Name of the company that issued the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-117">**szKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="10c63-117">**szKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-118">IDENTIFICADOR del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-118">ID of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-119">**szProductName**</span><span class="sxs-lookup"><span data-stu-id="10c63-119">**szProductName**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-120">Nombre del producto al que pertenece este paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-120">Name of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-121">**szProductId**</span><span class="sxs-lookup"><span data-stu-id="10c63-121">**szProductId**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-122">IDENTIFICADOR del producto al que pertenece este paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-122">ID of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-123">**szProductDesc**</span><span class="sxs-lookup"><span data-stu-id="10c63-123">**szProductDesc**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-124">Descripción del producto al que pertenece este paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-124">Description of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-125">**wMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="10c63-125">**wMajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-126">Versión principal del producto al que pertenece este paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-126">Major version of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-127">**wMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="10c63-127">**wMinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-128">Versión secundaria del producto al que pertenece este paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-128">Minor version of the product to which this key pack belongs.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-129">**dwPlatformType**</span><span class="sxs-lookup"><span data-stu-id="10c63-129">**dwPlatformType**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-130">Tipo de plataforma.</span><span class="sxs-lookup"><span data-stu-id="10c63-130">Platform type.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-131">**ucLicenseType**</span><span class="sxs-lookup"><span data-stu-id="10c63-131">**ucLicenseType**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-132">Tipo de licencias en el paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-132">Type of licenses in the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-133">**dwLanguageId**</span><span class="sxs-lookup"><span data-stu-id="10c63-133">**dwLanguageId**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-134">Identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="10c63-134">Language ID.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-135">**ucChannelOfPurchase**</span><span class="sxs-lookup"><span data-stu-id="10c63-135">**ucChannelOfPurchase**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-136">Canal de compra.</span><span class="sxs-lookup"><span data-stu-id="10c63-136">Channel of purchase.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-137">**szBeginSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="10c63-137">**szBeginSerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-138">Número de serie de la primera licencia.</span><span class="sxs-lookup"><span data-stu-id="10c63-138">Serial number for the first license.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-139">**dwTotalLicenseInKeyPack**</span><span class="sxs-lookup"><span data-stu-id="10c63-139">**dwTotalLicenseInKeyPack**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-140">Número total de licencias en el paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-140">Total number of licenses in the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-141">**dwProductFlags**</span><span class="sxs-lookup"><span data-stu-id="10c63-141">**dwProductFlags**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-142">Marcas.</span><span class="sxs-lookup"><span data-stu-id="10c63-142">Flags.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-143">**dwKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="10c63-143">**dwKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-144">IDENTIFICADOR del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-144">ID of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-145">**ucKeyPackStatus**</span><span class="sxs-lookup"><span data-stu-id="10c63-145">**ucKeyPackStatus**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-146">Estado del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-146">Status of the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-147">**dwActivateDate**</span><span class="sxs-lookup"><span data-stu-id="10c63-147">**dwActivateDate**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-148">Fecha de activación del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-148">Activation date for the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-149">**dwExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="10c63-149">**dwExpirationDate**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-150">Fecha de expiración del paquete de claves.</span><span class="sxs-lookup"><span data-stu-id="10c63-150">Expiration date for the key pack.</span></span>

</dd> <dt>

<span data-ttu-id="10c63-151">**dwNumberOfLicenses**</span><span class="sxs-lookup"><span data-stu-id="10c63-151">**dwNumberOfLicenses**</span></span>
</dt> <dd>

<span data-ttu-id="10c63-152">Número de licencias.</span><span class="sxs-lookup"><span data-stu-id="10c63-152">Number of licenses.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10c63-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10c63-153">Requirements</span></span>



| <span data-ttu-id="10c63-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="10c63-154">Requirement</span></span> | <span data-ttu-id="10c63-155">Value</span><span class="sxs-lookup"><span data-stu-id="10c63-155">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="10c63-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10c63-156">Minimum supported client</span></span><br/> | <span data-ttu-id="10c63-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10c63-157">Windows Vista</span></span><br/>       |
| <span data-ttu-id="10c63-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10c63-158">Minimum supported server</span></span><br/> | <span data-ttu-id="10c63-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10c63-159">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10c63-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="10c63-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10c63-161">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="10c63-161">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="10c63-162">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="10c63-162">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dt>

[<span data-ttu-id="10c63-163">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="10c63-163">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

 





