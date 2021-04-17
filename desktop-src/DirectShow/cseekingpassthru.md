---
description: La clase CSeekingPassThru es un objeto auxiliar que crea objetos CPosPassThru y CRendererPosPassThru.
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: Clase CSeekingPassThru (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 273f9b6686c4455452924dc43628801fae5d518a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690002"
---
# <a name="cseekingpassthru-class"></a><span data-ttu-id="56cc5-103">Clase CSeekingPassThru</span><span class="sxs-lookup"><span data-stu-id="56cc5-103">CSeekingPassThru class</span></span>

<span data-ttu-id="56cc5-104">La `CSeekingPassThru` clase es un objeto auxiliar que crea objetos [**CPosPassThru**](cpospassthru.md) y [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="56cc5-104">The `CSeekingPassThru` class is a helper object that creates [**CPosPassThru**](cpospassthru.md) and [**CRendererPosPassThru**](crendererpospassthru.md) objects.</span></span>

<span data-ttu-id="56cc5-105">Las clases **CPosPassThru** y **CRendererPosPassThru** son objetos auxiliares que pasan los comandos de búsqueda ascendentes, por lo que la `CSeekingPassThru` clase es un objeto auxiliar para crear objetos auxiliares.</span><span class="sxs-lookup"><span data-stu-id="56cc5-105">The **CPosPassThru** and **CRendererPosPassThru** classes are helper objects that pass seeking commands upstream, so the `CSeekingPassThru` class is a helper object for creating helper objects.</span></span>

<span data-ttu-id="56cc5-106">No es necesario usar esta clase directamente.</span><span class="sxs-lookup"><span data-stu-id="56cc5-106">It is not necessary to use this class directly.</span></span> <span data-ttu-id="56cc5-107">En su lugar, use la función [**CreatePosPassThru**](createpospassthru.md) , que controla todos los detalles del uso de esta clase.</span><span class="sxs-lookup"><span data-stu-id="56cc5-107">Instead, use the [**CreatePosPassThru**](createpospassthru.md) function, which handles all of the details of using this class.</span></span> <span data-ttu-id="56cc5-108">Tiene más ventajas de cargar el objeto desde Quartz.dll, lo que reduce ligeramente el tamaño del código del filtro.</span><span class="sxs-lookup"><span data-stu-id="56cc5-108">It has the further advantage of loading the object from Quartz.dll, which reduces the code size of your filter somewhat.</span></span> <span data-ttu-id="56cc5-109">Para obtener más información, vea [**CPosPassThru**](cpospassthru.md).</span><span class="sxs-lookup"><span data-stu-id="56cc5-109">For more information, see [**CPosPassThru**](cpospassthru.md).</span></span>

<span data-ttu-id="56cc5-110">La `CSeekingPassThru` clase expone la interfaz [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) .</span><span class="sxs-lookup"><span data-stu-id="56cc5-110">The `CSeekingPassThru` class exposes the [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) interface.</span></span> <span data-ttu-id="56cc5-111">El método [**ISeekingPassThru:: init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) inicializa el objeto.</span><span class="sxs-lookup"><span data-stu-id="56cc5-111">The [**ISeekingPassThru::Init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init) method initializes the object.</span></span> <span data-ttu-id="56cc5-112">Una vez inicializado el objeto, el filtro puede consultarlo para las interfaces [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) y [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .</span><span class="sxs-lookup"><span data-stu-id="56cc5-112">After the object is initialized, the filter can query it for the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) and [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interfaces.</span></span>



| <span data-ttu-id="56cc5-113">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="56cc5-113">Public Methods</span></span>                                                  | <span data-ttu-id="56cc5-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="56cc5-114">Description</span></span>                        |
|-----------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="56cc5-115">**CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="56cc5-115">**CSeekingPassThru**</span></span>](cseekingpassthru-cseekingpassthru.md)   | <span data-ttu-id="56cc5-116">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="56cc5-116">Constructor method.</span></span>                |
| [<span data-ttu-id="56cc5-117">**~ CSeekingPassThru**</span><span class="sxs-lookup"><span data-stu-id="56cc5-117">**~CSeekingPassThru**</span></span>](cseekingpassthru--cseekingpassthru.md) | <span data-ttu-id="56cc5-118">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="56cc5-118">Destructor method.</span></span>                 |
| [<span data-ttu-id="56cc5-119">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="56cc5-119">**CreateInstance**</span></span>](cseekingpassthru-createinstance.md)       | <span data-ttu-id="56cc5-120">Crea una instancia del objeto.</span><span class="sxs-lookup"><span data-stu-id="56cc5-120">Creates an instance of the object.</span></span> |
| <span data-ttu-id="56cc5-121">Métodos ISeekingPassThru</span><span class="sxs-lookup"><span data-stu-id="56cc5-121">ISeekingPassThru Methods</span></span>                                        | <span data-ttu-id="56cc5-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="56cc5-122">Description</span></span>                        |
| [<span data-ttu-id="56cc5-123">**Smss**</span><span class="sxs-lookup"><span data-stu-id="56cc5-123">**Init**</span></span>](cseekingpassthru-init.md)                           | <span data-ttu-id="56cc5-124">Inicializa el objeto.</span><span class="sxs-lookup"><span data-stu-id="56cc5-124">Initializes the object.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="56cc5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56cc5-125">Requirements</span></span>



| <span data-ttu-id="56cc5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="56cc5-126">Requirement</span></span> | <span data-ttu-id="56cc5-127">Value</span><span class="sxs-lookup"><span data-stu-id="56cc5-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56cc5-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56cc5-128">Header</span></span><br/>  | <dl> <span data-ttu-id="56cc5-129"><dt>Seekpt. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56cc5-129"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="56cc5-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56cc5-130">Library</span></span><br/> | <dl> <span data-ttu-id="56cc5-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="56cc5-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




