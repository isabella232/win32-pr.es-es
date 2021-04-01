---
title: Método QueryOfflineInformation de la clase Win32_TSVm
description: Recupera las propiedades del servidor de escritorio virtual (VDS) actual, pero solo cuando el servidor está sin conexión.
ms.assetid: f6ce74cb-a4a4-4e05-a0a7-bac0b7f52c45
ms.tgt_platform: multiple
keywords:
- Método QueryOfflineInformation Servicios de Escritorio remoto
- Método QueryOfflineInformation Servicios de Escritorio remoto, clase Win32_TSVm
- Win32_TSVm de clase Servicios de Escritorio remoto, método QueryOfflineInformation
topic_type:
- apiref
api_name:
- Win32_TSVm.QueryOfflineInformation
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4750ebdb82b08ae1ed0350e1ac448d9aca4003b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905380"
---
# <a name="queryofflineinformation-method-of-the-win32_tsvm-class"></a><span data-ttu-id="6efd0-106">Método QueryOfflineInformation de la \_ clase TSVm de Win32</span><span class="sxs-lookup"><span data-stu-id="6efd0-106">QueryOfflineInformation method of the Win32\_TSVm class</span></span>

<span data-ttu-id="6efd0-107">Recupera las propiedades del servidor de escritorio virtual (VDS) actual, pero solo cuando el servidor está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="6efd0-107">Retrieves the properties of the current virtual desktop server (VDS), but only when the server is offline.</span></span>

## <a name="syntax"></a><span data-ttu-id="6efd0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6efd0-108">Syntax</span></span>


```mof
uint32 QueryOfflineInformation(
  [out] string  Build,
  [out] string  CurrentVersion,
  [out] string  InstallationType,
  [out] string  EditionId,
  [out] string  SysPrepImageState,
  [out] string  SysPrepMode,
  [out] sint32  ProcArch,
  [out] boolean fIsVmbusCapable,
  [out] boolean fIsRdvIcInstalled
);
```



## <a name="parameters"></a><span data-ttu-id="6efd0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6efd0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6efd0-110">*Compilación* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6efd0-110">*Build* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6efd0-111">Si se ejecuta correctamente, devuelve la versión de compilación de VDS.</span><span class="sxs-lookup"><span data-stu-id="6efd0-111">On a success, returns the build version of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="6efd0-112">*CurrentVersion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6efd0-112">*CurrentVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6efd0-113">Si se ejecuta correctamente, devuelve la versión actual de VDS.</span><span class="sxs-lookup"><span data-stu-id="6efd0-113">On a success, returns the current version of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="6efd0-114">*InstallationType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6efd0-114">*InstallationType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6efd0-115">Si se ejecuta correctamente, devuelve el tipo de instalación de VDS.</span><span class="sxs-lookup"><span data-stu-id="6efd0-115">On a success, returns the installation type of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="6efd0-116">*EditionId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6efd0-116">*EditionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6efd0-117">Si se ejecuta correctamente, devuelve el ID. de edición del VDS.</span><span class="sxs-lookup"><span data-stu-id="6efd0-117">On a success, returns the edition ID of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="6efd0-118">*SysPrepImageState* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6efd0-118">*SysPrepImageState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6efd0-119">Si se ejecuta correctamente, devuelve el estado de la imagen de preparación del sistema de VDS.</span><span class="sxs-lookup"><span data-stu-id="6efd0-119">On success, returns the system prep image state of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="6efd0-120">*SysPrepMode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6efd0-120">*SysPrepMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6efd0-121">Si se ejecuta correctamente, devuelve el modo de preparación del sistema del VDS.</span><span class="sxs-lookup"><span data-stu-id="6efd0-121">On a success, returns the system prep mode of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="6efd0-122">*ProcArch* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6efd0-122">*ProcArch* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6efd0-123">Si se ejecuta correctamente, devuelve un valor que indica la arquitectura del procesador.</span><span class="sxs-lookup"><span data-stu-id="6efd0-123">On a success, returns a value indicating the processor architecture.</span></span>

<dt>

<span data-ttu-id="6efd0-124">0</span><span class="sxs-lookup"><span data-stu-id="6efd0-124">0</span></span>
</dt> <dd>

<span data-ttu-id="6efd0-125">x86</span><span class="sxs-lookup"><span data-stu-id="6efd0-125">x86</span></span>

</dd> <dt>

<span data-ttu-id="6efd0-126">1</span><span class="sxs-lookup"><span data-stu-id="6efd0-126">1</span></span>
</dt> <dd>

<span data-ttu-id="6efd0-127">AMD64</span><span class="sxs-lookup"><span data-stu-id="6efd0-127">amd64</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6efd0-128">*fIsVmbusCapable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6efd0-128">*fIsVmbusCapable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6efd0-129">Si se realiza correctamente, indica si el sistema es compatible con VMBus.</span><span class="sxs-lookup"><span data-stu-id="6efd0-129">on a success, indicates whether the system is VMBus-capable.</span></span>

</dd> <dt>

<span data-ttu-id="6efd0-130">*fIsRdvIcInstalled* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6efd0-130">*fIsRdvIcInstalled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6efd0-131">Si se realiza correctamente, indica si RDVIC está instalado.</span><span class="sxs-lookup"><span data-stu-id="6efd0-131">On a success, indicates if RDVIC is installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6efd0-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6efd0-132">Return value</span></span>

<span data-ttu-id="6efd0-133">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="6efd0-133">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="6efd0-134">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="6efd0-134">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="6efd0-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6efd0-135">Requirements</span></span>



| <span data-ttu-id="6efd0-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="6efd0-136">Requirement</span></span> | <span data-ttu-id="6efd0-137">Value</span><span class="sxs-lookup"><span data-stu-id="6efd0-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6efd0-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6efd0-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6efd0-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6efd0-139">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="6efd0-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6efd0-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6efd0-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6efd0-141">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="6efd0-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6efd0-142">Namespace</span></span><br/>                | <span data-ttu-id="6efd0-143">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="6efd0-143">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="6efd0-144">MOF</span><span class="sxs-lookup"><span data-stu-id="6efd0-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6efd0-145"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6efd0-145"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="6efd0-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6efd0-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6efd0-147"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6efd0-147"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6efd0-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="6efd0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6efd0-149">**Win32 \_ TSVm**</span><span class="sxs-lookup"><span data-stu-id="6efd0-149">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





