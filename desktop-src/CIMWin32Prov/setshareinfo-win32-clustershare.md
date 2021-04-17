---
description: Establece los parámetros del recurso compartido.
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: Método SetShareInfo de la clase Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bda6fe36d1168045ea9f8d331ff334920ed1dd19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659751"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a><span data-ttu-id="a1650-103">Método SetShareInfo de la \_ clase ClusterShare de Win32</span><span class="sxs-lookup"><span data-stu-id="a1650-103">SetShareInfo method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="a1650-104">Establece los parámetros del recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="a1650-104">Sets the parameters of the shared resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1650-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1650-105">Syntax</span></span>


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="a1650-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1650-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1650-107">*MaximumAllowed* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a1650-107">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a1650-108">Límite en el número máximo de usuarios a los que se les permite usar este recurso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="a1650-108">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="a1650-109">*Descripción* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a1650-109">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a1650-110">Describe el recurso que se comparte.</span><span class="sxs-lookup"><span data-stu-id="a1650-110">Describes the resource being shared.</span></span>

</dd> <dt>

<span data-ttu-id="a1650-111">*Acceso a* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a1650-111">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a1650-112">Descriptor de seguridad para permisos de nivel de usuario.</span><span class="sxs-lookup"><span data-stu-id="a1650-112">Security descriptor for user-level permissions.</span></span> <span data-ttu-id="a1650-113">Un descriptor de seguridad contiene información sobre el permiso, el propietario y las capacidades de acceso del recurso.</span><span class="sxs-lookup"><span data-stu-id="a1650-113">A security descriptor contains information about the permission, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="a1650-114">Para obtener más información, [**vea \_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="a1650-114">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1650-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1650-115">Requirements</span></span>



| <span data-ttu-id="a1650-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1650-116">Requirement</span></span> | <span data-ttu-id="a1650-117">Value</span><span class="sxs-lookup"><span data-stu-id="a1650-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1650-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1650-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a1650-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a1650-119">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="a1650-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1650-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a1650-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a1650-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a1650-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a1650-122">Namespace</span></span><br/>                | <span data-ttu-id="a1650-123">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a1650-123">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a1650-124">MOF</span><span class="sxs-lookup"><span data-stu-id="a1650-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1650-125"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1650-125"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1650-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a1650-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1650-127"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1650-127"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1650-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1650-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1650-129">**Win32 \_ ClusterShare**</span><span class="sxs-lookup"><span data-stu-id="a1650-129">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

