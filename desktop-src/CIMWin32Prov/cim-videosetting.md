---
description: La \_ clase de Videoconfiguración de CIM asocia el \_ objeto de configuración VIDEOCONTROLLERRESOLUTION de CIM con el controlador al que se aplica.
ms.assetid: 1f6742ad-ab92-4723-b691-0c3e6c0d82fa
ms.tgt_platform: multiple
title: CIM_VideoSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoSetting
- CIM_VideoSetting.Setting
- CIM_VideoSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a37fe8dd03738ae93f391a754caca84564dc6f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659730"
---
# <a name="cim_videosetting-class"></a><span data-ttu-id="d2b81-103">\_Clase de Videoconfiguración de CIM</span><span class="sxs-lookup"><span data-stu-id="d2b81-103">CIM\_VideoSetting class</span></span>

<span data-ttu-id="d2b81-104">La clase de **\_ videoconfiguración de CIM** asocia el objeto de configuración [**\_ VideoControllerResolution de CIM**](cim-videocontrollerresolution.md) con el controlador al que se aplica.</span><span class="sxs-lookup"><span data-stu-id="d2b81-104">The **CIM\_VideoSetting** class associates the [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) setting object with the controller to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d2b81-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="d2b81-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d2b81-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d2b81-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d2b81-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d2b81-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d2b81-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d2b81-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2b81-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2b81-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCEB-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoSetting : CIM_ElementSetting
{
  CIM_VideoControllerResolution REF Setting;
  CIM_VideoController           REF Element;
};
```

## <a name="members"></a><span data-ttu-id="d2b81-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="d2b81-110">Members</span></span>

<span data-ttu-id="d2b81-111">La clase de **\_ videoconfiguración de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d2b81-111">The **CIM\_VideoSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="d2b81-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2b81-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2b81-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2b81-113">Properties</span></span>

<span data-ttu-id="d2b81-114">La clase de **\_ Videoconfiguración de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d2b81-114">The **CIM\_VideoSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2b81-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="d2b81-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2b81-116">Tipo de datos **: \_ videocontroladora CIM**</span><span class="sxs-lookup"><span data-stu-id="d2b81-116">Data type: **CIM\_VideoController**</span></span>
</dt> <dt>

<span data-ttu-id="d2b81-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2b81-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2b81-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span><span class="sxs-lookup"><span data-stu-id="d2b81-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element")</span></span>
</dt> </dl>

<span data-ttu-id="d2b81-119">Un [**\_ videocontrolador de CIM**](cim-videocontroller.md) que describe el controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d2b81-119">A [**CIM\_VideoController**](cim-videocontroller.md) that describes the video controller.</span></span>

</dd> <dt>

<span data-ttu-id="d2b81-120">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="d2b81-120">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2b81-121">Tipo de datos: **CIM \_ VideoControllerResolution**</span><span class="sxs-lookup"><span data-stu-id="d2b81-121">Data type: **CIM\_VideoControllerResolution**</span></span>
</dt> <dt>

<span data-ttu-id="d2b81-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2b81-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2b81-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuración")</span><span class="sxs-lookup"><span data-stu-id="d2b81-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting")</span></span>
</dt> </dl>

<span data-ttu-id="d2b81-124">Un [**\_ VideoControllerResolution de CIM**](cim-videocontrollerresolution.md) que describe las resoluciones, las frecuencias de actualización, el modo de exploración y el número de colores que se pueden establecer para el controlador.</span><span class="sxs-lookup"><span data-stu-id="d2b81-124">A [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) that describes the resolutions, refresh rates, scan mode and number of colors that can be set for the Controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2b81-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2b81-125">Remarks</span></span>

<span data-ttu-id="d2b81-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="d2b81-126">WMI does not implement this class.</span></span> <span data-ttu-id="d2b81-127">Para las clases WMI que se derivan de la **\_ configuración** de VIDEODE CIM, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d2b81-127">For WMI classes derived from **CIM\_VideoSetting**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d2b81-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="d2b81-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d2b81-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="d2b81-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2b81-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2b81-130">Requirements</span></span>



| <span data-ttu-id="d2b81-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2b81-131">Requirement</span></span> | <span data-ttu-id="d2b81-132">Value</span><span class="sxs-lookup"><span data-stu-id="d2b81-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2b81-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2b81-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d2b81-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2b81-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2b81-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2b81-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d2b81-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2b81-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2b81-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d2b81-137">Namespace</span></span><br/>                | <span data-ttu-id="d2b81-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d2b81-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d2b81-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d2b81-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2b81-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2b81-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2b81-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d2b81-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2b81-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2b81-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2b81-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2b81-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2b81-144">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="d2b81-144">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> </dl>

 

