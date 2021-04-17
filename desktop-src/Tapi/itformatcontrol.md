---
description: La interfaz ITFormatControl expone métodos que permiten a una aplicación recuperar información relacionada con el formato de una secuencia de recepción o transmisión para una llamada.
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: Interfaz ITFormatControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0735e7bfaf5222948cef5e047530a35cb19a125
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690831"
---
# <a name="itformatcontrol-interface"></a><span data-ttu-id="22886-103">Interfaz ITFormatControl</span><span class="sxs-lookup"><span data-stu-id="22886-103">ITFormatControl interface</span></span>

<span data-ttu-id="22886-104">\[ Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="22886-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="22886-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="22886-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="22886-106">La interfaz **ITFormatControl** expone métodos que permiten a una aplicación recuperar información relacionada con el formato de una secuencia de recepción o transmisión para una llamada.</span><span class="sxs-lookup"><span data-stu-id="22886-106">The **ITFormatControl** interface exposes methods that allow an application to retrieve information concerning the format of a receive or transmit stream for a call.</span></span>

<span data-ttu-id="22886-107">El [MSP de H323](h323-msp.md) implementa esta interfaz y solo se expone cuando una llamada utiliza este proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="22886-107">This interface is implemented by the [H323 MSP](h323-msp.md) and is exposed only when a call uses this service provider.</span></span>

## <a name="members"></a><span data-ttu-id="22886-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="22886-108">Members</span></span>

<span data-ttu-id="22886-109">La interfaz **ITFormatControl** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="22886-109">The **ITFormatControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="22886-110">**ITFormatControl** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="22886-110">**ITFormatControl** also has these types of members:</span></span>

-   [<span data-ttu-id="22886-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="22886-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="22886-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="22886-112">Methods</span></span>

<span data-ttu-id="22886-113">La interfaz **ITFormatControl** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="22886-113">The **ITFormatControl** interface has these methods.</span></span>



| <span data-ttu-id="22886-114">Método</span><span class="sxs-lookup"><span data-stu-id="22886-114">Method</span></span>                                                                     | <span data-ttu-id="22886-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="22886-115">Description</span></span>                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="22886-116">**GetCurrentFormat**</span><span class="sxs-lookup"><span data-stu-id="22886-116">**GetCurrentFormat**</span></span>](itformatcontrol-getcurrentformat.md)               | <span data-ttu-id="22886-117">Obtiene el formato de medios de la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="22886-117">Gets the media format of the current stream.</span></span><br/>                        |
| [<span data-ttu-id="22886-118">**GetNumberOfCapabilities**</span><span class="sxs-lookup"><span data-stu-id="22886-118">**GetNumberOfCapabilities**</span></span>](itformatcontrol-getnumberofcapabilities.md) | <span data-ttu-id="22886-119">Obtiene el número de funciones asociadas al formato actual.</span><span class="sxs-lookup"><span data-stu-id="22886-119">Gets the number of capabilities associated with the current format.</span></span><br/> |
| [<span data-ttu-id="22886-120">**GetStreamCaps**</span><span class="sxs-lookup"><span data-stu-id="22886-120">**GetStreamCaps**</span></span>](itformatcontrol-getstreamcaps.md)                     | <span data-ttu-id="22886-121">Obtiene las capacidades asociadas a un índice de formato determinado.</span><span class="sxs-lookup"><span data-stu-id="22886-121">Gets the capabilities associated with a given format index.</span></span><br/>         |
| [<span data-ttu-id="22886-122">**ReleaseFormat**</span><span class="sxs-lookup"><span data-stu-id="22886-122">**ReleaseFormat**</span></span>](itformatcontrol-releaseformat.md)                     | <span data-ttu-id="22886-123">Libera la estructura asociada al formato.</span><span class="sxs-lookup"><span data-stu-id="22886-123">Releases the structure associated with the format.</span></span><br/>                  |
| [<span data-ttu-id="22886-124">**ReOrderCapabilities**</span><span class="sxs-lookup"><span data-stu-id="22886-124">**ReOrderCapabilities**</span></span>](itformatcontrol-reordercapabilities.md)         | <span data-ttu-id="22886-125">Establece un nuevo orden para las capacidades de formato.</span><span class="sxs-lookup"><span data-stu-id="22886-125">Sets a new order for format capabilities.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="22886-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22886-126">Requirements</span></span>



| <span data-ttu-id="22886-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="22886-127">Requirement</span></span> | <span data-ttu-id="22886-128">Value</span><span class="sxs-lookup"><span data-stu-id="22886-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="22886-129">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="22886-129">TAPI version</span></span><br/> | <span data-ttu-id="22886-130">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="22886-130">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="22886-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22886-131">Header</span></span><br/>       | <dl> <span data-ttu-id="22886-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="22886-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="22886-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22886-133">Library</span></span><br/>      | <dl> <span data-ttu-id="22886-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22886-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="22886-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22886-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="22886-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22886-136"><dt>Tapi3.dll</dt></span></span> </dl> |



 

