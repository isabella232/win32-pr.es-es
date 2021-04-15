---
title: Método SetUserAssignment de la clase Win32_RDMSVirtualDesktop
description: Asigna un escritorio virtual a un usuario.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- Método SetUserAssignment Servicios de Escritorio remoto
- Método SetUserAssignment Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de clase Servicios de Escritorio remoto, método SetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f02e1cc935e344edd6a9c52016052e082e08d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676925"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="5af17-106">Método SetUserAssignment de la \_ clase RDMSVirtualDesktop de Win32</span><span class="sxs-lookup"><span data-stu-id="5af17-106">SetUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="5af17-107">Asigna un escritorio virtual a un usuario.</span><span class="sxs-lookup"><span data-stu-id="5af17-107">Assigns a virtual desktop to a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="5af17-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5af17-108">Syntax</span></span>


```mof
uint32 SetUserAssignment(
  [in] string UserName,
  [in] string UserDomain
);
```



## <a name="parameters"></a><span data-ttu-id="5af17-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5af17-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5af17-110">*Nombre de usuario* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5af17-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5af17-111">Nombre de usuario del usuario.</span><span class="sxs-lookup"><span data-stu-id="5af17-111">The username of the user.</span></span>

</dd> <dt>

<span data-ttu-id="5af17-112">*UserDomain* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5af17-112">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5af17-113">El nombre de dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="5af17-113">The domain name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5af17-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5af17-114">Return value</span></span>

<span data-ttu-id="5af17-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="5af17-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5af17-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5af17-116">Requirements</span></span>



| <span data-ttu-id="5af17-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5af17-117">Requirement</span></span> | <span data-ttu-id="5af17-118">Value</span><span class="sxs-lookup"><span data-stu-id="5af17-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5af17-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5af17-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5af17-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5af17-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5af17-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5af17-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5af17-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5af17-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5af17-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5af17-123">Namespace</span></span><br/>                | <span data-ttu-id="5af17-124">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="5af17-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5af17-125">MOF</span><span class="sxs-lookup"><span data-stu-id="5af17-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5af17-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5af17-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5af17-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5af17-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5af17-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5af17-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5af17-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5af17-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af17-130">**Win32 \_ RDMSVirtualDesktop**</span><span class="sxs-lookup"><span data-stu-id="5af17-130">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





