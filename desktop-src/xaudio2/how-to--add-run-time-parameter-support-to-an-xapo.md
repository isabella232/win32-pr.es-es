---
description: Puede Agregar compatibilidad de parámetros en tiempo de ejecución a un XAPO implementando la interfaz IXAPOParameters. La compatibilidad de parámetros en tiempo de ejecución permite a un XAPO cambiar su comportamiento en función de los parámetros que se le pasan en tiempo de ejecución.
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: 'Cómo: agregar compatibilidad con parámetros en tiempo de ejecución en un XAPO'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582f51b3dfbdc6d31422494906d5f945f77ccb03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497638"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a><span data-ttu-id="3185c-104">Cómo: agregar compatibilidad con parámetros en tiempo de ejecución en un XAPO</span><span class="sxs-lookup"><span data-stu-id="3185c-104">How to: Add Run-time Parameter Support to an XAPO</span></span>

<span data-ttu-id="3185c-105">Puede Agregar compatibilidad de parámetros en tiempo de ejecución a un XAPO implementando la interfaz [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) .</span><span class="sxs-lookup"><span data-stu-id="3185c-105">You can add run-time parameter support to an XAPO by implementing the [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interface.</span></span> <span data-ttu-id="3185c-106">La compatibilidad de parámetros en tiempo de ejecución permite a un XAPO cambiar su comportamiento en función de los parámetros que se le pasan en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="3185c-106">Run-time parameter support allows an XAPO to change its behavior based on the parameters passed to it at run time.</span></span>

1.  <span data-ttu-id="3185c-107">Siga los pasos [que se describen en cómo: crear un XAPO](how-to--create-an-xapo.md).</span><span class="sxs-lookup"><span data-stu-id="3185c-107">Follow the steps in [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>
2.  <span data-ttu-id="3185c-108">Cambie XAPO para que derive de [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) y [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).</span><span class="sxs-lookup"><span data-stu-id="3185c-108">Change the XAPO to derive from [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) and [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).</span></span>
3.  <span data-ttu-id="3185c-109">Agregue llamadas a los métodos [**CXAPOParametersBase:: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) y [**CXAPOParametersBase:: EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) a la implementación de [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span><span class="sxs-lookup"><span data-stu-id="3185c-109">Add calls to the methods [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) and [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) to the implementation of [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span></span>

    > [!Note]  
    > <span data-ttu-id="3185c-110">Agregar estos métodos a [IXAPO::P rador](how-to--build-a-basic-audio-processing-graph.md) permite a [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) mantener sus copias de los parámetros de efecto en un estado seguro para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="3185c-110">Adding these methods to [IXAPO::Process](how-to--build-a-basic-audio-processing-graph.md) allows [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) to keep its copies of the effect parameters in a thread-safe state.</span></span> <span data-ttu-id="3185c-111">Llame a [**CXAPOParametersBase:: BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) al principio de [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process)y [**CXAPOParametersBase:: EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) al final de **IXAPO::P rador**.</span><span class="sxs-lookup"><span data-stu-id="3185c-111">Call [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) at the beginning of [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process), and [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) at the end of **IXAPO::Process**.</span></span>

     

4.  <span data-ttu-id="3185c-112">Agregue más código a la implementación [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) para cambiar su comportamiento en función de los valores almacenados por el método [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) .</span><span class="sxs-lookup"><span data-stu-id="3185c-112">Add more code to the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) implementation to change its behavior according to values stored by the [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) method.</span></span>

    > [!Note]  
    > <span data-ttu-id="3185c-113">Agregar código al método [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process) para usar los parámetros especificados por [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) permite cambiar el comportamiento del XAPO a lo largo de su vida.</span><span class="sxs-lookup"><span data-stu-id="3185c-113">Adding code to the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method to use the parameters specified by [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) allows the XAPO's behavior to be changed throughout its life.</span></span>

     

5.  <span data-ttu-id="3185c-114">Cuando se crea una instancia del efecto, se asigna un búfer de tres de las estructuras que representan los parámetros del efecto y se pasa al constructor [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) .</span><span class="sxs-lookup"><span data-stu-id="3185c-114">When you create an instance of the effect, allocate a buffer of three of the structures that will represent the effect's parameters, and pass it to the [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) constructor.</span></span>

    > [!Note]  
    > <span data-ttu-id="3185c-115">La instancia de [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) usa internamente este búfer para administrar los parámetros de efecto que se le pasan cuando se llama a [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters).</span><span class="sxs-lookup"><span data-stu-id="3185c-115">The [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) instance internally uses this buffer to manage effect parameters passed to it when you call [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters).</span></span> <span data-ttu-id="3185c-116">Debe inicializar todos los bloques de parámetros de proceso de *pParameterBlocks* en el mismo valor predeterminado antes de llamar a cualquiera de los métodos [**IXAPO::P rador**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters:: GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)y **IXAPOParameters:: SetParameters** .</span><span class="sxs-lookup"><span data-stu-id="3185c-116">You must initialize all the process parameter blocks in *pParameterBlocks* to the same default value before you call any of the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters::GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters), and **IXAPOParameters::SetParameters** methods.</span></span> <span data-ttu-id="3185c-117">Normalmente, esta inicialización se controla en [**IXAPO:: Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) o en [**IXAPO:: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).</span><span class="sxs-lookup"><span data-stu-id="3185c-117">Usually this initialization is handled in [**IXAPO::Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) or in [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="3185c-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3185c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3185c-119">Efectos de audio</span><span class="sxs-lookup"><span data-stu-id="3185c-119">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="3185c-120">Información general de XAPO</span><span class="sxs-lookup"><span data-stu-id="3185c-120">XAPO Overview</span></span>](xapo-overview.md)
</dt> </dl>

 

 
