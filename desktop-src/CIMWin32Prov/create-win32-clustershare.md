---
description: Crea una nueva instancia de ClusterShare de Win32 \_ .
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Método Create de la clase Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cbf7c42b8523bcd12b19e9b474ecc50bd031939
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153512"
---
# <a name="create-method-of-the-win32_clustershare-class"></a><span data-ttu-id="fb930-103">Método Create de la \_ clase Win32 ClusterShare</span><span class="sxs-lookup"><span data-stu-id="fb930-103">Create method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="fb930-104">Crea una nueva instancia de [**\_ ClusterShare de Win32**](win32-clustershare.md) .</span><span class="sxs-lookup"><span data-stu-id="fb930-104">Creates a new [**Win32\_ClusterShare**](win32-clustershare.md) instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb930-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb930-105">Syntax</span></span>


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="fb930-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb930-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb930-107">*Ruta de acceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb930-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb930-108">Ruta de acceso local del recurso compartido de Windows.</span><span class="sxs-lookup"><span data-stu-id="fb930-108">Local path of the Windows share.</span></span>

<span data-ttu-id="fb930-109">Ejemplo, "C: \\ archivos de programa".</span><span class="sxs-lookup"><span data-stu-id="fb930-109">Example, "C:\\Program Files".</span></span>

</dd> <dt>

<span data-ttu-id="fb930-110">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fb930-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb930-111">El alias de una ruta de acceso configurada como un recurso compartido en un equipo con Windows.</span><span class="sxs-lookup"><span data-stu-id="fb930-111">The alias to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="fb930-112">Ejemplo, "Public".</span><span class="sxs-lookup"><span data-stu-id="fb930-112">Example, "public".</span></span>

</dd> <dt>

<span data-ttu-id="fb930-113">*Tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="fb930-113">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb930-114">Tipo de recurso que se va a compartir.</span><span class="sxs-lookup"><span data-stu-id="fb930-114">Type of resource being shared.</span></span> <span data-ttu-id="fb930-115">Entre los tipos se incluyen las unidades de disco, las colas de impresión, las comunicaciones entre procesos (IPC) y los dispositivos generales.</span><span class="sxs-lookup"><span data-stu-id="fb930-115">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<dt>

<span data-ttu-id="fb930-116">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="fb930-116">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="fb930-117">Unidad de disco</span><span class="sxs-lookup"><span data-stu-id="fb930-117">Disk Drive</span></span>

</dd> <dt>

<span data-ttu-id="fb930-118">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="fb930-118">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="fb930-119">Cola de impresión</span><span class="sxs-lookup"><span data-stu-id="fb930-119">Print Queue</span></span>

</dd> <dt>

<span data-ttu-id="fb930-120">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="fb930-120">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="fb930-121">Dispositivo</span><span class="sxs-lookup"><span data-stu-id="fb930-121">Device</span></span>

</dd> <dt>

<span data-ttu-id="fb930-122">3 (0X3)</span><span class="sxs-lookup"><span data-stu-id="fb930-122">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="fb930-123">IPC</span><span class="sxs-lookup"><span data-stu-id="fb930-123">IPC</span></span>

</dd> <dt>

<span data-ttu-id="fb930-124">2147483648 (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="fb930-124">2147483648 (0x80000000)</span></span>
</dt> <dd>

<span data-ttu-id="fb930-125">Administrador de unidad de disco</span><span class="sxs-lookup"><span data-stu-id="fb930-125">Disk Drive Admin</span></span>

</dd> <dt>

<span data-ttu-id="fb930-126">2147483649 (0x80000001)</span><span class="sxs-lookup"><span data-stu-id="fb930-126">2147483649 (0x80000001)</span></span>
</dt> <dd>

<span data-ttu-id="fb930-127">Administrador de cola de impresión</span><span class="sxs-lookup"><span data-stu-id="fb930-127">Print Queue Admin</span></span>

</dd> <dt>

<span data-ttu-id="fb930-128">2147483650 (0x80000002)</span><span class="sxs-lookup"><span data-stu-id="fb930-128">2147483650 (0x80000002)</span></span>
</dt> <dd>

<span data-ttu-id="fb930-129">Administrador de dispositivos</span><span class="sxs-lookup"><span data-stu-id="fb930-129">Device Admin</span></span>

</dd> <dt>

<span data-ttu-id="fb930-130">2147483651 (0x80000003)</span><span class="sxs-lookup"><span data-stu-id="fb930-130">2147483651 (0x80000003)</span></span>
</dt> <dd>

<span data-ttu-id="fb930-131">Administración de IPC</span><span class="sxs-lookup"><span data-stu-id="fb930-131">IPC Admin</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fb930-132">*MaximumAllowed* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="fb930-132">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fb930-133">Límite en el número máximo de usuarios a los que se les permite usar este recurso al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="fb930-133">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="fb930-134">*Descripción* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="fb930-134">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fb930-135">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="fb930-135">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="fb930-136">*Contraseña* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="fb930-136">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fb930-137">TBD</span><span class="sxs-lookup"><span data-stu-id="fb930-137">TBD</span></span>

</dd> <dt>

<span data-ttu-id="fb930-138">*Acceso a* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="fb930-138">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fb930-139">Instancia integrada opcional de una [**clase \_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) que contiene el descriptor de seguridad para el nuevo recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="fb930-139">Optional embedded instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class that contains the security descriptor for the new share.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb930-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb930-140">Requirements</span></span>



| <span data-ttu-id="fb930-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb930-141">Requirement</span></span> | <span data-ttu-id="fb930-142">Value</span><span class="sxs-lookup"><span data-stu-id="fb930-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb930-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb930-143">Minimum supported client</span></span><br/> | <span data-ttu-id="fb930-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fb930-144">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="fb930-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb930-145">Minimum supported server</span></span><br/> | <span data-ttu-id="fb930-146">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fb930-146">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="fb930-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fb930-147">Namespace</span></span><br/>                | <span data-ttu-id="fb930-148">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fb930-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fb930-149">MOF</span><span class="sxs-lookup"><span data-stu-id="fb930-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb930-150"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb930-150"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb930-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb930-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb930-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb930-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb930-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb930-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb930-154">**Win32 \_ ClusterShare**</span><span class="sxs-lookup"><span data-stu-id="fb930-154">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

