---
title: MPTHREAT_INFOEX_BEHAVIOR estructura (MpClient. h)
description: Contiene información específica de la modificación del comportamiento.
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- MPTHREAT_INFOEX_BEHAVIOR estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPTHREAT_INFOEX_BEHAVIOR características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_BEHAVIOR
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0bc00aeb56aec38b88f2590211c705079834f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803530"
---
# <a name="mpthreat_infoex_behavior-structure"></a><span data-ttu-id="00a7e-105">MPTHREAT \_ estructura de comportamiento de INFOEX \_</span><span class="sxs-lookup"><span data-stu-id="00a7e-105">MPTHREAT\_INFOEX\_BEHAVIOR structure</span></span>

<span data-ttu-id="00a7e-106">Contiene información específica de la modificación del comportamiento.</span><span class="sxs-lookup"><span data-stu-id="00a7e-106">Contains behavior modification-specific information.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a7e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00a7e-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_INFOEX_BEHAVIOR {
  ULARGE_INTEGER         SignatureID;
  ULONGLONG              EngineVersion;
  ULONGLONG              ASDeltaSignatureVersion;
  ULONGLONG              AVDeltaSignatureVersion;
  MP_HASH_TYPE           HashType;
  DWORD                  FidelityValue;
  MP_MIDL_STRING  LPWSTR HashValue;
  MP_MIDL_STRING  LPWSTR TargetFileName;
  MP_MIDL_STRING  LPWSTR TargetFileHash;
} MPTHREAT_INFOEX_BEHAVIOR, *PMPTHREAT_INFOEX_BEHAVIOR;
```



## <a name="members"></a><span data-ttu-id="00a7e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="00a7e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="00a7e-109">**SignatureID**</span><span class="sxs-lookup"><span data-stu-id="00a7e-109">**SignatureID**</span></span>
</dt> <dd>

<span data-ttu-id="00a7e-110">Tipo: **ULARGE \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="00a7e-110">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="00a7e-111">IDENTIFICADOR de la firma de modificación del comportamiento proporcionado por el motor en el momento de la detección.</span><span class="sxs-lookup"><span data-stu-id="00a7e-111">Behavior modification signature ID given by the engine at the time of detection.</span></span>

</dd> <dt>

<span data-ttu-id="00a7e-112">**EngineVersion**</span><span class="sxs-lookup"><span data-stu-id="00a7e-112">**EngineVersion**</span></span>
</dt> <dd>

<span data-ttu-id="00a7e-113">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="00a7e-113">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="00a7e-114">Versión del módulo del motor.</span><span class="sxs-lookup"><span data-stu-id="00a7e-114">Engine module version.</span></span>

</dd> <dt>

<span data-ttu-id="00a7e-115">**ASDeltaSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="00a7e-115">**ASDeltaSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="00a7e-116">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="00a7e-116">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="00a7e-117">Versión de la firma de AntiSpyware.</span><span class="sxs-lookup"><span data-stu-id="00a7e-117">Antispyware signature version.</span></span>

</dd> <dt>

<span data-ttu-id="00a7e-118">**AVDeltaSignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="00a7e-118">**AVDeltaSignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="00a7e-119">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="00a7e-119">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="00a7e-120">Versión de firma de antivirus</span><span class="sxs-lookup"><span data-stu-id="00a7e-120">Antivirus signature version</span></span>

</dd> <dt>

<span data-ttu-id="00a7e-121">**HashType**</span><span class="sxs-lookup"><span data-stu-id="00a7e-121">**HashType**</span></span>
</dt> <dd>

<span data-ttu-id="00a7e-122">Tipo: **[ **\_ \_ tipo hash de MP**](mp-hash-type.md)**</span><span class="sxs-lookup"><span data-stu-id="00a7e-122">Type: **[**MP\_HASH\_TYPE**](mp-hash-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="00a7e-123">Tipo hash usado.</span><span class="sxs-lookup"><span data-stu-id="00a7e-123">Hash type used.</span></span> <span data-ttu-id="00a7e-124">Vea [**\_ \_ tipo de hash de MP**](mp-hash-type.md).</span><span class="sxs-lookup"><span data-stu-id="00a7e-124">See [**MP\_HASH\_TYPE**](mp-hash-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="00a7e-125">**FidelityValue**</span><span class="sxs-lookup"><span data-stu-id="00a7e-125">**FidelityValue**</span></span>
</dt> <dd>

<span data-ttu-id="00a7e-126">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="00a7e-126">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="00a7e-127">Valor de fidelidad.</span><span class="sxs-lookup"><span data-stu-id="00a7e-127">Fidelity value.</span></span>

</dd> <dt>

<span data-ttu-id="00a7e-128">**HashValue**</span><span class="sxs-lookup"><span data-stu-id="00a7e-128">**HashValue**</span></span>
</dt> <dd>

<span data-ttu-id="00a7e-129">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="00a7e-129">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="00a7e-130">Hash del archivo.</span><span class="sxs-lookup"><span data-stu-id="00a7e-130">The hash of the file.</span></span>

</dd> <dt>

<span data-ttu-id="00a7e-131">**TargetFileName**</span><span class="sxs-lookup"><span data-stu-id="00a7e-131">**TargetFileName**</span></span>
</dt> <dd>

<span data-ttu-id="00a7e-132">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="00a7e-132">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="00a7e-133">La ruta de acceso y el nombre del archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="00a7e-133">The path and name of the targeted file.</span></span>

</dd> <dt>

<span data-ttu-id="00a7e-134">**TargetFileHash**</span><span class="sxs-lookup"><span data-stu-id="00a7e-134">**TargetFileHash**</span></span>
</dt> <dd>

<span data-ttu-id="00a7e-135">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="00a7e-135">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="00a7e-136">El hash del archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="00a7e-136">The hash of the targeted file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="00a7e-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00a7e-137">Requirements</span></span>



| <span data-ttu-id="00a7e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="00a7e-138">Requirement</span></span> | <span data-ttu-id="00a7e-139">Value</span><span class="sxs-lookup"><span data-stu-id="00a7e-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00a7e-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00a7e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="00a7e-141">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="00a7e-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="00a7e-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00a7e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="00a7e-143">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="00a7e-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00a7e-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00a7e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="00a7e-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="00a7e-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00a7e-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="00a7e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a7e-147">**\_tipo hash de MP \_**</span><span class="sxs-lookup"><span data-stu-id="00a7e-147">**MP\_HASH\_TYPE**</span></span>](mp-hash-type.md)
</dt> </dl>

 

 





