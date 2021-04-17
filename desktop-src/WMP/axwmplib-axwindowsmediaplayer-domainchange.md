---
title: Evento DomainChange del objeto AxWindowsMediaPlayer
description: El evento DomainChange se produce cuando cambia el dominio del DVD. | Evento DomainChange del objeto AxWindowsMediaPlayer
ms.assetid: a080082e-1ba4-4080-b39c-b84292ecacb0
keywords:
- Evento DomainChange del objeto AxWindowsMediaPlayer Media Player de Windows
topic_type:
- apiref
api_name:
- DomainChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342ac559f75c3bb7d65b442bfbdced5e5ed3f690
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700060"
---
# <a name="domainchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d50e1-105">Evento DomainChange del objeto AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="d50e1-105">DomainChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d50e1-106">El evento DomainChange se produce cuando cambia el dominio del DVD.</span><span class="sxs-lookup"><span data-stu-id="d50e1-106">The DomainChange event occurs when the DVD domain changes.</span></span>

``` syntax
[C#]
private void player_DomainChange(
  object sender,
  _WMPOCXEvents_DomainChangeEvent e
)

[Visual Basic]
Private Sub player_DomainChange(  
  sender As Object,
  e As _WMPOCXEvents_DomainChangeEvent
) Handles player.DomainChange
```

## <a name="event-data"></a><span data-ttu-id="d50e1-107">Datos del evento</span><span class="sxs-lookup"><span data-stu-id="d50e1-107">Event Data</span></span>

<span data-ttu-id="d50e1-108">El controlador asociado a este evento es de tipo **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="d50e1-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DomainChangeEventHandler**.</span></span> <span data-ttu-id="d50e1-109">Este controlador recibe un argumento de tipo **AxWMPLib. \_ WMPOCXEvents \_ DomainChangeEvent**, que contiene la siguiente propiedad relacionada con este evento.</span><span class="sxs-lookup"><span data-stu-id="d50e1-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DomainChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="d50e1-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d50e1-110">Property</span></span>  | <span data-ttu-id="d50e1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d50e1-111">Description</span></span>                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d50e1-112">strDomain</span><span class="sxs-lookup"><span data-stu-id="d50e1-112">strDomain</span></span> | <span data-ttu-id="d50e1-113">System. StringIndicates el nuevo dominio.</span><span class="sxs-lookup"><span data-stu-id="d50e1-113">System.StringIndicates the new domain.</span></span> <span data-ttu-id="d50e1-114">Para los valores posibles, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="d50e1-114">For possible values, see the Remarks section.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d50e1-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d50e1-115">Remarks</span></span>

<span data-ttu-id="d50e1-116">En la tabla siguiente se muestran los posibles valores para la propiedad strDomain.</span><span class="sxs-lookup"><span data-stu-id="d50e1-116">The following table shows the possible values for the strDomain property.</span></span>



| <span data-ttu-id="d50e1-117">String</span><span class="sxs-lookup"><span data-stu-id="d50e1-117">String</span></span>            | <span data-ttu-id="d50e1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d50e1-118">Description</span></span>                                                          |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="d50e1-119">firstPlay</span><span class="sxs-lookup"><span data-stu-id="d50e1-119">firstPlay</span></span>         | <span data-ttu-id="d50e1-120">Realizar la inicialización predeterminada de un disco DVD.</span><span class="sxs-lookup"><span data-stu-id="d50e1-120">Performing default initialization of a DVD disc.</span></span>                     |
| <span data-ttu-id="d50e1-121">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="d50e1-121">videoManagerMenu</span></span>  | <span data-ttu-id="d50e1-122">Mostrando menús para todo el disco. También se conoce como menú o menú raíz.</span><span class="sxs-lookup"><span data-stu-id="d50e1-122">Displaying menus for whole disc. Also known as Root Menu or topMenu.</span></span> |
| <span data-ttu-id="d50e1-123">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="d50e1-123">videoTitleSetMenu</span></span> | <span data-ttu-id="d50e1-124">Mostrar menús para el conjunto de títulos actual.</span><span class="sxs-lookup"><span data-stu-id="d50e1-124">Displaying menus for current title set.</span></span> <span data-ttu-id="d50e1-125">También se conoce como titleMenu.</span><span class="sxs-lookup"><span data-stu-id="d50e1-125">Also known as titleMenu.</span></span>     |
| <span data-ttu-id="d50e1-126">title</span><span class="sxs-lookup"><span data-stu-id="d50e1-126">title</span></span>             | <span data-ttu-id="d50e1-127">Mostrar el título actual.</span><span class="sxs-lookup"><span data-stu-id="d50e1-127">Displaying the current title.</span></span>                                        |
| <span data-ttu-id="d50e1-128">stop</span><span class="sxs-lookup"><span data-stu-id="d50e1-128">stop</span></span>              | <span data-ttu-id="d50e1-129">El navegador de DVD está en el dominio de detención de DVD.</span><span class="sxs-lookup"><span data-stu-id="d50e1-129">The DVD Navigator is in the DVD Stop domain.</span></span>                         |



 

## <a name="requirements"></a><span data-ttu-id="d50e1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d50e1-130">Requirements</span></span>



| <span data-ttu-id="d50e1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d50e1-131">Requirement</span></span> | <span data-ttu-id="d50e1-132">Value</span><span class="sxs-lookup"><span data-stu-id="d50e1-132">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d50e1-133">Versión</span><span class="sxs-lookup"><span data-stu-id="d50e1-133">Version</span></span><br/>   | <span data-ttu-id="d50e1-134">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="d50e1-134">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d50e1-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d50e1-135">Namespace</span></span><br/> | <span data-ttu-id="d50e1-136">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d50e1-136">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d50e1-137">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="d50e1-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d50e1-138"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d50e1-138"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d50e1-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d50e1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d50e1-140">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d50e1-140">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d50e1-141">**Interfaz IWMPDVD (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="d50e1-141">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





