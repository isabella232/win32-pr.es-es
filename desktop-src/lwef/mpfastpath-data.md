---
title: MPFASTPATH_DATA estructura (MpClient. h)
description: Notificación de actualización de FastPath.
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- MPFASTPATH_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPFASTPATH_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPFASTPATH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2850a48074fee6984564550683c7fe595d0779ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714564"
---
# <a name="mpfastpath_data-structure"></a><span data-ttu-id="1dc9b-105">\_Estructura de datos MPFASTPATH</span><span class="sxs-lookup"><span data-stu-id="1dc9b-105">MPFASTPATH\_DATA structure</span></span>

<span data-ttu-id="1dc9b-106">Notificación de actualización de FastPath.</span><span class="sxs-lookup"><span data-stu-id="1dc9b-106">FastPath update notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dc9b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1dc9b-107">Syntax</span></span>


```C++
typedef struct tagMPFASTPATH_DATA {
  MP_SIGNATURE_TYPE         SignatureType;
  MP_FASTPATH_TYPE          FastPathSignatureType;
  MP_MIDL_STRING LPWSTR     FastPathSignatureVersion;
  ULARGE_INTEGER            CompilationTimestamp;
  MP_PERSISTENCE_LIMIT_TYPE PersistenceType;
  MP_MIDL_STRING LPWSTR     PersistenceValue;
  MP_MIDL_STRING LPWSTR     PersistencePath;
  MP_REMOVAL_REASON         Reason;
} MPFASTPATH_DATA, *PMPFASTPATH_DATA;
```



## <a name="members"></a><span data-ttu-id="1dc9b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="1dc9b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1dc9b-109">**SignatureType**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-109">**SignatureType**</span></span>
</dt> <dd>

<span data-ttu-id="1dc9b-110">Tipo: **[ **\_ \_ tipo de firma de MP**](mp-signature-type.md)**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-110">Type: **[**MP\_SIGNATURE\_TYPE**](mp-signature-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1dc9b-111">Tipo de firma.</span><span class="sxs-lookup"><span data-stu-id="1dc9b-111">Signature type.</span></span>

</dd> <dt>

<span data-ttu-id="1dc9b-112">**FastPathSignatureType**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-112">**FastPathSignatureType**</span></span>
</dt> <dd>

<span data-ttu-id="1dc9b-113">Tipo: **[ **MP \_ FASTPATH \_ Type**](mp-fastpath-type.md)**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-113">Type: **[**MP\_FASTPATH\_TYPE**](mp-fastpath-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1dc9b-114">Tipo de firma FastPath.</span><span class="sxs-lookup"><span data-stu-id="1dc9b-114">FastPath signature type.</span></span>

</dd> <dt>

<span data-ttu-id="1dc9b-115">**FastPathSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-115">**FastPathSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1dc9b-116">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-116">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="1dc9b-117">Versión de la firma FastPath (opcional).</span><span class="sxs-lookup"><span data-stu-id="1dc9b-117">FastPath signature version (optional).</span></span>

</dd> <dt>

<span data-ttu-id="1dc9b-118">**CompilationTimestamp**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-118">**CompilationTimestamp**</span></span>
</dt> <dd>

<span data-ttu-id="1dc9b-119">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-119">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="1dc9b-120">Marca de tiempo de compilación (UTC).</span><span class="sxs-lookup"><span data-stu-id="1dc9b-120">Compilation timestamp (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="1dc9b-121">**PersistenceType**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-121">**PersistenceType**</span></span>
</dt> <dd>

<span data-ttu-id="1dc9b-122">Tipo: **[ **\_ tipo de \_ límite \_ de persistencia de MP**](mp-persistence-limit-type.md)**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-122">Type: **[**MP\_PERSISTENCE\_LIMIT\_TYPE**](mp-persistence-limit-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1dc9b-123">Tipo de persistencia (opcional).</span><span class="sxs-lookup"><span data-stu-id="1dc9b-123">Persistence type (optional).</span></span>

</dd> <dt>

<span data-ttu-id="1dc9b-124">**PersistenceValue**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-124">**PersistenceValue**</span></span>
</dt> <dd>

<span data-ttu-id="1dc9b-125">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-125">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="1dc9b-126">Valor de persistencia (opcional).</span><span class="sxs-lookup"><span data-stu-id="1dc9b-126">Persistence value (optional).</span></span>

</dd> <dt>

<span data-ttu-id="1dc9b-127">**PersistencePath**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-127">**PersistencePath**</span></span>
</dt> <dd>

<span data-ttu-id="1dc9b-128">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-128">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="1dc9b-129">Ruta de acceso de persistencia (opcional).</span><span class="sxs-lookup"><span data-stu-id="1dc9b-129">Persistence path (optional).</span></span>

</dd> <dt>

<span data-ttu-id="1dc9b-130">**Motivo**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-130">**Reason**</span></span>
</dt> <dd>

<span data-ttu-id="1dc9b-131">Tipo: **[ **\_ \_ motivo** de la eliminación del MP](mp-removal-reason.md)**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-131">Type: **[**MP\_REMOVAL\_REASON**](mp-removal-reason.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1dc9b-132">Motivo de la eliminación de la firma.</span><span class="sxs-lookup"><span data-stu-id="1dc9b-132">Reason for signature removal.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1dc9b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dc9b-133">Requirements</span></span>



| <span data-ttu-id="1dc9b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dc9b-134">Requirement</span></span> | <span data-ttu-id="1dc9b-135">Value</span><span class="sxs-lookup"><span data-stu-id="1dc9b-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc9b-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dc9b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1dc9b-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1dc9b-137">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1dc9b-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dc9b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1dc9b-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1dc9b-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1dc9b-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1dc9b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dc9b-141"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dc9b-141"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dc9b-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="1dc9b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc9b-143">**\_tipo de FASTPATH de MP \_**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-143">**MP\_FASTPATH\_TYPE**</span></span>](mp-fastpath-type.md)
</dt> <dt>

[<span data-ttu-id="1dc9b-144">**\_tipo de \_ límite de persistencia de MP \_**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-144">**MP\_PERSISTENCE\_LIMIT\_TYPE**</span></span>](mp-persistence-limit-type.md)
</dt> <dt>

[<span data-ttu-id="1dc9b-145">**\_tipo de firma MP \_**</span><span class="sxs-lookup"><span data-stu-id="1dc9b-145">**MP\_SIGNATURE\_TYPE**</span></span>](mp-signature-type.md)
</dt> </dl>

 

 





