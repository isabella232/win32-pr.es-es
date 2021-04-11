---
description: Asocia un cabezal de vídeo al controlador de vídeo que lo incluye.
ms.assetid: D072DF7C-D55B-4203-9FE5-B395D1EC1632
title: Msvm_VideoHeadOnController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHeadOnController
- Msvm_VideoHeadOnController.Antecedent
- Msvm_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 11065c7b7a9e23b786697c3d4f0dbd63e67d6b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156365"
---
# <a name="msvm_videoheadoncontroller-class"></a><span data-ttu-id="bfeba-103">MSVM \_ VideoHeadOnController (clase)</span><span class="sxs-lookup"><span data-stu-id="bfeba-103">Msvm\_VideoHeadOnController class</span></span>

<span data-ttu-id="bfeba-104">Asocia un cabezal de vídeo al controlador de vídeo que lo incluye.</span><span class="sxs-lookup"><span data-stu-id="bfeba-104">Associates a video head with the video controller that includes it.</span></span>

<span data-ttu-id="bfeba-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="bfeba-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfeba-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfeba-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHeadOnController : CIM_VideoHeadOnController
{
  CIM_DisplayController REF Antecedent;
  Msvm_VideoHead        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="bfeba-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bfeba-107">Members</span></span>

<span data-ttu-id="bfeba-108">La clase **MSVM \_ VideoHeadOnController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bfeba-108">The **Msvm\_VideoHeadOnController** class has these types of members:</span></span>

-   [<span data-ttu-id="bfeba-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bfeba-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bfeba-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bfeba-110">Properties</span></span>

<span data-ttu-id="bfeba-111">La clase **MSVM \_ VideoHeadOnController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bfeba-111">The **Msvm\_VideoHeadOnController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bfeba-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="bfeba-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfeba-113">Tipo de datos: **[ **CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="bfeba-113">Data type: **[**CIM\_DisplayController**](/previous-versions//cc136810(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="bfeba-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfeba-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfeba-115">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="bfeba-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="bfeba-116">El controlador de vídeo que incluye el encabezado.</span><span class="sxs-lookup"><span data-stu-id="bfeba-116">The video controller that includes the head.</span></span>

</dd> <dt>

<span data-ttu-id="bfeba-117">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="bfeba-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfeba-118">Tipo de datos: **[ **MSVM \_ videohead**](msvm-videohead.md)**</span><span class="sxs-lookup"><span data-stu-id="bfeba-118">Data type: **[**Msvm\_VideoHead**](msvm-videohead.md)**</span></span>
</dt> <dt>

<span data-ttu-id="bfeba-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfeba-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfeba-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="bfeba-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="bfeba-121">El encabezado del dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bfeba-121">The head on the video device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfeba-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfeba-122">Remarks</span></span>

<span data-ttu-id="bfeba-123">El acceso a la clase **MSVM \_ VideoHeadOnController** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="bfeba-123">Access to the **Msvm\_VideoHeadOnController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bfeba-124">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bfeba-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfeba-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfeba-125">Requirements</span></span>



| <span data-ttu-id="bfeba-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfeba-126">Requirement</span></span> | <span data-ttu-id="bfeba-127">Value</span><span class="sxs-lookup"><span data-stu-id="bfeba-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfeba-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfeba-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bfeba-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="bfeba-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bfeba-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfeba-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bfeba-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="bfeba-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bfeba-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bfeba-132">Namespace</span></span><br/>                | <span data-ttu-id="bfeba-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bfeba-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bfeba-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bfeba-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfeba-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfeba-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfeba-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bfeba-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfeba-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bfeba-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bfeba-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfeba-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfeba-139">**\_VIDEOHEADONCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="bfeba-139">**CIM\_VideoHeadOnController**</span></span>](cim-videoheadoncontroller.md)
</dt> <dt>

<span data-ttu-id="bfeba-140">[**\_VIDEOHEADONCONTROLLER CIM**](/previous-versions//cc136950(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bfeba-140">[**CIM\_VideoHeadOnController**](/previous-versions//cc136950(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="bfeba-141">Clases de vídeo</span><span class="sxs-lookup"><span data-stu-id="bfeba-141">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

