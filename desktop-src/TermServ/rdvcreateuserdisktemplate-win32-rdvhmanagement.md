---
title: Método RdvCreateUserDiskTemplate de la clase Win32_RdvhManagement
description: Crea una plantilla de disco de usuario, con el tamaño máximo especificado, en la ubicación especificada.
ms.assetid: b8ca8b8c-58fd-44fc-9a88-5d7d41ef96a2
ms.tgt_platform: multiple
keywords:
- Método RdvCreateUserDiskTemplate Servicios de Escritorio remoto
- Método RdvCreateUserDiskTemplate Servicios de Escritorio remoto, clase Win32_RdvhManagement
- Win32_RdvhManagement de clase Servicios de Escritorio remoto, método RdvCreateUserDiskTemplate
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCreateUserDiskTemplate
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdc7fec869fa4ffde9ac0a5a724f73b04b84351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803614"
---
# <a name="rdvcreateuserdisktemplate-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="a8f27-106">Método RdvCreateUserDiskTemplate de la \_ clase RdvhManagement de Win32</span><span class="sxs-lookup"><span data-stu-id="a8f27-106">RdvCreateUserDiskTemplate method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="a8f27-107">Crea una plantilla de disco de usuario, con el tamaño máximo especificado, en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="a8f27-107">Creates a user disk template, with the specified maximum size, at the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f27-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8f27-108">Syntax</span></span>


```mof
uint32 RdvCreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a><span data-ttu-id="a8f27-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8f27-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f27-110">*UserDisksStorageUrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a8f27-110">*UserDisksStorageUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f27-111">Ubicación del almacenamiento en disco del usuario.</span><span class="sxs-lookup"><span data-stu-id="a8f27-111">Location of the user disk storage.</span></span>

</dd> <dt>

<span data-ttu-id="a8f27-112">*UserDiskMaxSizeInGB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a8f27-112">*UserDiskMaxSizeInGB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f27-113">Tamaño máximo del disco de usuario, en GB.</span><span class="sxs-lookup"><span data-stu-id="a8f27-113">Maximum size of the user disk, in GB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f27-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8f27-114">Return value</span></span>

<span data-ttu-id="a8f27-115">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="a8f27-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a8f27-116">Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a8f27-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f27-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8f27-117">Remarks</span></span>

<span data-ttu-id="a8f27-118">Todos los discos de usuario creados con esta plantilla tendrán el mismo tamaño máximo que la plantilla.</span><span class="sxs-lookup"><span data-stu-id="a8f27-118">All user disks created using this template will have the same maximum size as the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f27-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8f27-119">Requirements</span></span>



| <span data-ttu-id="a8f27-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8f27-120">Requirement</span></span> | <span data-ttu-id="a8f27-121">Value</span><span class="sxs-lookup"><span data-stu-id="a8f27-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f27-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8f27-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a8f27-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a8f27-123">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="a8f27-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8f27-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a8f27-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a8f27-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="a8f27-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a8f27-126">Namespace</span></span><br/>                | <span data-ttu-id="a8f27-127">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a8f27-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="a8f27-128">MOF</span><span class="sxs-lookup"><span data-stu-id="a8f27-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8f27-129"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8f27-129"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="a8f27-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8f27-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8f27-131"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8f27-131"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8f27-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8f27-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f27-133">**Win32 \_ RdvhManagement**</span><span class="sxs-lookup"><span data-stu-id="a8f27-133">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





