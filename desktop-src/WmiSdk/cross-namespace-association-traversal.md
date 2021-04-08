---
description: A partir de Windows 7, Instrumental de administración de Windows (WMI) implementa un mecanismo estándar para detectar perfiles mediante el esquema CIM.
ms.assetid: e748b623-5ff3-464d-ba09-96cf226de7b6
ms.tgt_platform: multiple
title: Cruce seguro de la asociación entre espacios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe2bbb408c4d89a7093adf45f3daf276df294ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908680"
---
# <a name="cross-namespace-association-traversal"></a><span data-ttu-id="e4887-103">Cruce seguro de la asociación entre espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="e4887-103">Cross-Namespace Association Traversal</span></span>

<span data-ttu-id="e4887-104">A partir de Windows 7, Instrumental de administración de Windows (WMI) implementa un mecanismo estándar para detectar perfiles mediante el esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="e4887-104">Starting in Windows 7, Windows Management Instrumentation (WMI) implemented a standard mechanism for discovering profiles by using the CIM schema.</span></span>

<span data-ttu-id="e4887-105">WMI admite el registro transversal de asociación entre espacios de nombres y el perfil de asociación.</span><span class="sxs-lookup"><span data-stu-id="e4887-105">WMI supports the cross-namespace association traversal and association profile registration.</span></span> <span data-ttu-id="e4887-106">Para obtener más información sobre el registro de perfiles y la implementación estándar de CIM de cruce seguro de la asociación, vea DSP1033 ( [https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf) )</span><span class="sxs-lookup"><span data-stu-id="e4887-106">For more information about profile registration and the CIM standard implementation of association traversal, see DSP1033 ([https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf))</span></span>

<span data-ttu-id="e4887-107">Para admitir esta característica, la infraestructura de WMI hizo lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e4887-107">To support this feature, the WMI infrastructure did the following:</span></span>

-   <span data-ttu-id="e4887-108">Se creó el espacio de nombres de interoperabilidad: \\ \\ interoperabilidad raíz.</span><span class="sxs-lookup"><span data-stu-id="e4887-108">Created the interop namespace: \\root\\interop.</span></span>
-   <span data-ttu-id="e4887-109">Cruce seguro de la Asociación de espacios de nombres cruzados permitido.</span><span class="sxs-lookup"><span data-stu-id="e4887-109">Allowed cross namespace association traversal.</span></span> <span data-ttu-id="e4887-110">Las asociaciones que cruzan los espacios de nombres admiten el filtrado en el nivel de clase de asociación y en el nivel de espacio de nombres implementado.</span><span class="sxs-lookup"><span data-stu-id="e4887-110">Associations that cross namespaces support filtering at the association class level and at the implemented namespace level.</span></span>
-   <span data-ttu-id="e4887-111">Se han agregado las clases [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)y [**CIM \_ ReferencedProfile**](cim-referencedprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="e4887-111">Added the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile), and [**CIM\_ReferencedProfile**](cim-referencedprofile.md) classes.</span></span>
-   <span data-ttu-id="e4887-112">Compatibilidad con la versión de esquema CIM 2.17.1.</span><span class="sxs-lookup"><span data-stu-id="e4887-112">Implemented CIM Schema version 2.17.1 compatibility.</span></span> <span data-ttu-id="e4887-113">Para obtener más información, consulte [compatibilidad con esquemas CIM](cim-schema-compatibility.md).</span><span class="sxs-lookup"><span data-stu-id="e4887-113">For more information, see [CIM Schema Compatibility](cim-schema-compatibility.md).</span></span>

## <a name="interop-namespace"></a><span data-ttu-id="e4887-114">Espacio de nombres Interop</span><span class="sxs-lookup"><span data-stu-id="e4887-114">Interop Namespace</span></span>

<span data-ttu-id="e4887-115">El espacio de nombres Interop proporciona una ubicación común para que una aplicación cliente detecte todos los perfiles que se admiten en un equipo.</span><span class="sxs-lookup"><span data-stu-id="e4887-115">The interop namespace provides a common location for a client application to discover all of the profiles that are supported on a computer.</span></span> <span data-ttu-id="e4887-116">Los perfiles se pueden usar para administrar diversos aspectos de un sistema operativo, una matriz de almacenamiento o una base de datos.</span><span class="sxs-lookup"><span data-stu-id="e4887-116">Profiles can be used to manage various aspects of an operating system, storage array, or database.</span></span>

