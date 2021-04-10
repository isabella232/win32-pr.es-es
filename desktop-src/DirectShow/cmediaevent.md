---
description: La clase CMediaEvent proporciona la implementación de la clase base de los métodos IDispatch del IMediaEvent de interfaz dual. Deja como virtual pura las propiedades y los métodos de la interfaz IMediaEvent.
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: Clase CMediaEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 927e561fa557ac33b1669ca7353377f7814ca448
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279830"
---
# <a name="cmediaevent-class"></a><span data-ttu-id="658b8-104">Clase CMediaEvent</span><span class="sxs-lookup"><span data-stu-id="658b8-104">CMediaEvent class</span></span>

![jerarquía de clases cmediaevent](images/cutil03.png)

<span data-ttu-id="658b8-106">La `CMediaEvent` clase proporciona la implementación de la clase base de los métodos **IDispatch** del [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)de interfaz dual.</span><span class="sxs-lookup"><span data-stu-id="658b8-106">The `CMediaEvent` class provides base class implementation of the **IDispatch** methods of the dual-interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span></span> <span data-ttu-id="658b8-107">Deja como virtual pura las propiedades y los métodos de la interfaz **IMediaEvent** .</span><span class="sxs-lookup"><span data-stu-id="658b8-107">It leaves as pure virtual the properties and methods of the **IMediaEvent** interface.</span></span>

<span data-ttu-id="658b8-108">La `CMediaEvent` clase también proporciona la implementación de la clase base de la interfaz [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) que se deriva de [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span><span class="sxs-lookup"><span data-stu-id="658b8-108">The `CMediaEvent` class also provides base class implementation of the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface which derives from [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span></span>

<span data-ttu-id="658b8-109">Las funciones miembro [**CMediaEvent:: GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent:: GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent:: GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)y [**CMediaEvent:: Invoke**](cmediaevent-invoke.md) son implementaciones estándar de la interfaz **IDispatch** mediante la clase [**CBaseDispatch**](cbasedispatch.md) (y una biblioteca de tipos) para analizar los comandos y pasarlos a los métodos virtuales puros de la interfaz [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="658b8-109">The [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent::GetTypeInfoCount**](cmediaevent-gettypeinfocount.md), and [**CMediaEvent::Invoke**](cmediaevent-invoke.md) member functions are standard implementations of the **IDispatch** interface using the [**CBaseDispatch**](cbasedispatch.md) class (and a type library) to parse the commands and pass them to the pure virtual methods of the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface.</span></span>



| <span data-ttu-id="658b8-110">Funciones de miembro</span><span class="sxs-lookup"><span data-stu-id="658b8-110">Member Functions</span></span>                                         | <span data-ttu-id="658b8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="658b8-111">Description</span></span>                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="658b8-112">**CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="658b8-112">**CMediaEvent**</span></span>](cmediaevent-cmediaevent.md)           | <span data-ttu-id="658b8-113">Construye un objeto **CMediaEvent** .</span><span class="sxs-lookup"><span data-stu-id="658b8-113">Constructs a **CMediaEvent** object.</span></span>                                                                                                                                                          |
| <span data-ttu-id="658b8-114">Métodos IDispatch</span><span class="sxs-lookup"><span data-stu-id="658b8-114">IDispatch Methods</span></span>                                        | <span data-ttu-id="658b8-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="658b8-115">Description</span></span>                                                                                                                                                                                   |
| [<span data-ttu-id="658b8-116">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="658b8-116">**GetIDsOfNames**</span></span>](cmediaevent-getidsofnames.md)       | <span data-ttu-id="658b8-117">Asigna un solo miembro y un conjunto opcional de parámetros a un conjunto correspondiente de identificadores de envío enteros, que se puede usar durante las llamadas subsiguientes al método **IDispatch:: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="658b8-117">Maps a single member and an optional set of parameters to a corresponding set of integer dispatch identifiers, which can be used during subsequent calls to the **IDispatch::Invoke** method.</span></span> |
| [<span data-ttu-id="658b8-118">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="658b8-118">**GetTypeInfo**</span></span>](cmediaevent-gettypeinfo.md)           | <span data-ttu-id="658b8-119">Recupera un objeto de información de tipo, que recupera la información de tipo de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="658b8-119">Retrieves a type-information object, which retrieves the type information for an interface.</span></span>                                                                                                   |
| [<span data-ttu-id="658b8-120">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="658b8-120">**GetTypeInfoCount**</span></span>](cmediaevent-gettypeinfocount.md) | <span data-ttu-id="658b8-121">Recupera el número de interfaces de información de tipo proporcionado por un objeto.</span><span class="sxs-lookup"><span data-stu-id="658b8-121">Retrieves the number of type-information interfaces provided by an object.</span></span>                                                                                                                    |
| [<span data-ttu-id="658b8-122">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="658b8-122">**Invoke**</span></span>](cmediaevent-invoke.md)                     | <span data-ttu-id="658b8-123">Proporciona acceso a las propiedades y los métodos expuestos por un objeto.</span><span class="sxs-lookup"><span data-stu-id="658b8-123">Provides access to properties and methods exposed by an object.</span></span>                                                                                                                               |



 

 

 



