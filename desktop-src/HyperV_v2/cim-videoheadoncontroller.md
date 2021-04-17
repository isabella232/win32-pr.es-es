---
description: Asocia un encabezado de vídeo con el adaptador de vídeo que lo contiene.
ms.assetid: d15f4350-1529-4246-9ea2-8453e52516c6
title: CIM_VideoHeadOnController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHeadOnController
- CIM_VideoHeadOnController.Antecedent
- CIM_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18178e6d9d7f1e684af1d4fe74336e1f2a02eedc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666900"
---
# <a name="cim_videoheadoncontroller-class"></a><span data-ttu-id="a1b05-103">\_Clase VideoHeadOnController de CIM</span><span class="sxs-lookup"><span data-stu-id="a1b05-103">CIM\_VideoHeadOnController class</span></span>

<span data-ttu-id="a1b05-104">Asocia un encabezado de vídeo con el adaptador de vídeo que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="a1b05-104">Associates a video head with the video adapter that contains it.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1b05-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1b05-105">Syntax</span></span>

``` syntax
[Association, Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHeadOnController : CIM_HostedDependency
{
  CIM_DisplayController REF Antecedent;
  CIM_VideoHead         REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="a1b05-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1b05-106">Members</span></span>

<span data-ttu-id="a1b05-107">La clase **CIM \_ VideoHeadOnController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a1b05-107">The **CIM\_VideoHeadOnController** class has these types of members:</span></span>

-   [<span data-ttu-id="a1b05-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1b05-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1b05-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a1b05-109">Properties</span></span>

<span data-ttu-id="a1b05-110">La clase **CIM \_ VideoHeadOnController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a1b05-110">The **CIM\_VideoHeadOnController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1b05-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="a1b05-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1b05-112">Tipo de datos: **CIM \_ DisplayController**</span><span class="sxs-lookup"><span data-stu-id="a1b05-112">Data type: **CIM\_DisplayController**</span></span>
</dt> <dt>

<span data-ttu-id="a1b05-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a1b05-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1b05-114">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="a1b05-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="a1b05-115">Adaptador de vídeo que incluye el encabezado.</span><span class="sxs-lookup"><span data-stu-id="a1b05-115">The video adapter that includes the head.</span></span>

</dd> <dt>

<span data-ttu-id="a1b05-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="a1b05-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1b05-117">Tipo de datos **: \_ Videopartida CIM**</span><span class="sxs-lookup"><span data-stu-id="a1b05-117">Data type: **CIM\_VideoHead**</span></span>
</dt> <dt>

<span data-ttu-id="a1b05-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a1b05-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1b05-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="a1b05-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="a1b05-120">El encabezado del adaptador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a1b05-120">The head on the video adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1b05-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1b05-121">Requirements</span></span>



| <span data-ttu-id="a1b05-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1b05-122">Requirement</span></span> | <span data-ttu-id="a1b05-123">Value</span><span class="sxs-lookup"><span data-stu-id="a1b05-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b05-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1b05-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a1b05-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a1b05-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a1b05-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1b05-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a1b05-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1b05-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a1b05-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a1b05-128">Namespace</span></span><br/>                | <span data-ttu-id="a1b05-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a1b05-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a1b05-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a1b05-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1b05-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1b05-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1b05-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a1b05-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1b05-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a1b05-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a1b05-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1b05-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b05-135">**\_HOSTEDDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="a1b05-135">**CIM\_HostedDependency**</span></span>](cim-hosteddependency.md)
</dt> </dl>

 

