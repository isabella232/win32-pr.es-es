---
description: La clase CMediaControl proporciona el control de clases base de los métodos IDispatch de la interfaz dual IMediaControl. Deja como virtual pura las propiedades y los métodos de la interfaz IMediaControl.
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: Clase CMediaControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae3a528263af4bd2fe5e4eccbe28793799c373a0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914213"
---
# <a name="cmediacontrol-class"></a><span data-ttu-id="20b16-104">Clase CMediaControl</span><span class="sxs-lookup"><span data-stu-id="20b16-104">CMediaControl class</span></span>

![jerarquía de clases cmediacontrol](images/cutil02.png)

<span data-ttu-id="20b16-106">La `CMediaControl` clase proporciona el control de clases base de los métodos [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) de la interfaz dual [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol).</span><span class="sxs-lookup"><span data-stu-id="20b16-106">The `CMediaControl` class provides base class handling of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) methods of the dual-interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol).</span></span> <span data-ttu-id="20b16-107">Deja como virtual pura las propiedades y los métodos de la interfaz **IMediaControl** .</span><span class="sxs-lookup"><span data-stu-id="20b16-107">It leaves as pure virtual the properties and methods of the **IMediaControl** interface.</span></span>

<span data-ttu-id="20b16-108">Normalmente, el administrador de gráficos de filtros es el único objeto que implementa la interfaz [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .</span><span class="sxs-lookup"><span data-stu-id="20b16-108">Typically, the filter graph manager is the only object that implements the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface.</span></span> <span data-ttu-id="20b16-109">(los filtros implementan la interfaz [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) , heredada por [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), para recibir comandos de control del administrador de gráficos de filtros). Por lo tanto, esta biblioteca de clases es de uso limitado para filtrar a los desarrolladores.</span><span class="sxs-lookup"><span data-stu-id="20b16-109">(filters implement the [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) interface, inherited by [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), to receive control commands from the filter graph manager.) Therefore, this class library is of limited use to filter developers.</span></span>

<span data-ttu-id="20b16-110">Las funciones miembro [**CMediaControl:: GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl:: GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl:: GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)y [**CMediaControl:: Invoke**](cmediacontrol-invoke.md) son implementaciones estándar de los métodos [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) mediante la clase [**CBaseDispatch**](cbasedispatch.md) (y una biblioteca de tipos) para analizar los comandos y pasarlos a los métodos virtuales puros de la interfaz [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .</span><span class="sxs-lookup"><span data-stu-id="20b16-110">The [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl::GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md), and [**CMediaControl::Invoke**](cmediacontrol-invoke.md) member functions are standard implementations of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) methods using the [**CBaseDispatch**](cbasedispatch.md) class (and a type library) to parse the commands and pass them to the pure virtual methods of the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface.</span></span>

<span data-ttu-id="20b16-111">Los métodos [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) , definidos en control. ODL, se dejan como virtuales puros.</span><span class="sxs-lookup"><span data-stu-id="20b16-111">The [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) methods, defined in control.odl, are left as pure virtual.</span></span>



| <span data-ttu-id="20b16-112">Funciones de miembro</span><span class="sxs-lookup"><span data-stu-id="20b16-112">Member Functions</span></span>                                           | <span data-ttu-id="20b16-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="20b16-113">Description</span></span>                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20b16-114">**CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="20b16-114">**CMediaControl**</span></span>](cmediacontrol-cmediacontrol.md)       | <span data-ttu-id="20b16-115">Construye un objeto **CMediaControl** .</span><span class="sxs-lookup"><span data-stu-id="20b16-115">Constructs a **CMediaControl** object.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="20b16-116">Métodos IDispatch</span><span class="sxs-lookup"><span data-stu-id="20b16-116">IDispatch Methods</span></span>                                          | <span data-ttu-id="20b16-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="20b16-117">Description</span></span>                                                                                                                                                                                                                             |
| [<span data-ttu-id="20b16-118">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="20b16-118">**GetIDsOfNames**</span></span>](cmediacontrol-getidsofnames.md)       | <span data-ttu-id="20b16-119">Asigna un solo miembro y un conjunto opcional de parámetros a un conjunto correspondiente de identificadores de envío enteros (DISPID), que se puede usar en las llamadas subsiguientes al método [**CMediaControl:: Invoke**](cmediacontrol-invoke.md) .</span><span class="sxs-lookup"><span data-stu-id="20b16-119">Maps a single member and an optional set of parameters to a corresponding set of integer dispatch identifiers (DISPIDs), which can be used during subsequent calls to the [**CMediaControl::Invoke**](cmediacontrol-invoke.md) method.</span></span> |
| [<span data-ttu-id="20b16-120">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="20b16-120">**GetTypeInfo**</span></span>](cmediacontrol-gettypeinfo.md)           | <span data-ttu-id="20b16-121">Recupera un objeto de información de tipo, que puede recuperar la información de tipo de una interfaz.</span><span class="sxs-lookup"><span data-stu-id="20b16-121">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>                                                                                                                                          |
| [<span data-ttu-id="20b16-122">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="20b16-122">**GetTypeInfoCount**</span></span>](cmediacontrol-gettypeinfocount.md) | <span data-ttu-id="20b16-123">Recupera el número de interfaces de información de tipo proporcionado por un objeto.</span><span class="sxs-lookup"><span data-stu-id="20b16-123">Retrieves the number of type-information interfaces provided by an object.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="20b16-124">**Invocar**</span><span class="sxs-lookup"><span data-stu-id="20b16-124">**Invoke**</span></span>](cmediacontrol-invoke.md)                     | <span data-ttu-id="20b16-125">Proporciona acceso a las propiedades y los métodos expuestos por un objeto.</span><span class="sxs-lookup"><span data-stu-id="20b16-125">Provides access to properties and methods exposed by an object.</span></span>                                                                                                                                                                         |



 

 

 
