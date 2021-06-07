---
UID: NF:directml.IDMLDevice1.CompileGraph
title: IDMLDevice1::CompileGraph
description: Compila un gráfico de operadores de DirectML en un objeto que se puede enviar a la GPU.
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
ms.openlocfilehash: 8a9b4ce9bd8f8bd8b1d6f2a6bbd144009eb0d79d
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417940"
---
# <a name="idmldevice1compilegraph-method-directmlh"></a><span data-ttu-id="50525-103">Método IDMLDevice1::CompileGraph (directml.h)</span><span class="sxs-lookup"><span data-stu-id="50525-103">IDMLDevice1::CompileGraph method (directml.h)</span></span>

<span data-ttu-id="50525-104">Compila un gráfico de operadores de DirectML en un objeto que se puede enviar a la GPU.</span><span class="sxs-lookup"><span data-stu-id="50525-104">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span>

<span data-ttu-id="50525-105">Un operador compilado representa la forma eficaz y al día de un operador adecuado para su ejecución en la GPU.</span><span class="sxs-lookup"><span data-stu-id="50525-105">A compiled operator represents the efficient, baked form of an operator suitable for execution on the GPU.</span></span> <span data-ttu-id="50525-106">Un operador compilado contiene el estado (como sombreadores y otros objetos) necesario para la ejecución.</span><span class="sxs-lookup"><span data-stu-id="50525-106">A compiled operator holds state (such as shaders and other objects) required for execution.</span></span> <span data-ttu-id="50525-107">Dado que un operador compilado implementa la interfaz [IDMLPageable,](/windows/win32/api/directml/nn-directml-idmlpageable) puede expulsar una de la memoria de GPU si lo desea.</span><span class="sxs-lookup"><span data-stu-id="50525-107">Because a compiled operator implements the [IDMLPageable](/windows/win32/api/directml/nn-directml-idmlpageable) interface, you're able to evict one from GPU memory if you wish.</span></span> <span data-ttu-id="50525-108">Vea [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) e [IDMLDevice1::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="50525-108">See [IDMLDevice1::Evict](/windows/win32/api/directml/nf-directml-idmldevice-evict) and [IDMLDevice1::MakeResident](/windows/win32/api/directml/nf-directml-idmldevice-makeresident) for more info.</span></span>

<span data-ttu-id="50525-109">El operador compilado no usa ni hace referencia a los objetos [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) proporcionados en la descripción del gráfico después de que este método vuelva.</span><span class="sxs-lookup"><span data-stu-id="50525-109">The compiled operator doesn't use nor reference the [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator) objects supplied within the graph description after this method returns.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50525-110">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="50525-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="50525-111">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="50525-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="50525-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50525-112">Syntax</span></span>

```cpp
HRESULT CompileGraph(
  const DML_GRAPH_DESC *desc,
  DML_EXECUTION_FLAGS  flags,
  REFIID               riid,
  void                 **ppv
);
```

## <a name="parameters"></a><span data-ttu-id="50525-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50525-113">Parameters</span></span>

`desc`

<span data-ttu-id="50525-114">Tipo: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="50525-114">Type: **[DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)\***</span></span>

