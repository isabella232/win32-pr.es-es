---
description: Las interfaces de CRM son necesarias para proporcionar compatibilidad con los trabajos de CRM y los compensadores de CRM desarrollados mediante Visual Basic y Visual C++.
ms.assetid: 68a75da7-1f35-41a4-8872-e3f4ad1fc30d
title: Interfaces de CRM para COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ba3235b1cd2a82fc913dd676bbb78324f340cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807904"
---
# <a name="com-crm-interfaces"></a><span data-ttu-id="4e44f-103">Interfaces de CRM para COM+</span><span class="sxs-lookup"><span data-stu-id="4e44f-103">COM+ CRM Interfaces</span></span>

<span data-ttu-id="4e44f-104">Las interfaces de CRM son necesarias para proporcionar compatibilidad con los trabajos de CRM y los compensadores de CRM desarrollados mediante Visual Basic y Visual C++.</span><span class="sxs-lookup"><span data-stu-id="4e44f-104">The CRM interfaces are required to provide support for CRM Workers and CRM Compensators developed using Visual Basic and Visual C++.</span></span>

<span data-ttu-id="4e44f-105">Puede usar el Administrador de recursos de compensación de COM+ (CRM) para integrar rápida y fácilmente los recursos de la aplicación con las transacciones de Microsoft Coordinador de transacciones distribuidas (DTC).</span><span class="sxs-lookup"><span data-stu-id="4e44f-105">You can use the COM+ Compensating Resource Manager (CRM) to quickly and easily integrate application resources with Microsoft Distributed Transaction Coordinator (DTC) transactions.</span></span>

<span data-ttu-id="4e44f-106">Es más fácil para los componentes escritos con Visual Basic crear una entrada de registro como una colección de variantes.</span><span class="sxs-lookup"><span data-stu-id="4e44f-106">It is easier for components written with Visual Basic to build up a log record as a collection of Variants.</span></span> <span data-ttu-id="4e44f-107">Además, los componentes de Visual Basic son subprocesos de apartamento, lo que implica que debe ser posible calcular las referencias de las interfaces del apartamento multiproceso a un contenedor uniproceso.</span><span class="sxs-lookup"><span data-stu-id="4e44f-107">Also, Visual Basic components are apartment threaded, which implies that it must be possible to marshal the interfaces from the multithreaded apartment to a single-threaded apartment.</span></span> <span data-ttu-id="4e44f-108">Los componentes de CRM desarrollados con Visual C++ también podrían usar el modelo de subprocesos de apartamento, aunque se recomienda usar el modelo de subprocesos de ambos en su lugar.</span><span class="sxs-lookup"><span data-stu-id="4e44f-108">CRM components developed with Visual C++ could also use the Apartment threading model, although it is recommended that these use the Both threading model instead.</span></span>

<span data-ttu-id="4e44f-109">Las interfaces descritas en la tabla siguiente proporcionan información de referencia detallada para los programadores de CRMs de COM+.</span><span class="sxs-lookup"><span data-stu-id="4e44f-109">The interfaces described in the following table provide detailed reference information for developers of COM+ CRMs.</span></span>



| <span data-ttu-id="4e44f-110">Interfaces CRM</span><span class="sxs-lookup"><span data-stu-id="4e44f-110">CRM interfaces</span></span>                                             | <span data-ttu-id="4e44f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e44f-111">Description</span></span>                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e44f-112">**ICrmCompensator**</span><span class="sxs-lookup"><span data-stu-id="4e44f-112">**ICrmCompensator**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator)                 | <span data-ttu-id="4e44f-113">Esta interfaz proporciona entradas de registro no estructuradas en Visual C++.</span><span class="sxs-lookup"><span data-stu-id="4e44f-113">This interface delivers unstructured log records in Visual C++.</span></span>                                                           |
| [<span data-ttu-id="4e44f-114">**ICrmCompensatorVariants**</span><span class="sxs-lookup"><span data-stu-id="4e44f-114">**ICrmCompensatorVariants**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) | <span data-ttu-id="4e44f-115">Esta interfaz proporciona entradas de registro estructuradas al compensador de CRM cuando se usa Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4e44f-115">This interface delivers structured log records to the CRM Compensator when using Visual Basic.</span></span>                            |
| [<span data-ttu-id="4e44f-116">**ICrmFormatLogRecords**</span><span class="sxs-lookup"><span data-stu-id="4e44f-116">**ICrmFormatLogRecords**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmformatlogrecords)       | <span data-ttu-id="4e44f-117">Esta interfaz convierte las entradas de registro en un formato visible para que se puedan presentar mediante una herramienta de supervisión genérica.</span><span class="sxs-lookup"><span data-stu-id="4e44f-117">This interface converts the log records to viewable format so that they can be presented using a generic monitoring tool.</span></span> |
| [<span data-ttu-id="4e44f-118">**ICrmLogControl**</span><span class="sxs-lookup"><span data-stu-id="4e44f-118">**ICrmLogControl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)                   | <span data-ttu-id="4e44f-119">Esta interfaz la usa el compensador de CRM y el trabajo de CRM para escribir registros en el registro y hacerlos duraderos.</span><span class="sxs-lookup"><span data-stu-id="4e44f-119">This interface is used by the CRM Worker and CRM Compensator to write records to the log and make them durable.</span></span>           |
| [<span data-ttu-id="4e44f-120">**ICrmMonitor**</span><span class="sxs-lookup"><span data-stu-id="4e44f-120">**ICrmMonitor**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)                         | <span data-ttu-id="4e44f-121">Esta interfaz captura una instantánea del estado actual de un CRM y contiene un funcionario de CRM específico.</span><span class="sxs-lookup"><span data-stu-id="4e44f-121">This interface captures a snapshot of the current state of a CRM and holds a specific CRM clerk.</span></span>                          |
| [<span data-ttu-id="4e44f-122">**ICrmMonitorClerks**</span><span class="sxs-lookup"><span data-stu-id="4e44f-122">**ICrmMonitorClerks**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)             | <span data-ttu-id="4e44f-123">Esta interfaz obtiene información sobre el estado de los empleados.</span><span class="sxs-lookup"><span data-stu-id="4e44f-123">This interface obtains information about the state of clerks.</span></span>                                                             |
| [<span data-ttu-id="4e44f-124">**ICrmMonitorLogRecords**</span><span class="sxs-lookup"><span data-stu-id="4e44f-124">**ICrmMonitorLogRecords**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)     | <span data-ttu-id="4e44f-125">Esta interfaz supervisa las entradas de registro individuales mantenidas por un funcionario de CRM específico para una transacción determinada.</span><span class="sxs-lookup"><span data-stu-id="4e44f-125">This interface monitors the individual log records maintained by a specific CRM clerk for a given transaction.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="4e44f-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e44f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e44f-127">Conceptos de Administrador de recursos de compensación de COM+</span><span class="sxs-lookup"><span data-stu-id="4e44f-127">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



