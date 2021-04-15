---
title: MPTHREAT_LOCALIZED_INFO estructura (MpClient. h)
description: Información localizada para una amenaza.
ms.assetid: 99DC9737-9A61-4407-B544-A7A979C5B556
keywords:
- MPTHREAT_LOCALIZED_INFO estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_LOCALIZED_INFO características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_LOCALIZED_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87ea0bee7c8cae15389b40b64038aad92a56dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422284"
---
# <a name="mpthreat_localized_info-structure"></a><span data-ttu-id="2adb1-105">MPTHREAT \_ estructura de \_ información localizada</span><span class="sxs-lookup"><span data-stu-id="2adb1-105">MPTHREAT\_LOCALIZED\_INFO structure</span></span>

<span data-ttu-id="2adb1-106">Información localizada para una amenaza.</span><span class="sxs-lookup"><span data-stu-id="2adb1-106">Localized information for a threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="2adb1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2adb1-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_LOCALIZED_INFO {
  MPTHREAT_ID           ThreatID;
  MP_MIDL_STRING LPWSTR CategoryName;
  MP_MIDL_STRING LPWSTR CategoryDescription;
  MP_MIDL_STRING LPWSTR SeverityName;
  MP_MIDL_STRING LPWSTR SeverityDescription;
  MP_MIDL_STRING LPWSTR ShortDescription;
  MP_MIDL_STRING LPWSTR DefaultActionName;;
  MP_MIDL_STRING LPWSTR Advice;
  MP_MIDL_STRING LPWSTR ThreatUrl;
} MPTHREAT_LOCALIZED_INFO, *PMPTHREAT_LOCALIZED_INFO;
```



## <a name="members"></a><span data-ttu-id="2adb1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2adb1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2adb1-109">**ThreatID**</span><span class="sxs-lookup"><span data-stu-id="2adb1-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="2adb1-110">Tipo: **\_ ID. de MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="2adb1-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="2adb1-111">Identificador de amenaza.</span><span class="sxs-lookup"><span data-stu-id="2adb1-111">Threat identifier.</span></span> <span data-ttu-id="2adb1-112">El bit superior se establece para identificar las amenazas relacionadas con el antivirus.</span><span class="sxs-lookup"><span data-stu-id="2adb1-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="2adb1-113">**CategoryName**</span><span class="sxs-lookup"><span data-stu-id="2adb1-113">**CategoryName**</span></span>
</dt> <dd>

<span data-ttu-id="2adb1-114">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="2adb1-114">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="2adb1-115">Clasificación de amenazas, como un troyano o un registrador de virus.</span><span class="sxs-lookup"><span data-stu-id="2adb1-115">Threat classification, such as a trojan or a keylogger.</span></span>

</dd> <dt>

<span data-ttu-id="2adb1-116">**CategoryDescription**</span><span class="sxs-lookup"><span data-stu-id="2adb1-116">**CategoryDescription**</span></span>
</dt> <dd>

<span data-ttu-id="2adb1-117">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="2adb1-117">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="2adb1-118">Descripción de la categoría de amenaza.</span><span class="sxs-lookup"><span data-stu-id="2adb1-118">Description of threat category.</span></span>

</dd> <dt>

<span data-ttu-id="2adb1-119">**SeverityName**</span><span class="sxs-lookup"><span data-stu-id="2adb1-119">**SeverityName**</span></span>
</dt> <dd>

<span data-ttu-id="2adb1-120">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="2adb1-120">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="2adb1-121">Nivel de gravedad de las amenazas, como grave o moderado.</span><span class="sxs-lookup"><span data-stu-id="2adb1-121">Threat severity level, such as severe or moderate.</span></span>

</dd> <dt>

<span data-ttu-id="2adb1-122">**SeverityDescription**</span><span class="sxs-lookup"><span data-stu-id="2adb1-122">**SeverityDescription**</span></span>
</dt> <dd>

<span data-ttu-id="2adb1-123">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="2adb1-123">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="2adb1-124">Descripción del nivel de gravedad de las amenazas.</span><span class="sxs-lookup"><span data-stu-id="2adb1-124">Description of threat severity level.</span></span>

</dd> <dt>

<span data-ttu-id="2adb1-125">**ShortDescription**</span><span class="sxs-lookup"><span data-stu-id="2adb1-125">**ShortDescription**</span></span>
</dt> <dd>

<span data-ttu-id="2adb1-126">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="2adb1-126">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="2adb1-127">Breve descripción de la amenaza.</span><span class="sxs-lookup"><span data-stu-id="2adb1-127">Short description of threat.</span></span>

</dd> <dt>

<span data-ttu-id="2adb1-128">**DefaultActionName;**</span><span class="sxs-lookup"><span data-stu-id="2adb1-128">**DefaultActionName;**</span></span>
</dt> <dd>

<span data-ttu-id="2adb1-129">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="2adb1-129">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="2adb1-130">Nombre de la acción predeterminada, como quitar o poner en cuarentena, sugerida por el motor.</span><span class="sxs-lookup"><span data-stu-id="2adb1-130">Name of default action, such as remove or quarantine, suggested by engine.</span></span>

</dd> <dt>

<span data-ttu-id="2adb1-131">**Advice**</span><span class="sxs-lookup"><span data-stu-id="2adb1-131">**Advice**</span></span>
</dt> <dd>

<span data-ttu-id="2adb1-132">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="2adb1-132">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="2adb1-133">Consejos para la amenaza concreta.</span><span class="sxs-lookup"><span data-stu-id="2adb1-133">Advice for the particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="2adb1-134">**ThreatUrl**</span><span class="sxs-lookup"><span data-stu-id="2adb1-134">**ThreatUrl**</span></span>
</dt> <dd>

<span data-ttu-id="2adb1-135">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="2adb1-135">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="2adb1-136">Una dirección URL a una página web que contiene información sobre la amenaza.</span><span class="sxs-lookup"><span data-stu-id="2adb1-136">A URL to a webpage containing information about the threat.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2adb1-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2adb1-137">Requirements</span></span>



| <span data-ttu-id="2adb1-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="2adb1-138">Requirement</span></span> | <span data-ttu-id="2adb1-139">Value</span><span class="sxs-lookup"><span data-stu-id="2adb1-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2adb1-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2adb1-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2adb1-141">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2adb1-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2adb1-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2adb1-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2adb1-143">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2adb1-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2adb1-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2adb1-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="2adb1-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2adb1-145"><dt>MpClient.h</dt></span></span> </dl> |



 

 





