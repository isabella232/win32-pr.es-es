---
title: Método join de la clase Win32_RDMSJoinedNode
description: Agrega un nodo a Escritorio remoto Management Services (RDMS).
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Método de combinación Servicios de Escritorio remoto
- Método join Servicios de Escritorio remoto, clase Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode de clase Servicios de Escritorio remoto, método join
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Join
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587e68758971453e8c4e307ccb37ce6cede262f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422061"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="ae101-106">Método join de la \_ clase Win32 RDMSJoinedNode</span><span class="sxs-lookup"><span data-stu-id="ae101-106">Join method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="ae101-107">Agrega un nodo a Escritorio remoto Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="ae101-107">Adds a node to Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="ae101-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae101-108">Syntax</span></span>


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a><span data-ttu-id="ae101-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae101-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae101-110">*NodeFQDN* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae101-110">*NodeFQDN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae101-111">El nombre de dominio completo del nodo.</span><span class="sxs-lookup"><span data-stu-id="ae101-111">The fully qualified domain name of the node.</span></span>

</dd> <dt>

<span data-ttu-id="ae101-112">*NodeSID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae101-112">*NodeSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae101-113">El identificador de seguridad (SID) del nodo.</span><span class="sxs-lookup"><span data-stu-id="ae101-113">The security identifier (SID) of the node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae101-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae101-114">Return value</span></span>

<span data-ttu-id="ae101-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="ae101-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae101-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae101-116">Requirements</span></span>



| <span data-ttu-id="ae101-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae101-117">Requirement</span></span> | <span data-ttu-id="ae101-118">Value</span><span class="sxs-lookup"><span data-stu-id="ae101-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae101-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae101-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ae101-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ae101-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ae101-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae101-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ae101-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ae101-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="ae101-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ae101-123">Namespace</span></span><br/>                | <span data-ttu-id="ae101-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="ae101-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="ae101-125">MOF</span><span class="sxs-lookup"><span data-stu-id="ae101-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae101-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae101-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae101-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae101-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae101-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae101-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="ae101-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae101-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae101-130">**Win32 \_ RDMSJoinedNode**</span><span class="sxs-lookup"><span data-stu-id="ae101-130">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





