---
description: 'La interfaz ISampleGrabberCB proporciona métodos de devolución de llamada para el método ISampleGrabber:: SetCallback. Si la aplicación llama a este método, debe implementar esta interfaz. Para obtener más información, vea ISampleGrabber.'
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: Interfaz ISampleGrabberCB (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5c39d11e6560bc5e50a4c8a9b42a1cbb095b4b71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679271"
---
# <a name="isamplegrabbercb-interface"></a><span data-ttu-id="44339-105">Interfaz ISampleGrabberCB</span><span class="sxs-lookup"><span data-stu-id="44339-105">ISampleGrabberCB interface</span></span>

> [!Note]  
> <span data-ttu-id="44339-106">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="44339-106">\[Deprecated.</span></span> <span data-ttu-id="44339-107">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="44339-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="44339-108">La `ISampleGrabberCB` interfaz proporciona métodos de devolución de llamada para el método [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md) .</span><span class="sxs-lookup"><span data-stu-id="44339-108">The `ISampleGrabberCB` interface provides callback methods for the [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) method.</span></span> <span data-ttu-id="44339-109">Si la aplicación llama a este método, debe implementar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="44339-109">If your application calls that method, it must implement this interface.</span></span> <span data-ttu-id="44339-110">Para obtener más información, vea [**ISampleGrabber**](isamplegrabber.md).</span><span class="sxs-lookup"><span data-stu-id="44339-110">For more information, see [**ISampleGrabber**](isamplegrabber.md).</span></span>

## <a name="members"></a><span data-ttu-id="44339-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="44339-111">Members</span></span>

<span data-ttu-id="44339-112">La interfaz **ISampleGrabberCB** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="44339-112">The **ISampleGrabberCB** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="44339-113">**ISampleGrabberCB** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="44339-113">**ISampleGrabberCB** also has these types of members:</span></span>

-   [<span data-ttu-id="44339-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="44339-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="44339-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="44339-115">Methods</span></span>

<span data-ttu-id="44339-116">La interfaz **ISampleGrabberCB** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="44339-116">The **ISampleGrabberCB** interface has these methods.</span></span>



| <span data-ttu-id="44339-117">Método</span><span class="sxs-lookup"><span data-stu-id="44339-117">Method</span></span>                                        | <span data-ttu-id="44339-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="44339-118">Description</span></span>                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="44339-119">**BufferCB**</span><span class="sxs-lookup"><span data-stu-id="44339-119">**BufferCB**</span></span>](isamplegrabbercb-buffercb.md) | <span data-ttu-id="44339-120">Método de devolución de llamada que recibe un puntero al búfer de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="44339-120">Callback method that receives a pointer to the sample buffer.</span></span><br/> |
| [<span data-ttu-id="44339-121">**SampleCB**</span><span class="sxs-lookup"><span data-stu-id="44339-121">**SampleCB**</span></span>](isamplegrabbercb-samplecb.md) | <span data-ttu-id="44339-122">Método de devolución de llamada que recibe un puntero al ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="44339-122">Callback method that receives a pointer to the media sample.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="44339-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44339-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="44339-124">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="44339-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="44339-125">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="44339-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="44339-126">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="44339-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="44339-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44339-127">Requirements</span></span>



| <span data-ttu-id="44339-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="44339-128">Requirement</span></span> | <span data-ttu-id="44339-129">Value</span><span class="sxs-lookup"><span data-stu-id="44339-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44339-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44339-130">Header</span></span><br/>  | <dl> <span data-ttu-id="44339-131"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="44339-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="44339-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44339-132">Library</span></span><br/> | <dl> <span data-ttu-id="44339-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44339-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
