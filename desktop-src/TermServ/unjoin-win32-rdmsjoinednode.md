---
title: Método unjoin de la clase Win32_RDMSJoinedNode
description: Quita un nodo de los servicios de administración de Escritorio remoto (RDMS).
ms.assetid: 37c462f4-a19d-4b85-8fac-2735deb7c04f
ms.tgt_platform: multiple
keywords:
- Unjoin (método) Servicios de Escritorio remoto
- Método unjoin Servicios de Escritorio remoto, clase Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode de clase Servicios de Escritorio remoto, unjoin (método)
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Unjoin
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 234f7cc3ad8a797fff51661528f4545ed9fea3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685998"
---
# <a name="unjoin-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="cb3ae-106">Método unjoin de la \_ clase Win32 RDMSJoinedNode</span><span class="sxs-lookup"><span data-stu-id="cb3ae-106">Unjoin method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="cb3ae-107">Quita un nodo de los servicios de administración de Escritorio remoto (RDMS).</span><span class="sxs-lookup"><span data-stu-id="cb3ae-107">Removes a node from Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3ae-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb3ae-108">Syntax</span></span>


```mof
uint32 Unjoin();
```



## <a name="parameters"></a><span data-ttu-id="cb3ae-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb3ae-109">Parameters</span></span>

<span data-ttu-id="cb3ae-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cb3ae-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb3ae-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb3ae-111">Return value</span></span>

<span data-ttu-id="cb3ae-112">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="cb3ae-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb3ae-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb3ae-113">Requirements</span></span>



| <span data-ttu-id="cb3ae-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb3ae-114">Requirement</span></span> | <span data-ttu-id="cb3ae-115">Value</span><span class="sxs-lookup"><span data-stu-id="cb3ae-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3ae-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb3ae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cb3ae-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cb3ae-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="cb3ae-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb3ae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cb3ae-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cb3ae-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="cb3ae-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cb3ae-120">Namespace</span></span><br/>                | <span data-ttu-id="cb3ae-121">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="cb3ae-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="cb3ae-122">MOF</span><span class="sxs-lookup"><span data-stu-id="cb3ae-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb3ae-123"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb3ae-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb3ae-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb3ae-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb3ae-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb3ae-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="cb3ae-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb3ae-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3ae-127">**Win32 \_ RDMSJoinedNode**</span><span class="sxs-lookup"><span data-stu-id="cb3ae-127">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





