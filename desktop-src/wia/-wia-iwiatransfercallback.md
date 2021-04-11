---
description: La interfaz IWiaTransferCallback recibe las devoluciones de llamada durante una transferencia de datos.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: Interfaz IWiaTransferCallback (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 918482ebcb24f2638a006ab1bbc452ea28ff61e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154392"
---
# <a name="iwiatransfercallback-interface"></a><span data-ttu-id="dea71-103">Interfaz IWiaTransferCallback</span><span class="sxs-lookup"><span data-stu-id="dea71-103">IWiaTransferCallback interface</span></span>

<span data-ttu-id="dea71-104">La interfaz **IWiaTransferCallback** recibe las devoluciones de llamada durante una transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="dea71-104">The **IWiaTransferCallback** interface receives callbacks during a data transfer.</span></span>

## <a name="members"></a><span data-ttu-id="dea71-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="dea71-105">Members</span></span>

<span data-ttu-id="dea71-106">La interfaz **IWiaTransferCallback** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dea71-106">The **IWiaTransferCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dea71-107">**IWiaTransferCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dea71-107">**IWiaTransferCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="dea71-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="dea71-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dea71-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="dea71-109">Methods</span></span>

<span data-ttu-id="dea71-110">La interfaz **IWiaTransferCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dea71-110">The **IWiaTransferCallback** interface has these methods.</span></span>



| <span data-ttu-id="dea71-111">Método</span><span class="sxs-lookup"><span data-stu-id="dea71-111">Method</span></span>                                                                 | <span data-ttu-id="dea71-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="dea71-112">Description</span></span>                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="dea71-113">**GetNextStream**</span><span class="sxs-lookup"><span data-stu-id="dea71-113">**GetNextStream**</span></span>](-wia-iwiatransfercallback-getnextstream.md)       | <span data-ttu-id="dea71-114">Obtiene una nueva secuencia para el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="dea71-114">Gets a new stream for the specified item.</span></span> <br/>                    |
| [<span data-ttu-id="dea71-115">**TransferCallback**</span><span class="sxs-lookup"><span data-stu-id="dea71-115">**TransferCallback**</span></span>](-wia-iwiatransfercallback-transfercallback.md) | <span data-ttu-id="dea71-116">Proporciona el progreso y otras notificaciones durante una transferencia.</span><span class="sxs-lookup"><span data-stu-id="dea71-116">Provides progress and other notifications during a transfer.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="dea71-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dea71-117">Remarks</span></span>

<span data-ttu-id="dea71-118">Los desarrolladores de filtros de procesamiento de imágenes deben implementar esta interfaz y la interfaz [**IWiaImageFilter**](-wia-iwiaimagefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="dea71-118">Image processing filter developers should implement this interface and the [**IWiaImageFilter**](-wia-iwiaimagefilter.md) interface.</span></span>

<span data-ttu-id="dea71-119">La interfaz **IWiaTransferCallback** , al igual que todas las interfaces del modelo de objetos componentes (com), hereda los métodos de interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dea71-119">The **IWiaTransferCallback** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="dea71-120">Métodos IUnknown</span><span class="sxs-lookup"><span data-stu-id="dea71-120">IUnknown Methods</span></span>                                        | <span data-ttu-id="dea71-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="dea71-121">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="dea71-122">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="dea71-122">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="dea71-123">Devuelve punteros a las interfaces compatibles.</span><span class="sxs-lookup"><span data-stu-id="dea71-123">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="dea71-124">IUnknown:: AddRef</span><span class="sxs-lookup"><span data-stu-id="dea71-124">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="dea71-125">Incrementa el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="dea71-125">Increments reference count.</span></span>               |
| [<span data-ttu-id="dea71-126">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="dea71-126">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="dea71-127">Reduce el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="dea71-127">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="dea71-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dea71-128">Requirements</span></span>



| <span data-ttu-id="dea71-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dea71-129">Requirement</span></span> | <span data-ttu-id="dea71-130">Value</span><span class="sxs-lookup"><span data-stu-id="dea71-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dea71-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dea71-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dea71-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="dea71-132">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="dea71-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dea71-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dea71-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="dea71-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dea71-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dea71-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dea71-136"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="dea71-136"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="dea71-137">IDL</span><span class="sxs-lookup"><span data-stu-id="dea71-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dea71-138"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dea71-138"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="dea71-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dea71-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="dea71-140"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dea71-140"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