<span data-ttu-id="e4887-117">Todas las clases y objetos de interoperabilidad se deben definir en el \\ espacio de nombres de interoperabilidad raíz.</span><span class="sxs-lookup"><span data-stu-id="e4887-117">All interop classes and objects must be defined in the root\\interop namespace.</span></span>

## <a name="cim-classes"></a><span data-ttu-id="e4887-118">Clases CIM</span><span class="sxs-lookup"><span data-stu-id="e4887-118">CIM Classes</span></span>

<span data-ttu-id="e4887-119">Las clases CIM descritas en la lista siguiente admiten el cruce seguro de la asociación entre espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="e4887-119">The CIM classes described in the following list support cross-namespace association traversal.</span></span>

<dl> <dt>

<span data-ttu-id="e4887-120"><span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e4887-120"><span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="e4887-121">Se utiliza para identificar la especificación de perfil que se anuncia como implementada.</span><span class="sxs-lookup"><span data-stu-id="e4887-121">Used to identify the profile specification that is advertised as being implemented.</span></span> <span data-ttu-id="e4887-122">Esta clase especifica información que incluye el nombre del perfil, la organización y la versión con la que es compatible la implementación.</span><span class="sxs-lookup"><span data-stu-id="e4887-122">This class specifies information that includes the profile name, organization, and version with which the implementation is compliant.</span></span>

</dd> <dt>

<span data-ttu-id="e4887-123"><span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)</span><span class="sxs-lookup"><span data-stu-id="e4887-123"><span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)</span></span>
</dt> <dd>

<span data-ttu-id="e4887-124">Se utiliza para asociar instancias de elementos de administración que se definen en perfiles con la clase [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) que identifica las especificaciones de perfil determinadas que se implementan.</span><span class="sxs-lookup"><span data-stu-id="e4887-124">Used to associate instances of management elements that are defined in profiles with the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) class that identifies the particular profile specifications that are implemented.</span></span>

</dd> <dt>

<span data-ttu-id="e4887-125"><span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**\_REFERENCEDPROFILE CIM**](cim-referencedprofile.md)</span><span class="sxs-lookup"><span data-stu-id="e4887-125"><span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**CIM\_ReferencedProfile**](cim-referencedprofile.md)</span></span>
</dt> <dd>

<span data-ttu-id="e4887-126">Se utiliza para representar la relación entre los perfiles.</span><span class="sxs-lookup"><span data-stu-id="e4887-126">Used to represent the relationship between profiles.</span></span>

</dd> </dl>

## <a name="implementing-cross-namespace-association-traversal"></a><span data-ttu-id="e4887-127">Implementación del cruce seguro de la asociación entre espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="e4887-127">Implementing Cross-Namespace Association Traversal</span></span>

<span data-ttu-id="e4887-128">El servicio WMI permite el cruce seguro de la asociación entre espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="e4887-128">The WMI service allows cross-namespace association traversal.</span></span> <span data-ttu-id="e4887-129">WMI proporciona el espacio de nombres de interoperabilidad para registrar perfiles y asociarlos a perfiles que se implementan en distintos espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="e4887-129">WMI provides the interop namespace for registering profiles and associating them with profiles that are implemented in different namespaces.</span></span> <span data-ttu-id="e4887-130">Sin embargo, para usar el recorrido de asociación, los implementadores deben crear instancias de las clases de perfil en la interoperabilidad y en el espacio de nombres implementado.</span><span class="sxs-lookup"><span data-stu-id="e4887-130">However, to use association traversal, implementers must instantiate the profile classes both in the interop and in the implemented namespace.</span></span> <span data-ttu-id="e4887-131">Para obtener más información, consulte [escribir un proveedor de Asociación para la interoperabilidad](writing-an-association-provider-for-interop.md).</span><span class="sxs-lookup"><span data-stu-id="e4887-131">For more information, see [Writing an Association Provider for Interop](writing-an-association-provider-for-interop.md).</span></span>

