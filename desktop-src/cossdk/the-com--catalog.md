---
description: El catálogo de COM+ almacena los atributos de la aplicación COM+, los atributos de clase y los atributos de nivel de equipo. Garantiza la coherencia entre estos atributos y proporciona operaciones comunes sobre estos atributos.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: El catálogo de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad869a6df6a61fc338fe07002512a1de27002788
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666171"
---
# <a name="the-com-catalog"></a><span data-ttu-id="8ed0e-104">El catálogo de COM+</span><span class="sxs-lookup"><span data-stu-id="8ed0e-104">The COM+ Catalog</span></span>

<span data-ttu-id="8ed0e-105">El catálogo de COM+ almacena los atributos de la aplicación COM+, los atributos de clase y los atributos de nivel de equipo.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-105">The COM+ catalog stores COM+ application attributes, class attributes, and computer-level attributes.</span></span> <span data-ttu-id="8ed0e-106">Garantiza la coherencia entre estos atributos y proporciona operaciones comunes sobre estos atributos.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-106">It guarantees consistency among these attributes and provides common operations on top of these attributes.</span></span>

<span data-ttu-id="8ed0e-107">El catálogo de COM+ utiliza dos almacenes diferentes, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8ed0e-107">The COM+ catalog uses two different stores, as follows:</span></span>

-   <span data-ttu-id="8ed0e-108">La base de datos de registro de COM+</span><span class="sxs-lookup"><span data-stu-id="8ed0e-108">The COM+ registration database</span></span>
-   <span data-ttu-id="8ed0e-109">El registro de Windows **( \_ clases HKEY \_ raíz**)</span><span class="sxs-lookup"><span data-stu-id="8ed0e-109">The Windows registry (**HKEY\_CLASSES\_ROOT**)</span></span>

<span data-ttu-id="8ed0e-110">El catálogo presenta una vista lógica y unificada de estos dos almacenes y los expone a través de la biblioteca de administración de COM+.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-110">The catalog presents a unified, logical view of these two stores and exposes them through the COM+ Administration Library.</span></span> <span data-ttu-id="8ed0e-111">Esta biblioteca proporciona, a través de un lenguaje de scripting, toda la funcionalidad de la herramienta administrativa Servicios de componentes.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-111">This library provides, through a scripting language, all the functionality of the Component Services administrative tool.</span></span>

<span data-ttu-id="8ed0e-112">En el caso de los componentes COM existentes que no requieren ningún servicio COM+ nuevo, la búsqueda se produce en el registro de Windows existente.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-112">For existing COM components that do not require any new COM+ services, lookup occurs in the existing Windows registry.</span></span> <span data-ttu-id="8ed0e-113">El catálogo de COM+ también utiliza el registro de Windows para la biblioteca de tipos y el registro de código auxiliar y proxy de interfaz.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-113">The COM+ catalog also uses the Windows registry for type library and interface proxy/stub registration.</span></span>

## <a name="split-registration"></a><span data-ttu-id="8ed0e-114">Dividir registro</span><span class="sxs-lookup"><span data-stu-id="8ed0e-114">Split Registration</span></span>

<span data-ttu-id="8ed0e-115">En el caso de los componentes nuevos que ya son componentes COM existentes que se usan en el entorno de servicios (por ejemplo, componentes MTS), el aspecto COM básico del registro se almacena en el registro de Windows y los nuevos servicios y atributos (por ejemplo, los componentes en cola) se almacenan en la base de datos de registro de COM+.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-115">For new components that are actually already existing COM components that are used in the services environment (for example, MTS components), the basic COM aspect of the registration is stored in the Windows registry and new services and attributes (for example, queued components) are stored in the COM+ registration database.</span></span> <span data-ttu-id="8ed0e-116">Esto se conoce como *registro dividido*.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-116">This is known as a *split registration*.</span></span>

<span data-ttu-id="8ed0e-117">Cada atributo se almacena en una sola ubicación: el registro de Windows o la base de datos de registro de COM+.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-117">Each attribute is stored in only one location: either the Windows registry or the COM+ registration database.</span></span> <span data-ttu-id="8ed0e-118">Los nuevos componentes COM se registran exclusivamente en la base de datos de registro de COM+, con algunas duplicaciones en el registro de Windows para que las herramientas existentes puedan utilizarlos.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-118">New COM components are registered exclusively in the COM+ registration database, with some duplication in the Windows registry so that existing tools can use them.</span></span>

## <a name="transactional-updates-to-the-catalog"></a><span data-ttu-id="8ed0e-119">Actualizaciones transaccionales en el catálogo</span><span class="sxs-lookup"><span data-stu-id="8ed0e-119">Transactional Updates to the Catalog</span></span>

<span data-ttu-id="8ed0e-120">Algunas operaciones en el catálogo se realizan de manera transaccional.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-120">Some operations on the catalog are performed in a transactional manner.</span></span> <span data-ttu-id="8ed0e-121">Al invocar la biblioteca de administración de COM+ desde un componente transaccional, las actualizaciones de la base de datos de registro de COM+ se realizarán dentro del límite de la transacción del componente que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-121">When you invoke the COM+ Administration Library from a transactional component, the updates to the COM+ registration database will take place within the calling component's transaction boundary.</span></span>

<span data-ttu-id="8ed0e-122">Sin embargo, no se garantiza que las actualizaciones que implican cambios en otros almacenes (como el sistema de archivos y el registro de Windows) sean completamente transaccionales.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-122">However, updates that involve changes to other stores (such as the file system and Windows registry) are not guaranteed to be fully transactional.</span></span> <span data-ttu-id="8ed0e-123">Una transacción anulada puede dejar estos almacenes en un estado incoherente con los cambios realizados en otro o en la base de datos de registro de COM+.</span><span class="sxs-lookup"><span data-stu-id="8ed0e-123">An aborted transaction can leave these stores in a state that is inconsistent with any changes made to one another or to the COM+ registration database.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ed0e-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8ed0e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ed0e-125">Crear paquetes de instalación para aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="8ed0e-125">Creating Installation Packages for COM+ Applications</span></span>](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[<span data-ttu-id="8ed0e-126">Implementación de servidores proxy de aplicación</span><span class="sxs-lookup"><span data-stu-id="8ed0e-126">Deploying Application Proxies</span></span>](deploying-application-proxies.md)
</dt> <dt>

[<span data-ttu-id="8ed0e-127">La utilidad de replicación COMREPL</span><span class="sxs-lookup"><span data-stu-id="8ed0e-127">The COMREPL Replication Utility</span></span>](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



