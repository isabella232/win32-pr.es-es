---
title: MPEXPIRATION_DATA estructura (MpClient. h)
description: Notificación de estado de expiración del producto.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- MPEXPIRATION_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPEXPIRATION_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPEXPIRATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df5e417b1ce6b1d1f4c15d646b44b0ea6c1fade2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651386"
---
# <a name="mpexpiration_data-structure"></a><span data-ttu-id="0dad1-105">\_Estructura de datos MPEXPIRATION</span><span class="sxs-lookup"><span data-stu-id="0dad1-105">MPEXPIRATION\_DATA structure</span></span>

<span data-ttu-id="0dad1-106">Notificación de estado de expiración del producto.</span><span class="sxs-lookup"><span data-stu-id="0dad1-106">Product expiration status notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dad1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0dad1-107">Syntax</span></span>


```C++
typedef struct tagMPEXPIRATION_DATA {
  MP_EXPIRE_REASON       Reason;
  MP_EXPIRE_STATE_REPORT State;
} MPEXPIRATION_DATA, *PMPEXPIRATION_DATA;
```



## <a name="members"></a><span data-ttu-id="0dad1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0dad1-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0dad1-109">**Motivo**</span><span class="sxs-lookup"><span data-stu-id="0dad1-109">**Reason**</span></span>
</dt> <dd>

<span data-ttu-id="0dad1-110">Tipo: **el \_ \_ motivo de expiración del módulo de administración**</span><span class="sxs-lookup"><span data-stu-id="0dad1-110">Type: **MP\_EXPIRE\_REASON**</span></span>

</dd> <dd>

<span data-ttu-id="0dad1-111">Motivo de la expiración.</span><span class="sxs-lookup"><span data-stu-id="0dad1-111">Expiration reason.</span></span> <span data-ttu-id="0dad1-112">Este es uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="0dad1-112">This is one of the following possible values:</span></span>



| <span data-ttu-id="0dad1-113">Value</span><span class="sxs-lookup"><span data-stu-id="0dad1-113">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="0dad1-114">Significado</span><span class="sxs-lookup"><span data-stu-id="0dad1-114">Meaning</span></span>                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <span data-ttu-id="0dad1-115"><dt>**Módulo de administración \_ EXPIRAdo \_ desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0dad1-115"><dt>**MP\_EXPIRED\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="0dad1-116">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="0dad1-116">Unknown.</span></span><br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <span data-ttu-id="0dad1-117"><dt>**Módulo de administración \_ \_Evaluación expirada**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0dad1-117"><dt>**MP\_EXPIRED\_EVAL**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="0dad1-118">Evaluación.</span><span class="sxs-lookup"><span data-stu-id="0dad1-118">Evaluation.</span></span><br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <span data-ttu-id="0dad1-119"><dt>**Módulo de administración \_ \_Wat expira**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0dad1-119"><dt>**MP\_EXPIRED\_WAT**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="0dad1-120">Desconoce.</span><span class="sxs-lookup"><span data-stu-id="0dad1-120">WAT.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="0dad1-121">**State**</span><span class="sxs-lookup"><span data-stu-id="0dad1-121">**State**</span></span>
</dt> <dd>

<span data-ttu-id="0dad1-122">Tipo: **\_ \_ \_ Informe de estado de expiración de MP**</span><span class="sxs-lookup"><span data-stu-id="0dad1-122">Type: **MP\_EXPIRE\_STATE\_REPORT**</span></span>

</dd> <dd>

<span data-ttu-id="0dad1-123">Estado de expiración.</span><span class="sxs-lookup"><span data-stu-id="0dad1-123">Expiration state.</span></span> <span data-ttu-id="0dad1-124">Este es uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="0dad1-124">This is one of the following possible values:</span></span>



| <span data-ttu-id="0dad1-125">Value</span><span class="sxs-lookup"><span data-stu-id="0dad1-125">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="0dad1-126">Significado</span><span class="sxs-lookup"><span data-stu-id="0dad1-126">Meaning</span></span>                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <span data-ttu-id="0dad1-127"><dt>**Módulo de administración \_ Informe de estado de EXPIRAción \_ \_ \_ desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0dad1-127"><dt>**MP\_EXPIRE\_STATE\_REPORT\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="0dad1-128">Estado desconocido.</span><span class="sxs-lookup"><span data-stu-id="0dad1-128">State unknown.</span></span><br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <span data-ttu-id="0dad1-129"><dt>**Módulo de administración \_ Informe de estado de EXPIRAción \_ \_ \_ válido**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0dad1-129"><dt>**MP\_EXPIRE\_STATE\_REPORT\_VALID**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="0dad1-130">Sin expiración.</span><span class="sxs-lookup"><span data-stu-id="0dad1-130">No expiration.</span></span><br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <span data-ttu-id="0dad1-131"><dt>**Módulo de administración \_ \_ \_ \_ Advertencia de informe de estado de expiración**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0dad1-131"><dt>**MP\_EXPIRE\_STATE\_REPORT\_WARNING**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="0dad1-132">Próximo expirado.</span><span class="sxs-lookup"><span data-stu-id="0dad1-132">Near expired.</span></span><br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <span data-ttu-id="0dad1-133"><dt>**Módulo de administración \_ El informe de estado de EXPIRAción \_ \_ \_ expiró**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0dad1-133"><dt>**MP\_EXPIRE\_STATE\_REPORT\_EXPIRED**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="0dad1-134">Expirado.</span><span class="sxs-lookup"><span data-stu-id="0dad1-134">Expired.</span></span><br/>       |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0dad1-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dad1-135">Requirements</span></span>



| <span data-ttu-id="0dad1-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dad1-136">Requirement</span></span> | <span data-ttu-id="0dad1-137">Value</span><span class="sxs-lookup"><span data-stu-id="0dad1-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0dad1-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dad1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0dad1-139">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0dad1-139">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0dad1-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0dad1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0dad1-141">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0dad1-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0dad1-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0dad1-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dad1-143"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dad1-143"><dt>MpClient.h</dt></span></span> </dl> |



 

 





