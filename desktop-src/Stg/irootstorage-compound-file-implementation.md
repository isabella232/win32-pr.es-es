---
title: 'IRootStorage: implementación de archivos compuestos'
description: La implementación de archivos compuestos de COM de IRootStorage permite guardar archivos en situaciones de poca memoria o de poco espacio en disco. Para obtener información sobre cómo se comporta esta interfaz, vea IRootStorage.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- IRootStorage Strctd STG, implementación de archivo compuesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928f78e88ffaa526006c0a33e803076db0ec301e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780106"
---
# <a name="irootstorage---compound-file-implementation"></a><span data-ttu-id="91ea7-105">IRootStorage: implementación de archivos compuestos</span><span class="sxs-lookup"><span data-stu-id="91ea7-105">IRootStorage - Compound File Implementation</span></span>

<span data-ttu-id="91ea7-106">La implementación de archivos compuestos de COM de [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) permite guardar archivos en situaciones de poca memoria o de poco espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="91ea7-106">COM's compound file implementation of [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) allows you to support saving files in low-memory or low disk-space situations.</span></span> <span data-ttu-id="91ea7-107">Para obtener información sobre cómo se comporta esta interfaz, vea **IRootStorage**.</span><span class="sxs-lookup"><span data-stu-id="91ea7-107">For information on how this interface behaves, see **IRootStorage**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="91ea7-108">Cuándo usar</span><span class="sxs-lookup"><span data-stu-id="91ea7-108">When to Use</span></span>

<span data-ttu-id="91ea7-109">Use la implementación proporcionada por el sistema de [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) solo para admitir el guardado de archivos en condiciones de memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="91ea7-109">Use the system-supplied implementation of [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) only to support saving files under low-memory conditions.</span></span>

## <a name="remarks"></a><span data-ttu-id="91ea7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91ea7-110">Remarks</span></span>

<span data-ttu-id="91ea7-111">Es posible llamar a la implementación de COM de [**IRootStorage:: SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) para realizar una operación de guardar como normal en otro archivo.</span><span class="sxs-lookup"><span data-stu-id="91ea7-111">It is possible to call COM's implementation of [**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) to do a normal save-as operation to another file.</span></span> <span data-ttu-id="91ea7-112">Sin embargo, las aplicaciones que lo hacen podrían no ser compatibles con las generaciones futuras del almacenamiento COM.</span><span class="sxs-lookup"><span data-stu-id="91ea7-112">However, applications that do this might not be compatible with future generations of COM storage.</span></span> <span data-ttu-id="91ea7-113">Para evitar esta posibilidad, las aplicaciones que realizan una operación de guardar como deben crear manualmente el segundo archivo compuesto e invocar [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto).</span><span class="sxs-lookup"><span data-stu-id="91ea7-113">To avoid this possibility, applications performing a save-as operation should manually create the second compound file and invoke [**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto).</span></span> <span data-ttu-id="91ea7-114">El método **IRootStorage:: SwitchToFile** solo se debe usar en situaciones de emergencia (memoria insuficiente o espacio en disco).</span><span class="sxs-lookup"><span data-stu-id="91ea7-114">The **IRootStorage::SwitchToFile** method should be used only in emergency (low-memory or disk-space) situations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91ea7-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91ea7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91ea7-116">**IRootStorage**</span><span class="sxs-lookup"><span data-stu-id="91ea7-116">**IRootStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[<span data-ttu-id="91ea7-117">**IRootStorage::SwitchToFile**</span><span class="sxs-lookup"><span data-stu-id="91ea7-117">**IRootStorage::SwitchToFile**</span></span>](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




