---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: Compila un grafo de operadores de DirectML en un objeto que se puede enviar a la GPU.
helpviewer_keywords:
- CompileGraph
- CompileGraph method
- CompileGraph method
- IDMLDevice1 interface
- IDMLDevice1 interface
- CompileGraph method
- IDMLDevice1.CompileGraph
- IDMLDevice1::CompileGraph
- direct3d12.idmldevice1_compileoperator
- directml/IDMLDevice1::CompileGraph
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1::CompileGraph
- directml/IDMLDevice1::CompileGraph
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.dll
api_name:
- IDMLDevice1.CompileGraph
ms.openlocfilehash: 25dbc62fac9cd38d9728a295e336038441aee19f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721214"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a><span data-ttu-id="9fa73-103">IDMLDevice1:: CompileGraph (método) (directml. h)</span><span class="sxs-lookup"><span data-stu-id="9fa73-103">IDMLDevice1::CompileGraph method (directml.h)</span></span>

<span data-ttu-id="9fa73-104">Compila un grafo de operadores de DirectML en un objeto que se puede enviar a la GPU.</span><span class="sxs-lookup"><span data-stu-id="9fa73-104">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span>

<span data-ttu-id="9fa73-105">Un operador compilado representa la forma eficaz y horneada de un operador adecuado para su ejecución en la GPU.</span><span class="sxs-lookup"><span data-stu-id="9fa73-105">A compiled operator represents the efficient, baked form of an operator suitable for execution on the GPU.</span></span> <span data-ttu-id="9fa73-106">Un operador compilado mantiene el estado (como los sombreadores y otros objetos) necesarios para la ejecución.</span><span class="sxs-lookup"><span data-stu-id="9fa73-106">A compiled operator holds state (such as shaders and other objects) required for execution.</span></span> <span data-ttu-id="9fa73-107">Dado que un operador compilado implementa la interfaz [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) , puede expulsar una de la memoria de GPU si lo desea.</span><span class="sxs-lookup"><span data-stu-id="9fa73-107">Because a compiled operator implements the [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) interface, you're able to evict one from GPU memory if you wish.</span></span> <span data-ttu-id="9fa73-108">Vea [IDMLDevice1:: expulsión](/windows/win32/api/directml/nf-directml-idmldevice-evict) y [IDMLDevice1:: MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9fa73-108">See [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) and [IDMLDevice1::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) for more info.</span></span>

<span data-ttu-id="9fa73-109">El operador compilado no usa ni hace referencia a los objetos [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) proporcionados en la descripción del gráfico después de que este método devuelva.</span><span class="sxs-lookup"><span data-stu-id="9fa73-109">The compiled operator doesn't use nor reference the [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) objects supplied within the graph description after this method returns.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fa73-110">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="9fa73-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="9fa73-111">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="9fa73-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9fa73-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fa73-112">Syntax</span></span>

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="9fa73-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fa73-113">Parameters</span></span>

`desc`

<span data-ttu-id="9fa73-114">Tipo: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="9fa73-114">Type: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span></span>

