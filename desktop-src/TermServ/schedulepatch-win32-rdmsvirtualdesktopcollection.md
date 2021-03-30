---
title: Método SchedulePatch de la clase Win32_RDMSVirtualDesktopCollection
description: Programa un trabajo de aprovisionamiento de actualizaciones de software que instala las actualizaciones de software en las máquinas virtuales de una colección de escritorios virtuales.
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- Método SchedulePatch Servicios de Escritorio remoto
- Método SchedulePatch Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de clase Servicios de Escritorio remoto, método SchedulePatch
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SchedulePatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9585e3d13ea1f02115506741c153d62c33fcc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490313"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="d7e22-106">Método SchedulePatch de la \_ clase RDMSVirtualDesktopCollection de Win32</span><span class="sxs-lookup"><span data-stu-id="d7e22-106">SchedulePatch method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="d7e22-107">Programa un trabajo de aprovisionamiento de actualizaciones de software que instala las actualizaciones de software en las máquinas virtuales de una colección de escritorios virtuales.</span><span class="sxs-lookup"><span data-stu-id="d7e22-107">Schedules a software update provisioning job that installs software updates on the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7e22-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7e22-108">Syntax</span></span>


```mof
uint32 SchedulePatch(
  [in] DATETIME StartTime,
  [in] DATETIME ForceLogOffTime,
  [in] string   JobInputXml
);
```



## <a name="parameters"></a><span data-ttu-id="d7e22-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7e22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7e22-110">*StartTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7e22-110">*StartTime* \[in\]</span></span>
</dt> <dd>

> [!Note]  
> <span data-ttu-id="d7e22-111">El sistema no cerrará la sesión de los usuarios de las máquinas virtuales hasta la hora especificada en el parámetro *ForceLogOffTime* .</span><span class="sxs-lookup"><span data-stu-id="d7e22-111">The system will not log off users of the virtual machines until the time specified in the *ForceLogOffTime* parameter.</span></span>

 

<span data-ttu-id="d7e22-112">Fecha y hora de instalación de las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="d7e22-112">The date and time to install the updates.</span></span>

</dd> <dt>

<span data-ttu-id="d7e22-113">*ForceLogOffTime* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7e22-113">*ForceLogOffTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7e22-114">Fecha y hora en que el sistema cerrará la sesión de los usuarios de las máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="d7e22-114">The date and time on which the system will log off users of the virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="d7e22-115">*JobInputXml* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7e22-115">*JobInputXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7e22-116">Cadena con formato XML que contiene la información del trabajo de actualización de software.</span><span class="sxs-lookup"><span data-stu-id="d7e22-116">An XML formatted string that contains the software update job information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7e22-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7e22-117">Return value</span></span>

<span data-ttu-id="d7e22-118">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.</span><span class="sxs-lookup"><span data-stu-id="d7e22-118">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7e22-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7e22-119">Requirements</span></span>



| <span data-ttu-id="d7e22-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7e22-120">Requirement</span></span> | <span data-ttu-id="d7e22-121">Value</span><span class="sxs-lookup"><span data-stu-id="d7e22-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7e22-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7e22-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d7e22-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d7e22-123">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="d7e22-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7e22-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d7e22-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d7e22-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="d7e22-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d7e22-126">Namespace</span></span><br/>                | <span data-ttu-id="d7e22-127">RDMs raíz de \\ CIMv2 \\</span><span class="sxs-lookup"><span data-stu-id="d7e22-127">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="d7e22-128">MOF</span><span class="sxs-lookup"><span data-stu-id="d7e22-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7e22-129"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7e22-129"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="d7e22-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7e22-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7e22-131"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7e22-131"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="d7e22-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7e22-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7e22-133">**Win32 \_ RDMSVirtualDesktopCollection**</span><span class="sxs-lookup"><span data-stu-id="d7e22-133">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





