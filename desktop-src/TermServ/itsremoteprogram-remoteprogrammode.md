---
title: Propiedad RemoteProgramMode de ITSRemoteProgram
description: Modo RemoteApp de Windows Server 2008 R2.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RemoteProgramMode
- Propiedad RemoteProgramMode Servicios de Escritorio remoto, interfaz ITSRemoteProgram
- Servicios de Escritorio remoto de la interfaz ITSRemoteProgram, propiedad RemoteProgramMode
- Propiedad RemoteProgramMode Servicios de Escritorio remoto, interfaz ITSRemoteProgram2
- Servicios de Escritorio remoto de la interfaz ITSRemoteProgram2, propiedad RemoteProgramMode
- Propiedad RemoteProgramMode Servicios de Escritorio remoto, interfaz ITSRemoteProgram3
- Servicios de Escritorio remoto de la interfaz ITSRemoteProgram3, propiedad RemoteProgramMode
topic_type:
- apiref
api_name:
- ITSRemoteProgram.RemoteProgramMode
- ITSRemoteProgram.get_RemoteProgramMode
- ITSRemoteProgram.put_RemoteProgramMode
- ITSRemoteProgram2.RemoteProgramMode
- ITSRemoteProgram2.get_RemoteProgramMode
- ITSRemoteProgram2.put_RemoteProgramMode
- ITSRemoteProgram3.RemoteProgramMode
- ITSRemoteProgram3.get_RemoteProgramMode
- ITSRemoteProgram3.put_RemoteProgramMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8582824e2f6349e37b125ffd974847b602ad6fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686016"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a><span data-ttu-id="e0bd5-110">ITSRemoteProgram:: RemoteProgramMode (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e0bd5-110">ITSRemoteProgram::RemoteProgramMode property</span></span>

<span data-ttu-id="e0bd5-111">Modo RemoteApp de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-111">The Windows Server 2008 R2 RemoteApp mode.</span></span>

<span data-ttu-id="e0bd5-112">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0bd5-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0bd5-113">Syntax</span></span>


```C++
HRESULT put_RemoteProgramMode(
  [in]  VARIANT_BOOL vboolRemoteProgramMode
);

HRESULT get_RemoteProgramMode(
  [out] VARIANT_BOOL *pvboolRemoteProgramMode
);
```



## <a name="property-value"></a><span data-ttu-id="e0bd5-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e0bd5-114">Property value</span></span>

<span data-ttu-id="e0bd5-115">Modo RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-115">The RemoteApp mode.</span></span> <span data-ttu-id="e0bd5-116">Si se establece en **Variant \_ true**, el modo RemoteApp está habilitado y la sesión remota hospedará los programas de RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-116">If set to **VARIANT\_TRUE**, RemoteApp mode is enabled, and the remote session will host RemoteApp programs.</span></span> <span data-ttu-id="e0bd5-117">Si se establece en **Variant \_ false** (el valor predeterminado), el modo RemoteApp no está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-117">If set to **VARIANT\_FALSE** (the default), RemoteApp mode is not enabled.</span></span> <span data-ttu-id="e0bd5-118">La sesión remota hospedará un escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-118">The remote session will host a remote desktop.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e0bd5-119">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e0bd5-119">Error codes</span></span>

<span data-ttu-id="e0bd5-120">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="e0bd5-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0bd5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0bd5-121">Requirements</span></span>



| <span data-ttu-id="e0bd5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0bd5-122">Requirement</span></span> | <span data-ttu-id="e0bd5-123">Value</span><span class="sxs-lookup"><span data-stu-id="e0bd5-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0bd5-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0bd5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e0bd5-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0bd5-125">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e0bd5-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0bd5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e0bd5-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0bd5-127">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e0bd5-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e0bd5-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="e0bd5-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0bd5-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e0bd5-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e0bd5-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0bd5-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0bd5-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e0bd5-132">IID</span><span class="sxs-lookup"><span data-stu-id="e0bd5-132">IID</span></span><br/>                      | <span data-ttu-id="e0bd5-133">IID \_ ITSRemoteProgram se define como FDD029F9-467A-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="e0bd5-133">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="e0bd5-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0bd5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0bd5-135">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="e0bd5-135">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> <dt>

[<span data-ttu-id="e0bd5-136">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="e0bd5-136">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="e0bd5-137">**ITSRemoteProgram**</span><span class="sxs-lookup"><span data-stu-id="e0bd5-137">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 