<span data-ttu-id="50525-115">Descripción del gráfico que se compilará.</span><span class="sxs-lookup"><span data-stu-id="50525-115">A description of the graph to compile.</span></span> <span data-ttu-id="50525-116">Vea [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span><span class="sxs-lookup"><span data-stu-id="50525-116">See [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md).</span></span>

`flags`

<span data-ttu-id="50525-117">Tipo: [ **DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span><span class="sxs-lookup"><span data-stu-id="50525-117">Type: [**DML_EXECUTION_FLAGS**](/windows/win32/api/directml/ne-directml-dml_execution_flags)</span></span>

<span data-ttu-id="50525-118">Cualquier marca para controlar la ejecución de este operador.</span><span class="sxs-lookup"><span data-stu-id="50525-118">Any flags to control the execution of this operator.</span></span>

`riid`

<span data-ttu-id="50525-119">Tipo: <b>REFIID</b></span><span class="sxs-lookup"><span data-stu-id="50525-119">Type: <b>REFIID</b></span></span>

<span data-ttu-id="50525-120">Referencia al identificador único global (GUID) de la interfaz que desea que se devuelva en <i>ppv.</i></span><span class="sxs-lookup"><span data-stu-id="50525-120">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in <i>ppv</i>.</span></span> <span data-ttu-id="50525-121">Se espera que sea el GUID de [IDMLCompiledOperator.](/windows/win32/api/directml/nn-directml-idmlcompiledoperator)</span><span class="sxs-lookup"><span data-stu-id="50525-121">This is expected to be the GUID of [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator).</span></span>

`ppv`

<span data-ttu-id="50525-122">Tipo: <b>void\*\*</b></span><span class="sxs-lookup"><span data-stu-id="50525-122">Type: <b>void\*\*</b></span></span>

<span data-ttu-id="50525-123">Puntero a un bloque de memoria que recibe un puntero al operador compilado.</span><span class="sxs-lookup"><span data-stu-id="50525-123">A pointer to a memory block that receives a pointer to the compiled operator.</span></span> <span data-ttu-id="50525-124">Esta es la dirección de un puntero a [un IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), que representa el operador compilado creado.</span><span class="sxs-lookup"><span data-stu-id="50525-124">This is the address of a pointer to an [IDMLCompiledOperator](/windows/win32/api/directml/nn-directml-idmlcompiledoperator), representing  the compiled operator created.</span></span>


## <a name="return-value"></a><span data-ttu-id="50525-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50525-125">Return value</span></span>

<span data-ttu-id="50525-126">Tipo: [ **HRESULT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="50525-126">Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="50525-127">Si este método se realiza correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="50525-127">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="50525-128">De lo contrario, devuelve un código de error **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="50525-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="50525-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="50525-129">Remarks</span></span>

<span data-ttu-id="50525-130">Graph API de operador de DirectML proporciona una manera abstracta de usar DirectML de forma eficaz en diversos hardware.</span><span class="sxs-lookup"><span data-stu-id="50525-130">The DirectML operator graph API provides an abstract way to use DirectML efficiently across diverse hardware.</span></span> <span data-ttu-id="50525-131">DirectML aplica optimizaciones de nivel de tensor, como elegir el diseño de tensor más eficaz en función del adaptador que se usa.</span><span class="sxs-lookup"><span data-stu-id="50525-131">DirectML applies tensor-level optimizations such as choosing the most efficient tensor layout based on the adapter being used.</span></span> <span data-ttu-id="50525-132">También aplica optimizaciones como la eliminación de operadores Join o Split.</span><span class="sxs-lookup"><span data-stu-id="50525-132">It also applies optimizations such as the removal of Join or Split operators.</span></span>

<span data-ttu-id="50525-133">Se recomienda aplicar optimizaciones de alto nivel antes de crear un gráfico de DirectML.</span><span class="sxs-lookup"><span data-stu-id="50525-133">We recommend that you apply high-level optimizations before building a DirectML graph.</span></span> <span data-ttu-id="50525-134">Por ejemplo, la conversión de operadores de Convolution con BatchNorm, el plegado constante y la eliminación de subexpresión común.</span><span class="sxs-lookup"><span data-stu-id="50525-134">For example, fusing Convolution operators with BatchNorm, constant folding, and common subexpression elimination.</span></span> <span data-ttu-id="50525-135">Las optimizaciones del optimizador de grafos de DirectML están diseñadas para complementar dichas optimizaciones independientes del dispositivo, que normalmente se controlan de forma genérica mediante marcos de aprendizaje automático.</span><span class="sxs-lookup"><span data-stu-id="50525-135">The optimizations within DirectML's graph optimizer are intended to complement such device-independent optimizations, which are typically handled generically by machine learning frameworks.</span></span>

## <a name="requirements"></a><span data-ttu-id="50525-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50525-136">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="50525-137">**Plataforma de destino**</span><span class="sxs-lookup"><span data-stu-id="50525-137">**Target Platform**</span></span> | <span data-ttu-id="50525-138">Windows</span><span class="sxs-lookup"><span data-stu-id="50525-138">Windows</span></span> |
| <span data-ttu-id="50525-139">**Header**</span><span class="sxs-lookup"><span data-stu-id="50525-139">**Header**</span></span> | <span data-ttu-id="50525-140">directml.h</span><span class="sxs-lookup"><span data-stu-id="50525-140">directml.h</span></span> |
| <span data-ttu-id="50525-141">**Library**</span><span class="sxs-lookup"><span data-stu-id="50525-141">**Library**</span></span> | <span data-ttu-id="50525-142">DirectML.lib</span><span class="sxs-lookup"><span data-stu-id="50525-142">DirectML.lib</span></span> |
| <span data-ttu-id="50525-143">**Dll**</span><span class="sxs-lookup"><span data-stu-id="50525-143">**DLL**</span></span> | <span data-ttu-id="50525-144">DirectML.dll</span><span class="sxs-lookup"><span data-stu-id="50525-144">DirectML.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="50525-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="50525-145">See also</span></span>

[<span data-ttu-id="50525-146">IDMLDevice1</span><span class="sxs-lookup"><span data-stu-id="50525-146">IDMLDevice1</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)