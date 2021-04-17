---
title: Método GetJoinedNodeCount de la clase Win32_RDMSJoinedNode
description: Obtiene el número de servidores que tienen instalados los roles especificados.
ms.assetid: ed2ae0b5-5cbc-4c11-a2ad-065f88dd5842
ms.tgt_platform: multiple
keywords:
- Método GetJoinedNodeCount Servicios de Escritorio remoto
- Método GetJoinedNodeCount Servicios de Escritorio remoto, clase Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode de clase Servicios de Escritorio remoto, método GetJoinedNodeCount
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.GetJoinedNodeCount
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ecc5c388814873aa690e9af5adda5081aad4d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676709"
---
# <a name="getjoinednodecount-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="c3441-106">Método GetJoinedNodeCount de la \_ clase RDMSJoinedNode de Win32</span><span class="sxs-lookup"><span data-stu-id="c3441-106">GetJoinedNodeCount method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="c3441-107">Obtiene el número de servidores que tienen instalados los roles especificados.</span><span class="sxs-lookup"><span data-stu-id="c3441-107">Get number of servers that have the specified roles installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3441-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3441-108">Syntax</span></span>


```mof
uint32 GetJoinedNodeCount(
  [in]  uint32 roleType,
  [out] uint32 Count
);
```



## <a name="parameters"></a><span data-ttu-id="c3441-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3441-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3441-110">*roleType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c3441-110">*roleType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3441-111">Un campo de bits que especifica los tipos de rol.</span><span class="sxs-lookup"><span data-stu-id="c3441-111">A bitfield that specifies the role types.</span></span>

<dt>

<span data-ttu-id="c3441-112">0</span><span class="sxs-lookup"><span data-stu-id="c3441-112">0</span></span>
</dt> <dd>

<span data-ttu-id="c3441-113">Todo</span><span class="sxs-lookup"><span data-stu-id="c3441-113">All</span></span>

</dd> <dt>

<span data-ttu-id="c3441-114">1</span><span class="sxs-lookup"><span data-stu-id="c3441-114">1</span></span>
</dt> <dd>

<span data-ttu-id="c3441-115">Conexión a Escritorio remoto Broker (RDCB)</span><span class="sxs-lookup"><span data-stu-id="c3441-115">Remote Desktop Connection Broker (RDCB)</span></span>

</dd> <dt>

<span data-ttu-id="c3441-116">2</span><span class="sxs-lookup"><span data-stu-id="c3441-116">2</span></span>
</dt> <dd>

<span data-ttu-id="c3441-117">Host de sesión de Escritorio remoto (RDSH)</span><span class="sxs-lookup"><span data-stu-id="c3441-117">Remote Desktop Session Host (RDSH)</span></span>

</dd> <dt>

<span data-ttu-id="c3441-118">4</span><span class="sxs-lookup"><span data-stu-id="c3441-118">4</span></span>
</dt> <dd>

<span data-ttu-id="c3441-119">Host de virtualización de Escritorio remoto (RDVH)</span><span class="sxs-lookup"><span data-stu-id="c3441-119">Remote Desktop Virtualization Host (RDVH)</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c3441-120">*Recuento* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c3441-120">*Count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3441-121">Si se ejecuta correctamente, devuelve el número de servidores con los roles especificados instalados.</span><span class="sxs-lookup"><span data-stu-id="c3441-121">On success, returns the number of servers with the specified roles installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3441-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3441-122">Return value</span></span>

<span data-ttu-id="c3441-123">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="c3441-123">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3441-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3441-124">Requirements</span></span>



| <span data-ttu-id="c3441-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3441-125">Requirement</span></span> | <span data-ttu-id="c3441-126">Value</span><span class="sxs-lookup"><span data-stu-id="c3441-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3441-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3441-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c3441-128">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c3441-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c3441-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3441-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c3441-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c3441-130">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="c3441-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c3441-131">Namespace</span></span><br/>                | <span data-ttu-id="c3441-132">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="c3441-132">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c3441-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c3441-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3441-134"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3441-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3441-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c3441-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3441-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3441-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c3441-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3441-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3441-138">**Win32 \_ RDMSJoinedNode**</span><span class="sxs-lookup"><span data-stu-id="c3441-138">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





