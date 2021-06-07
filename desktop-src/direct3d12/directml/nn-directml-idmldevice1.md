---
UID: NN:directml.IDMLDevice1
title: IDMLDevice1
description: Representa un dispositivo DirectML, que se usa para crear operadores, tablas de enlace, grabadoras de comandos y otros objetos.
helpviewer_keywords:
- IDMLDevice1
- IDMLDevice1 interface
- IDMLDevice1 interface
- described
- direct3d12.idmldevice1
- directml/IDMLDevice1
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
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDMLDevice1
- directml/IDMLDevice1
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- DirectML.h
api_name:
- IDMLDevice1
ms.openlocfilehash: 7a10cf2c9fe683775d163c7b5cb0e30fe07de08f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417941"
---
# <a name="idmldevice1-interface-directmlh"></a><span data-ttu-id="e26d5-103">Interfaz IDMLDevice1 (directml.h)</span><span class="sxs-lookup"><span data-stu-id="e26d5-103">IDMLDevice1 interface (directml.h)</span></span>

<span data-ttu-id="e26d5-104">Representa un dispositivo DirectML, que se usa para crear operadores, tablas de enlace, grabadoras de comandos y otros objetos.</span><span class="sxs-lookup"><span data-stu-id="e26d5-104">Represents a DirectML device, which is used to create operators, binding tables, command recorders, and other objects.</span></span> <span data-ttu-id="e26d5-105">La **interfaz IDMLDevice1** hereda de [IDMLDevice.](/windows/win32/api/directml/nn-directml-idmldevice)</span><span class="sxs-lookup"><span data-stu-id="e26d5-105">The **IDMLDevice1** interface inherits from [IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice).</span></span>

<span data-ttu-id="e26d5-106">Un dispositivo DirectML siempre está asociado a exactamente un dispositivo Direct3D 12 subyacente.</span><span class="sxs-lookup"><span data-stu-id="e26d5-106">A DirectML device is always associated with exactly one underlying Direct3D 12 device.</span></span> <span data-ttu-id="e26d5-107">Todos los objetos creados por el dispositivo DirectML mantienen una referencia segura a su dispositivo primario.</span><span class="sxs-lookup"><span data-stu-id="e26d5-107">All objects created by the DirectML device maintain a strong reference to their parent device.</span></span> <span data-ttu-id="e26d5-108">A diferencia del dispositivo Direct3D 12, el dispositivo DML no es un singleton.</span><span class="sxs-lookup"><span data-stu-id="e26d5-108">Unlike the Direct3D 12 device, the DML device is not a singleton.</span></span> <span data-ttu-id="e26d5-109">Por lo tanto, es posible crear varios dispositivos DirectML en el mismo dispositivo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e26d5-109">Therefore, it's possible to create multiple DirectML devices over the same Direct3D 12 device.</span></span> <span data-ttu-id="e26d5-110">Sin embargo, esto no se recomienda, ya que el dispositivo DirectML no tiene ningún estado mutable, por lo que no hay ninguna ventaja para crear varios dispositivos DML en el mismo dispositivo Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="e26d5-110">However, this isn't recommended as the DirectML device has no mutable state, so there's little advantage to creating multiple DML devices over the same Direct3D 12 device.</span></span>

<span data-ttu-id="e26d5-111">Este objeto es seguro para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="e26d5-111">This object is thread-safe.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e26d5-112">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="e26d5-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="e26d5-113">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="e26d5-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="availability"></a><span data-ttu-id="e26d5-114">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="e26d5-114">Availability</span></span>
<span data-ttu-id="e26d5-115">Esta API se introdujo en la versión de `1.1.0` DirectML.</span><span class="sxs-lookup"><span data-stu-id="e26d5-115">This API was introduced in DirectML version `1.1.0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="e26d5-116">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="e26d5-116">Tensor constraints</span></span>
<span data-ttu-id="e26d5-117">**Plataforma de destino:** Windows</span><span class="sxs-lookup"><span data-stu-id="e26d5-117">**Target Platform**: Windows</span></span>


## <a name="inheritance"></a><span data-ttu-id="e26d5-118">Herencia</span><span class="sxs-lookup"><span data-stu-id="e26d5-118">Inheritance</span></span>


<span data-ttu-id="e26d5-119">La interfaz IDMLDevice1 hereda de la interfaz IDMLDevice.</span><span class="sxs-lookup"><span data-stu-id="e26d5-119">The IDMLDevice1 interface inherits from the IDMLDevice interface.</span></span>



## <a name="methods"></a><span data-ttu-id="e26d5-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="e26d5-120">Methods</span></span>

<p><span data-ttu-id="e26d5-121">La <b>interfaz IDMLDevice1</b> tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e26d5-121">The <b>IDMLDevice1</b> interface has these methods.</span></span></p>

| <span data-ttu-id="e26d5-122">Método</span><span class="sxs-lookup"><span data-stu-id="e26d5-122">Method</span></span> | <span data-ttu-id="e26d5-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="e26d5-123">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="e26d5-124">IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="e26d5-124">IDMLDevice1::CompileGraph</span></span>](../directml/nf-directml-idmldevice1-compilegraph.md) | <span data-ttu-id="e26d5-125">Compila un gráfico de operadores de DirectML en un objeto que se puede enviar a la GPU.</span><span class="sxs-lookup"><span data-stu-id="e26d5-125">Compiles a graph of DirectML operators into an object that can be dispatched to the GPU.</span></span> |


## <a name="requirements"></a><span data-ttu-id="e26d5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e26d5-126">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e26d5-127">**Plataforma de destino**</span><span class="sxs-lookup"><span data-stu-id="e26d5-127">**Target Platform**</span></span> | <span data-ttu-id="e26d5-128">Windows</span><span class="sxs-lookup"><span data-stu-id="e26d5-128">Windows</span></span> |
| <span data-ttu-id="e26d5-129">**Header**</span><span class="sxs-lookup"><span data-stu-id="e26d5-129">**Header**</span></span> | <span data-ttu-id="e26d5-130">directml.h</span><span class="sxs-lookup"><span data-stu-id="e26d5-130">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="e26d5-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e26d5-131">See also</span></span>

[<span data-ttu-id="e26d5-132">Interfaz IDMLDevice</span><span class="sxs-lookup"><span data-stu-id="e26d5-132">IDMLDevice interface</span></span>](/windows/win32/api/directml/nn-directml-idmldevice)