<span data-ttu-id="9fa73-115">Descripción del gráfico que se va a compilar.</span><span class="sxs-lookup"><span data-stu-id="9fa73-115">A description of the graph to compile.</span></span> <span data-ttu-id="9fa73-116">Vea [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span><span class="sxs-lookup"><span data-stu-id="9fa73-116">See [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span></span>

`flags`

<span data-ttu-id="9fa73-117">Tipo: [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span><span class="sxs-lookup"><span data-stu-id="9fa73-117">Type: [**DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span></span>

<span data-ttu-id="9fa73-118">Cualquier marcador para controlar la ejecución de este operador.</span><span class="sxs-lookup"><span data-stu-id="9fa73-118">Any flags to control the execution of this operator.</span></span>

`riid`

<span data-ttu-id="9fa73-119">Tipo: <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="9fa73-119">Type: <b>REFIID</b></span></span>

<span data-ttu-id="9fa73-120">Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en <i>PPV</i>.</span><span class="sxs-lookup"><span data-stu-id="9fa73-120">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>.</span></span> <span data-ttu-id="9fa73-121">Se espera que sea el GUID de [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).</span><span class="sxs-lookup"><span data-stu-id="9fa73-121">This is expected to be the GUID of [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).</span></span>

`ppv`

<span data-ttu-id="9fa73-122">Tipo: <b>void \* \*</b></span><span class="sxs-lookup"><span data-stu-id="9fa73-122">Type: <b>void\*\*</b></span></span>

<span data-ttu-id="9fa73-123">Un puntero a un bloque de memoria que recibe un puntero al operador compilado.</span><span class="sxs-lookup"><span data-stu-id="9fa73-123">A pointer to a memory block that receives a pointer to the compiled operator.</span></span> <span data-ttu-id="9fa73-124">Se trata de la dirección de un puntero a un [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), que representa el operador compilado creado.</span><span class="sxs-lookup"><span data-stu-id="9fa73-124">This is the address of a pointer to an [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), representing  the compiled operator created.</span></span>


## <a name="return-value"></a><span data-ttu-id="9fa73-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fa73-125">Return value</span></span>

<span data-ttu-id="9fa73-126">Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="9fa73-126">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="9fa73-127">Si este método se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="9fa73-127">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="9fa73-128">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9fa73-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fa73-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fa73-129">Remarks</span></span>

<span data-ttu-id="9fa73-130">La API del operador DirectML proporciona una manera abstracta de usar DirectML de forma eficaz en diverso hardware.</span><span class="sxs-lookup"><span data-stu-id="9fa73-130">The DirectML operator graph API provides an abstract way to use DirectML efficiently across diverse hardware.</span></span> <span data-ttu-id="9fa73-131">DirectML aplica optimizaciones de nivel de tensores, como elegir el diseño de tensores más eficaz basado en el adaptador que se está usando.</span><span class="sxs-lookup"><span data-stu-id="9fa73-131">DirectML applies tensor-level optimizations such as choosing the most efficient tensor layout based on the adapter being used.</span></span> <span data-ttu-id="9fa73-132">También aplica optimizaciones como la eliminación de operadores de combinación o de división.</span><span class="sxs-lookup"><span data-stu-id="9fa73-132">It also applies optimizations such as the removal of Join or Split operators.</span></span>

<span data-ttu-id="9fa73-133">Se recomienda aplicar optimizaciones de alto nivel antes de compilar un gráfico de DirectML.</span><span class="sxs-lookup"><span data-stu-id="9fa73-133">We recommend that you apply high-level optimizations before building a DirectML graph.</span></span> <span data-ttu-id="9fa73-134">Por ejemplo, fusionar operadores de convolución con BatchNorm, plegamiento de constantes y eliminación común de subexpresiones.</span><span class="sxs-lookup"><span data-stu-id="9fa73-134">For example, fusing Convolution operators with BatchNorm, constant folding, and common subexpression elimination.</span></span> <span data-ttu-id="9fa73-135">Las optimizaciones del optimizador de gráficos de DirectML están diseñadas para complementar estas optimizaciones independientes del dispositivo, que normalmente se administran de forma genérica mediante marcos de aprendizaje automático.</span><span class="sxs-lookup"><span data-stu-id="9fa73-135">The optimizations within DirectML's graph optimizer are intended to complement such device-independent optimizations, which are typically handled generically by machine learning frameworks.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fa73-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fa73-136">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9fa73-137">**Plataforma de destino**</span><span class="sxs-lookup"><span data-stu-id="9fa73-137">**Target Platform**</span></span> | <span data-ttu-id="9fa73-138">Windows</span><span class="sxs-lookup"><span data-stu-id="9fa73-138">Windows</span></span> |
| <span data-ttu-id="9fa73-139">**Header**</span><span class="sxs-lookup"><span data-stu-id="9fa73-139">**Header**</span></span> | <span data-ttu-id="9fa73-140">directml. h</span><span class="sxs-lookup"><span data-stu-id="9fa73-140">directml.h</span></span> |
| <span data-ttu-id="9fa73-141">**Library**</span><span class="sxs-lookup"><span data-stu-id="9fa73-141">**Library**</span></span> | <span data-ttu-id="9fa73-142">DirectML. lib</span><span class="sxs-lookup"><span data-stu-id="9fa73-142">DirectML.lib</span></span> |
| <span data-ttu-id="9fa73-143">**DLL**</span><span class="sxs-lookup"><span data-stu-id="9fa73-143">**DLL**</span></span> | <span data-ttu-id="9fa73-144">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="9fa73-144">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="9fa73-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fa73-145">See also</span></span>

[<span data-ttu-id="9fa73-146">IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="9fa73-146">IDMLDevice1</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)