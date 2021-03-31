---
title: Estructura LSLicense
description: Contiene información acerca de una licencia de Servicios de Escritorio remoto específica.
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la estructura LSLicense
- Puntero de estructura LPLSLicense Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dcb8551c1d1edfd9486d42df63de9a76fab38433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490331"
---
# <a name="lslicense-structure"></a><span data-ttu-id="63e11-105">Estructura LSLicense</span><span class="sxs-lookup"><span data-stu-id="63e11-105">LSLicense structure</span></span>

<span data-ttu-id="63e11-106">Contiene información acerca de una licencia de Servicios de Escritorio remoto específica.</span><span class="sxs-lookup"><span data-stu-id="63e11-106">Contains information about a specific Remote Desktop Services license.</span></span>

> [!Note]  
> <span data-ttu-id="63e11-107">Esta estructura no está definida en ningún archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="63e11-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="63e11-108">Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.</span><span class="sxs-lookup"><span data-stu-id="63e11-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="63e11-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63e11-109">Syntax</span></span>


```C++
typedef struct _LSLicense {
  DWORD dwVersion;
  DWORD dwLicenseId;
  DWORD dwKeyPackId;
  TCHAR szHWID[GUID_MAX_SIZE];
  TCHAR szMachineName[MAXCOMPUTERNAMELENGTH];
  TCHAR szUserName[MAXUSERNAMELENGTH];
  DWORD dwCertSerialLicense;
  DWORD dwLicenseSerialNumber;
  DWORD ftIssueDate;
  DWORD ftExpireDate;
  UCHAR ucLicenseStatus;
} LSLicense, *LPLSLicense;
```



## <a name="members"></a><span data-ttu-id="63e11-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="63e11-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="63e11-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="63e11-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="63e11-112">Versión de la licencia.</span><span class="sxs-lookup"><span data-stu-id="63e11-112">Version of the license.</span></span>

</dd> <dt>

<span data-ttu-id="63e11-113">**dwLicenseId**</span><span class="sxs-lookup"><span data-stu-id="63e11-113">**dwLicenseId**</span></span>
</dt> <dd>

<span data-ttu-id="63e11-114">IDENTIFICADOR de la licencia.</span><span class="sxs-lookup"><span data-stu-id="63e11-114">ID of the license.</span></span>

</dd> <dt>

<span data-ttu-id="63e11-115">**dwKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="63e11-115">**dwKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="63e11-116">IDENTIFICADOR del [**LSKeyPack**](lskeypack.md) que contiene la licencia.</span><span class="sxs-lookup"><span data-stu-id="63e11-116">ID of the [**LSKeyPack**](lskeypack.md) that contains the license.</span></span>

</dd> <dt>

<span data-ttu-id="63e11-117">**szHWID**</span><span class="sxs-lookup"><span data-stu-id="63e11-117">**szHWID**</span></span>
</dt> <dd>

<span data-ttu-id="63e11-118">IDENTIFICADOR de hardware del cliente de Conexión a Escritorio remoto (RDC) que emitió la licencia.</span><span class="sxs-lookup"><span data-stu-id="63e11-118">Hardware ID of the Remote Desktop Connection (RDC) client that was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="63e11-119">**szMachineName**</span><span class="sxs-lookup"><span data-stu-id="63e11-119">**szMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="63e11-120">Nombre del cliente de Conexión a Escritorio remoto (RDC) que emitió la licencia.</span><span class="sxs-lookup"><span data-stu-id="63e11-120">Name of the Remote Desktop Connection (RDC) client that was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="63e11-121">**szUserName**</span><span class="sxs-lookup"><span data-stu-id="63e11-121">**szUserName**</span></span>
</dt> <dd>

<span data-ttu-id="63e11-122">Nombre del usuario que emitió la licencia.</span><span class="sxs-lookup"><span data-stu-id="63e11-122">Name of the user who was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="63e11-123">**dwCertSerialLicense**</span><span class="sxs-lookup"><span data-stu-id="63e11-123">**dwCertSerialLicense**</span></span>
</dt> <dd>

<span data-ttu-id="63e11-124">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="63e11-124">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="63e11-125">**dwLicenseSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="63e11-125">**dwLicenseSerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="63e11-126">Número de serie de la licencia.</span><span class="sxs-lookup"><span data-stu-id="63e11-126">Serial number of the license.</span></span>

</dd> <dt>

<span data-ttu-id="63e11-127">**ftIssueDate**</span><span class="sxs-lookup"><span data-stu-id="63e11-127">**ftIssueDate**</span></span>
</dt> <dd>

<span data-ttu-id="63e11-128">Fecha en que se emitió la licencia.</span><span class="sxs-lookup"><span data-stu-id="63e11-128">Date that the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="63e11-129">**ftExpireDate**</span><span class="sxs-lookup"><span data-stu-id="63e11-129">**ftExpireDate**</span></span>
</dt> <dd>

<span data-ttu-id="63e11-130">Fecha en que expirará la licencia.</span><span class="sxs-lookup"><span data-stu-id="63e11-130">Date that the license will expire.</span></span>

</dd> <dt>

<span data-ttu-id="63e11-131">**ucLicenseStatus**</span><span class="sxs-lookup"><span data-stu-id="63e11-131">**ucLicenseStatus**</span></span>
</dt> <dd>

<span data-ttu-id="63e11-132">Estado actual de la licencia.</span><span class="sxs-lookup"><span data-stu-id="63e11-132">Current status of the license.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63e11-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63e11-133">Requirements</span></span>



| <span data-ttu-id="63e11-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="63e11-134">Requirement</span></span> | <span data-ttu-id="63e11-135">Value</span><span class="sxs-lookup"><span data-stu-id="63e11-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="63e11-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63e11-136">Minimum supported client</span></span><br/> | <span data-ttu-id="63e11-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63e11-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="63e11-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63e11-138">Minimum supported server</span></span><br/> | <span data-ttu-id="63e11-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63e11-139">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63e11-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="63e11-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e11-141">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="63e11-141">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="63e11-142">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="63e11-142">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="63e11-143">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="63e11-143">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dt>

[<span data-ttu-id="63e11-144">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="63e11-144">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

 