<span data-ttu-id="e4887-132">Las asociaciones que cruzan espacios de nombres dentro del mismo entorno de administración deben crearse en los espacios de nombres de interoperabilidad e implementados.</span><span class="sxs-lookup"><span data-stu-id="e4887-132">Associations that cross namespaces within the same management environment must be instantiated in both the interop and implemented namespaces.</span></span> <span data-ttu-id="e4887-133">De lo contrario, el cruce seguro de la asociación no funcionará.</span><span class="sxs-lookup"><span data-stu-id="e4887-133">Otherwise, association traversal will not work.</span></span> <span data-ttu-id="e4887-134">Por ejemplo, el proveedor de asociaciones de Perfil de energía se debe registrar con los espacios de nombres root/Interop y root/cimv2/Power.</span><span class="sxs-lookup"><span data-stu-id="e4887-134">For example, the power profile association provider must be registered with both root/interop and root/cimv2/power namespaces.</span></span> <span data-ttu-id="e4887-135">El cruce seguro de la asociación debe ser capaz de producirse desde el espacio de nombres de nuevo al otro.</span><span class="sxs-lookup"><span data-stu-id="e4887-135">Association traversal should be able to occur from either namespace back to the other.</span></span> <span data-ttu-id="e4887-136">Para obtener ejemplos de cruce seguro de la asociación, vea [acceso a datos en el espacio de nombres de interoperabilidad](accessing-data-in-the-interop-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="e4887-136">For examples of association traversal, see [Accessing Data in the Interop Namespace](accessing-data-in-the-interop-namespace.md).</span></span>

<span data-ttu-id="e4887-137">\* \* Windows Vista: \* \*</span><span class="sxs-lookup"><span data-stu-id="e4887-137">\*\*Windows Vista:  \*\*</span></span>

<span data-ttu-id="e4887-138">Después de actualizar a Windows 7, si hay perfiles de dispositivo de interoperabilidad que se instalaron previamente en el espacio de nombres root/Interop, no se instalará ningún perfil de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e4887-138">After upgrading to Windows 7, if there are interop device profiles that were previously installed in the root/interop namespace, no Windows 7 profiles will be installed.</span></span> <span data-ttu-id="e4887-139">Estos objetos de Perfil de terceros sobrescriben el esquema de interoperabilidad de Windows 7 para mantener la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="e4887-139">These third-party profile objects overwrite Windows 7 interop schema to maintain functionality.</span></span> <span data-ttu-id="e4887-140">Además, se registra el ID. de evento 5631 de la aplicación WMI.</span><span class="sxs-lookup"><span data-stu-id="e4887-140">Additionally, the WMI application event ID 5631 is recorded.</span></span>

<span data-ttu-id="e4887-141">Para obtener los perfiles de interoperabilidad de Windows 7, se debe compilar la versión de Windows 7 del archivo Interop. mof y los archivos MFL relacionados.</span><span class="sxs-lookup"><span data-stu-id="e4887-141">To get the Windows 7 interop profiles, the Windows 7 version of the Interop.mof file and the related MFL files must be compiled.</span></span> <span data-ttu-id="e4887-142">Para obtener más información, vea [compilar archivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="e4887-142">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4887-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e4887-143">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e4887-144">[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e4887-144">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e4887-145">**\_ELEMENTCONFORMSTOPROFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="e4887-145">**CIM\_ElementConformsToProfile**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[<span data-ttu-id="e4887-146">**\_REFERENCEDPROFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="e4887-146">**CIM\_ReferencedProfile**</span></span>](cim-referencedprofile.md)
</dt> <dt>

[<span data-ttu-id="e4887-147">Compatibilidad con esquemas CIM</span><span class="sxs-lookup"><span data-stu-id="e4887-147">CIM Schema Compatibility</span></span>](cim-schema-compatibility.md)
</dt> <dt>

[<span data-ttu-id="e4887-148">Escribir un proveedor de Asociación para la interoperabilidad</span><span class="sxs-lookup"><span data-stu-id="e4887-148">Writing an Association Provider for Interop</span></span>](writing-an-association-provider-for-interop.md)
</dt> <dt>

[<span data-ttu-id="e4887-149">Obtener acceso a los datos en el espacio de nombres Interop</span><span class="sxs-lookup"><span data-stu-id="e4887-149">Accessing Data in the Interop Namespace</span></span>](accessing-data-in-the-interop-namespace.md)
</dt> </dl>

 

 
