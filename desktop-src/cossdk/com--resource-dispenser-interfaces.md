---
description: Interfaces dispensadoras de recursos COM+
ms.assetid: 66ee4dd6-15d2-49e8-89a3-6fbb5770cabf
title: Interfaces dispensadoras de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a6ea5c5c09f67f86b42ebf5b881f1d19ad1501
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907094"
---
# <a name="com-resource-dispenser-interfaces"></a><span data-ttu-id="8e8c3-103">Interfaces dispensadoras de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="8e8c3-103">COM+ Resource Dispenser Interfaces</span></span>

<span data-ttu-id="8e8c3-104">Los componentes de aplicación usan dispensadores de recursos para acceder a la información compartida.</span><span class="sxs-lookup"><span data-stu-id="8e8c3-104">Application components use resource dispensers to access shared information.</span></span> <span data-ttu-id="8e8c3-105">Las interfaces descritas en la tabla siguiente proporcionan información de referencia detallada para los desarrolladores de distribuidores de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e8c3-105">The interfaces described in the following table provide detailed reference information for developers of resource dispensers.</span></span>



| <span data-ttu-id="8e8c3-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="8e8c3-106">Interfaces</span></span>                                                | <span data-ttu-id="8e8c3-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e8c3-107">Description</span></span>                                                                                                               |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e8c3-108">**IDispenserDriver**</span><span class="sxs-lookup"><span data-stu-id="8e8c3-108">**IDispenserDriver**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)<br/>   | <span data-ttu-id="8e8c3-109">El titular del dispensador de recursos llama a esta interfaz para crear, dar de alta, evaluar y destruir un recurso.</span><span class="sxs-lookup"><span data-stu-id="8e8c3-109">This interface is called by the resource dispenser holder to create, enlist, evaluate, and destroy a resource.</span></span><br/> |
| [<span data-ttu-id="8e8c3-110">**IDispenserManager**</span><span class="sxs-lookup"><span data-stu-id="8e8c3-110">**IDispenserManager**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager)<br/> | <span data-ttu-id="8e8c3-111">Los distribuidores de recursos usan esta interfaz para conectarse al administrador dispensador.</span><span class="sxs-lookup"><span data-stu-id="8e8c3-111">Resource dispensers use this interface to connect to the dispenser manager.</span></span><br/>                                    |
| [<span data-ttu-id="8e8c3-112">**IHolder**</span><span class="sxs-lookup"><span data-stu-id="8e8c3-112">**IHolder**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)<br/>                     | <span data-ttu-id="8e8c3-113">Esta interfaz se usa para preparar y administrar recursos.</span><span class="sxs-lookup"><span data-stu-id="8e8c3-113">This interface is used to prepare and handle resources.</span></span><br/>                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="8e8c3-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8e8c3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e8c3-115">Conceptos del dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="8e8c3-115">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> <dt>

[<span data-ttu-id="8e8c3-116">Tipos usados en las interfaces del dispensador de recursos COM+</span><span class="sxs-lookup"><span data-stu-id="8e8c3-116">Types Used in COM+ Resource Dispenser Interfaces</span></span>](types-used-in-com--resource-dispenser-interfaces.md)
</dt> </dl>

 

 




