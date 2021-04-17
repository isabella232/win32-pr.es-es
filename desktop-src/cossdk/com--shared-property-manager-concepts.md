---
description: En COM+, el estado transitorio compartido de los objetos se administra mediante el administrador de propiedades compartidas (SPM). SPM es un dispensador de recursos que puede usar para compartir el estado entre varios objetos dentro de un proceso de servidor.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: Conceptos de Administrador de propiedades compartidos de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be55c4a83aa363c911564aefabbe1d85f3804fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714873"
---
# <a name="com-shared-property-manager-concepts"></a><span data-ttu-id="c2d51-104">Conceptos de Administrador de propiedades compartidos de COM+</span><span class="sxs-lookup"><span data-stu-id="c2d51-104">COM+ Shared Property Manager Concepts</span></span>

<span data-ttu-id="c2d51-105">En COM+, el estado transitorio compartido de los objetos se administra mediante el administrador de propiedades compartidas (SPM).</span><span class="sxs-lookup"><span data-stu-id="c2d51-105">In COM+, shared transient state for objects is managed by using the shared property manager (SPM).</span></span> <span data-ttu-id="c2d51-106">SPM es un dispensador de recursos que puede usar para compartir el estado entre varios objetos dentro de un proceso de servidor.</span><span class="sxs-lookup"><span data-stu-id="c2d51-106">The SPM is a resource dispenser that you can use to share state among multiple objects within a server process.</span></span>

<span data-ttu-id="c2d51-107">Las variables globales no se pueden usar en un entorno distribuido debido a problemas de simultaneidad y conflicto de nombres.</span><span class="sxs-lookup"><span data-stu-id="c2d51-107">You cannot use global variables in a distributed environment because of concurrency and name collision issues.</span></span> <span data-ttu-id="c2d51-108">El administrador de propiedades compartidas elimina los conflictos de nombres al proporcionar grupos de propiedades compartidas, que establecen espacios de nombres únicos para las propiedades compartidas que contienen.</span><span class="sxs-lookup"><span data-stu-id="c2d51-108">The shared property manager eliminates name collisions by providing shared property groups, which establish unique namespaces for the shared properties they contain.</span></span> <span data-ttu-id="c2d51-109">SPM también implementa bloqueos y semáforos para ayudar a proteger las propiedades compartidas de acceso simultáneo, lo que podría provocar la pérdida de actualizaciones y dejar propiedades en un estado impredecible.</span><span class="sxs-lookup"><span data-stu-id="c2d51-109">The SPM also implements locks and semaphores to help protect shared properties from simultaneous access, which could result in lost updates and leave properties in an unpredictable state.</span></span>

> [!Note]  
> <span data-ttu-id="c2d51-110">El estado transitorio compartido es la información de estado conservada en memoria que no sobrevive los errores del sistema.</span><span class="sxs-lookup"><span data-stu-id="c2d51-110">Shared transient state is state information kept in memory that does not survive system failures.</span></span> <span data-ttu-id="c2d51-111">La información está diseñada para que la compartan varios objetos a través de los límites de transacciones (pero no entre procesos).</span><span class="sxs-lookup"><span data-stu-id="c2d51-111">The information is designed to be shared by multiple objects across transaction (but not across process) boundaries.</span></span>

 

<span data-ttu-id="c2d51-112">Las propiedades compartidas almacenadas en SPM solo están disponibles para los objetos que se ejecutan en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="c2d51-112">Shared properties stored in the SPM are available only to objects running in the same process.</span></span> <span data-ttu-id="c2d51-113">Esto significa que los objetos que utilizarán SPM para almacenar valores y que necesitarán tener acceso a estos valores se deben instalar como parte de la misma aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="c2d51-113">This means that the objects that will use the SPM for storing values and that will need to have access to these values must be installed as part of the same COM+ application.</span></span> <span data-ttu-id="c2d51-114">Los administradores del sistema pueden trasladar las clases COM+ de un paquete a otro una vez implementada la aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="c2d51-114">It is possible for system administrators to move COM+ classes from one package to another after your COM+ application has been deployed.</span></span> <span data-ttu-id="c2d51-115">Si confía en varios objetos que comparten propiedades a través de SPM, debe documentar claramente que deben instalarse en la misma aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="c2d51-115">If you rely on several objects sharing properties through the SPM, you should clearly document that they must be installed in the same COM+ application.</span></span>

<span data-ttu-id="c2d51-116">También es importante que los componentes que comparten propiedades tengan el mismo atributo de activación.</span><span class="sxs-lookup"><span data-stu-id="c2d51-116">It's also important for components sharing properties to have the same activation attribute.</span></span> <span data-ttu-id="c2d51-117">Si dos componentes del mismo paquete tienen atributos de activación diferentes, por lo general no podrán compartir propiedades.</span><span class="sxs-lookup"><span data-stu-id="c2d51-117">If two components in the same package have different activation attributes, they generally won't be able to share properties.</span></span> <span data-ttu-id="c2d51-118">Por ejemplo, si un componente está configurado para ejecutarse en un proceso de cliente y el otro está configurado para ejecutarse en un proceso de servidor, sus objetos normalmente se ejecutarán en procesos diferentes, aunque estén en el mismo paquete.</span><span class="sxs-lookup"><span data-stu-id="c2d51-118">For example, if one component is configured to run in a client process and the other is configured to run in a server process, their objects will usually run in different processes even though they're in the same package.</span></span>

<span data-ttu-id="c2d51-119">Siempre debe crear una instancia de los objetos [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md)y [**SharedProperty**](sharedproperty.md) a partir de los componentes com+ en lugar de hacerlo desde un cliente base.</span><span class="sxs-lookup"><span data-stu-id="c2d51-119">You should always instantiate the [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md), and [**SharedProperty**](sharedproperty.md) objects from COM+ components rather than from a base client.</span></span> <span data-ttu-id="c2d51-120">Si un cliente base crea propiedades y grupos de propiedades compartidas, las propiedades compartidas se encuentran dentro del proceso de cliente base, no en un proceso de servidor.</span><span class="sxs-lookup"><span data-stu-id="c2d51-120">If a base client creates shared property groups and properties, the shared properties are inside the base-client process, not in a server process.</span></span> <span data-ttu-id="c2d51-121">Esto significa que los objetos COM+ no pueden compartir las propiedades a menos que los objetos también se ejecuten en el proceso del cliente (que no suele ser una buena idea).</span><span class="sxs-lookup"><span data-stu-id="c2d51-121">This means the COM+ objects cannot share the properties unless the objects are also running in the client process (which is generally not a good idea).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2d51-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c2d51-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2d51-123">Administrador de propiedades compartidos de COM+</span><span class="sxs-lookup"><span data-stu-id="c2d51-123">COM+ Shared Property Manager</span></span>](com--shared-property-manager.md)
</dt> <dt>

[<span data-ttu-id="c2d51-124">Grupos de propiedades compartidas</span><span class="sxs-lookup"><span data-stu-id="c2d51-124">Shared Property Groups</span></span>](shared-property-groups.md)
</dt> </dl>

 

 



