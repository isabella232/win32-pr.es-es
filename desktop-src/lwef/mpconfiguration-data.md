---
title: MPCONFIGURATION_DATA estructura (MpClient. h)
description: Contiene datos sobre los cambios de configuración, incluidos los valores antiguos y nuevos.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- MPCONFIGURATION_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPCONFIGURATION_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPCONFIGURATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb54ae4e323f2144dd25c52005d8484b0a207e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079223"
---
# <a name="mpconfiguration_data-structure"></a><span data-ttu-id="c9b44-105">\_Estructura de datos MPCONFIGURATION</span><span class="sxs-lookup"><span data-stu-id="c9b44-105">MPCONFIGURATION\_DATA structure</span></span>

<span data-ttu-id="c9b44-106">Contiene datos sobre los cambios de configuración, incluidos los valores antiguos y nuevos.</span><span class="sxs-lookup"><span data-stu-id="c9b44-106">Contains data about configuration changes, including the old and new values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b44-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9b44-107">Syntax</span></span>


```C++
typedef struct tagMPCONFIGURATION_DATA {
  MP_MIDL_STRING LPWSTR ConfigurationName;
  DWORD                 DataType;
  DWORD                 PreviousDataSize;
  BYTE                  *pPreviousData;
  DWORD                 CurrentDataSize;
  BYTE                  *pCurrentData;
} MPCONFIGURATION_DATA, *PMPCONFIGURATION_DATA;
```



## <a name="members"></a><span data-ttu-id="c9b44-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c9b44-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c9b44-109">**ConfigurationName**</span><span class="sxs-lookup"><span data-stu-id="c9b44-109">**ConfigurationName**</span></span>
</dt> <dd>

<span data-ttu-id="c9b44-110">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="c9b44-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="c9b44-111">Nombre de la configuración que cambió.</span><span class="sxs-lookup"><span data-stu-id="c9b44-111">Name of the configuration that changed.</span></span>

</dd> <dt>

<span data-ttu-id="c9b44-112">**DataType**</span><span class="sxs-lookup"><span data-stu-id="c9b44-112">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="c9b44-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c9b44-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c9b44-114">El tipo de datos utilizado.</span><span class="sxs-lookup"><span data-stu-id="c9b44-114">The type of data used.</span></span>

</dd> <dt>

<span data-ttu-id="c9b44-115">**PreviousDataSize**</span><span class="sxs-lookup"><span data-stu-id="c9b44-115">**PreviousDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="c9b44-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c9b44-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c9b44-117">Tamaño de los datos anteriores, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c9b44-117">Size of previous data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c9b44-118">**pPreviousData**</span><span class="sxs-lookup"><span data-stu-id="c9b44-118">**pPreviousData**</span></span>
</dt> <dd>

<span data-ttu-id="c9b44-119">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="c9b44-119">Type: \**BYTE\** _</span></span>

</dd> <dd>

<span data-ttu-id="c9b44-120">Puntero a los datos anteriores.</span><span class="sxs-lookup"><span data-stu-id="c9b44-120">Pointer to previous data.</span></span>

</dd> <dt>

<span data-ttu-id="c9b44-121">_ *CurrentDataSize*\*</span><span class="sxs-lookup"><span data-stu-id="c9b44-121">_ *CurrentDataSize*\*</span></span>
</dt> <dd>

<span data-ttu-id="c9b44-122">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="c9b44-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="c9b44-123">Tamaño de los datos nuevos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c9b44-123">Size of new data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c9b44-124">**pCurrentData**</span><span class="sxs-lookup"><span data-stu-id="c9b44-124">**pCurrentData**</span></span>
</dt> <dd>

<span data-ttu-id="c9b44-125">Tipo: **byte \***</span><span class="sxs-lookup"><span data-stu-id="c9b44-125">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="c9b44-126">Puntero a los nuevos datos.</span><span class="sxs-lookup"><span data-stu-id="c9b44-126">Pointer to new data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9b44-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9b44-127">Requirements</span></span>



| <span data-ttu-id="c9b44-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9b44-128">Requirement</span></span> | <span data-ttu-id="c9b44-129">Value</span><span class="sxs-lookup"><span data-stu-id="c9b44-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b44-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9b44-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c9b44-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9b44-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c9b44-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c9b44-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c9b44-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c9b44-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9b44-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9b44-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9b44-135"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9b44-135"><dt>MpClient.h</dt></span></span> </dl> |



 

 





