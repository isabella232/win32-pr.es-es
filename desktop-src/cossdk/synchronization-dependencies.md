---
description: Los valores de sincronización se pueden determinar o restringir automáticamente mediante la configuración de otras propiedades, como los requisitos transaccionales y la activación Just-in-Time (JIT).
ms.assetid: 16771121-cb10-42b4-babc-59270188495a
title: Dependencias de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c139d0d6e78288b25e42bd0a84b29432cebb44ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907150"
---
# <a name="synchronization-dependencies"></a><span data-ttu-id="8a5f6-103">Dependencias de sincronización</span><span class="sxs-lookup"><span data-stu-id="8a5f6-103">Synchronization Dependencies</span></span>

<span data-ttu-id="8a5f6-104">Los valores de sincronización se pueden determinar o restringir automáticamente mediante la configuración de otras propiedades, como los requisitos transaccionales y la activación Just-in-Time (JIT).</span><span class="sxs-lookup"><span data-stu-id="8a5f6-104">Synchronization values can be automatically determined or constrained by the configuration of other properties, such as transactional requirements and just-in-time (JIT) activation.</span></span> <span data-ttu-id="8a5f6-105">Por ejemplo, COM+ aplica la sincronización para los componentes transaccionales y para los componentes activados por JIT.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-105">For example, COM+ enforces synchronization both for transactional and for JIT-activated components.</span></span>

<span data-ttu-id="8a5f6-106">Estas dependencias existen porque los componentes que están activados con JIT o que participan en transacciones deben tener el aislamiento y el comportamiento de simultaneidad adecuados.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-106">These dependencies exist because components that are JIT-activated or participating in transactions must have proper isolation and concurrency behavior.</span></span> <span data-ttu-id="8a5f6-107">Por lo tanto, COM+ requiere que el acceso a estos componentes se serialice mediante la aplicación de la sincronización.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-107">Therefore, COM+ requires that access to these components be serialized by enforcing synchronization.</span></span> <span data-ttu-id="8a5f6-108">(Para obtener más información sobre estas dependencias, consulte [activación Just-in-Time de com+](com--just-in-time-activation.md)).</span><span class="sxs-lookup"><span data-stu-id="8a5f6-108">(For details on these dependencies, see [COM+ Just-in-Time Activation](com--just-in-time-activation.md).)</span></span>

<span data-ttu-id="8a5f6-109">En las tablas siguientes se muestran las características de los valores de atributo de sincronización de COM+.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-109">The following tables show the characteristics of the COM+ synchronization attribute values.</span></span>

### <a name="transactional-requirement"></a><span data-ttu-id="8a5f6-110">Requisito transaccional</span><span class="sxs-lookup"><span data-stu-id="8a5f6-110">Transactional requirement</span></span>



| <span data-ttu-id="8a5f6-111">Cuando las transacciones se establecen en</span><span class="sxs-lookup"><span data-stu-id="8a5f6-111">When transactions are set to</span></span> | <span data-ttu-id="8a5f6-112">La sincronización se puede establecer en</span><span class="sxs-lookup"><span data-stu-id="8a5f6-112">Synchronization can be set to</span></span>                    |
|------------------------------|--------------------------------------------------|
| <span data-ttu-id="8a5f6-113">Disabled</span><span class="sxs-lookup"><span data-stu-id="8a5f6-113">Disabled</span></span><br/>          | <span data-ttu-id="8a5f6-114">Cualquier cosa, en función de la activación JIT</span><span class="sxs-lookup"><span data-stu-id="8a5f6-114">Anything, depending on JIT activation</span></span><br/> |
| <span data-ttu-id="8a5f6-115">No compatible</span><span class="sxs-lookup"><span data-stu-id="8a5f6-115">Not Supported</span></span><br/>     | <span data-ttu-id="8a5f6-116">Cualquier cosa, en función de la activación JIT</span><span class="sxs-lookup"><span data-stu-id="8a5f6-116">Anything, depending on JIT activation</span></span><br/> |
| <span data-ttu-id="8a5f6-117">Compatible</span><span class="sxs-lookup"><span data-stu-id="8a5f6-117">Supported</span></span><br/>         | <span data-ttu-id="8a5f6-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8a5f6-118">Required</span></span><br/>                              |
| <span data-ttu-id="8a5f6-119">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8a5f6-119">Required</span></span><br/>          | <span data-ttu-id="8a5f6-120">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8a5f6-120">Required</span></span><br/>                              |
| <span data-ttu-id="8a5f6-121">Se requiere nueva</span><span class="sxs-lookup"><span data-stu-id="8a5f6-121">Requires New</span></span><br/>      | <span data-ttu-id="8a5f6-122">Requerido o requiere nuevo</span><span class="sxs-lookup"><span data-stu-id="8a5f6-122">Required or Requires New</span></span><br/>              |



 

### <a name="jit-activation"></a><span data-ttu-id="8a5f6-123">Activación JIT</span><span class="sxs-lookup"><span data-stu-id="8a5f6-123">JIT Activation</span></span>



| <span data-ttu-id="8a5f6-124">Cuando la activación JIT está establecida en</span><span class="sxs-lookup"><span data-stu-id="8a5f6-124">When JIT Activation is set to</span></span> | <span data-ttu-id="8a5f6-125">La sincronización se puede establecer en</span><span class="sxs-lookup"><span data-stu-id="8a5f6-125">Synchronization can be set to</span></span>       |
|-------------------------------|-------------------------------------|
| <span data-ttu-id="8a5f6-126">habilitado</span><span class="sxs-lookup"><span data-stu-id="8a5f6-126">Enabled</span></span><br/>            | <span data-ttu-id="8a5f6-127">Requerido o requiere nuevo</span><span class="sxs-lookup"><span data-stu-id="8a5f6-127">Required or Requires New</span></span><br/> |
| <span data-ttu-id="8a5f6-128">Disabled</span><span class="sxs-lookup"><span data-stu-id="8a5f6-128">Disabled</span></span><br/>           | <span data-ttu-id="8a5f6-129">Haya</span><span class="sxs-lookup"><span data-stu-id="8a5f6-129">Anything</span></span><br/>                 |



 

<span data-ttu-id="8a5f6-130">Para obtener más información sobre cómo se comportan conjuntamente las transacciones, la activación JIT y los atributos de sincronización, vea [Configuring Transactions](configuring-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="8a5f6-130">For more detail about how transaction, JIT Activation, and Synchronization attributes behave together, see [Configuring Transactions](configuring-transactions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a5f6-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a5f6-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a5f6-132">Establecer el atributo de sincronización</span><span class="sxs-lookup"><span data-stu-id="8a5f6-132">Setting the Synchronization Attribute</span></span>](setting-the-synchronization-attribute.md)
</dt> <dt>

[<span data-ttu-id="8a5f6-133">Valores de atributo de sincronización</span><span class="sxs-lookup"><span data-stu-id="8a5f6-133">Synchronization Attribute Values</span></span>](synchronization-attribute-values.md)
</dt> </dl>

 

 




