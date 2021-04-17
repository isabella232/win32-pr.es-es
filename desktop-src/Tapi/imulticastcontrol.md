---
description: IPConf MSP implementa la interfaz IMulticastControl y solo está disponible en los objetos de llamada de multidifusión.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: Interfaz IMulticastControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98ad006ea41034d6d4da32359d1ecbcdd250ab6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690785"
---
# <a name="imulticastcontrol-interface"></a><span data-ttu-id="5450a-103">Interfaz IMulticastControl</span><span class="sxs-lookup"><span data-stu-id="5450a-103">IMulticastControl interface</span></span>

<span data-ttu-id="5450a-104">\[**IMulticastControl** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5450a-104">\[**IMulticastControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5450a-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="5450a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5450a-106">IPConf MSP implementa la interfaz **IMulticastControl** y solo está disponible en los objetos de llamada de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="5450a-106">The **IMulticastControl** interface is implemented by the IPConf MSP and available only on multicast call objects.</span></span> <span data-ttu-id="5450a-107">Esta interfaz expone métodos que permiten la creación y la manipulación de terminales que pueden comunicarse entre clientes H323 y SDP.</span><span class="sxs-lookup"><span data-stu-id="5450a-107">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span> <span data-ttu-id="5450a-108">La interfaz **IMulticastControl** controla el modo de bucle invertido de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="5450a-108">The **IMulticastControl** interface controls the multicast loopback mode.</span></span>

<span data-ttu-id="5450a-109">En el \_ modo mm no \_ loopback, se deshabilita el bucle invertido de multidifusión, lo que significa que dos aplicaciones en el mismo equipo que se unen al mismo grupo de multidifusión obtendrán los paquetes de los demás.</span><span class="sxs-lookup"><span data-stu-id="5450a-109">In the MM\_NO\_LOOPBACK mode, multicast loopback is disabled, which means two applications on the same machine who join the same multicast group will get each other's packets.</span></span> <span data-ttu-id="5450a-110">Este modo tiene el mejor rendimiento si siempre hay una aplicación que se une al grupo de multidifusión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="5450a-110">This mode has the best performance if there is always only one application joining the multicast group on the machine.</span></span> <span data-ttu-id="5450a-111">MM \_ no hay \_ modo de bucle invertido es el modo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5450a-111">MM\_NO\_LOOPBACK mode is the default mode.</span></span>

<span data-ttu-id="5450a-112">El \_ \_ modo de bucle invertido completo de mm solo es adecuado para pruebas.</span><span class="sxs-lookup"><span data-stu-id="5450a-112">The MM\_FULL\_LOOPBACK mode is good only for testing.</span></span> <span data-ttu-id="5450a-113">También se recorren en bucle todos los paquetes enviados.</span><span class="sxs-lookup"><span data-stu-id="5450a-113">All the packets sent out are looped back as well.</span></span> <span data-ttu-id="5450a-114">Se puede usar para comprobar si los dispositivos funcionan.</span><span class="sxs-lookup"><span data-stu-id="5450a-114">This can be used to test if the devices are working.</span></span>

<span data-ttu-id="5450a-115">El \_ modo bucle selectivo de mm \_ se usa para permitir que varias aplicaciones de un equipo se unan al mismo grupo de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="5450a-115">The MM\_SELECTIVE\_LOOPBACK mode is used to enable multiple applications on one machine to join the same multicast group.</span></span> <span data-ttu-id="5450a-116">Los paquetes se recorren en bucle desde la pila y cada sesión de RTP es responsable de filtrar los paquetes no deseados.</span><span class="sxs-lookup"><span data-stu-id="5450a-116">The packets are looped back from the stack, and each RTP session is responsible for filtering out unwanted packets.</span></span>

## <a name="members"></a><span data-ttu-id="5450a-117">Miembros</span><span class="sxs-lookup"><span data-stu-id="5450a-117">Members</span></span>

<span data-ttu-id="5450a-118">La interfaz **IMulticastControl** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5450a-118">The **IMulticastControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5450a-119">**IMulticastControl** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5450a-119">**IMulticastControl** also has these types of members:</span></span>

-   [<span data-ttu-id="5450a-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="5450a-120">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5450a-121">Métodos</span><span class="sxs-lookup"><span data-stu-id="5450a-121">Methods</span></span>

<span data-ttu-id="5450a-122">La interfaz **IMulticastControl** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5450a-122">The **IMulticastControl** interface has these methods.</span></span>



| <span data-ttu-id="5450a-123">Método</span><span class="sxs-lookup"><span data-stu-id="5450a-123">Method</span></span>                                                          | <span data-ttu-id="5450a-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="5450a-124">Description</span></span>                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [<span data-ttu-id="5450a-125">**obtener \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="5450a-125">**get\_LoopbackMode**</span></span>](imulticastcontrol-get-loopbackmode.md) | <span data-ttu-id="5450a-126">Obtiene el modo de bucle invertido de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="5450a-126">Gets the multicast loopback mode.</span></span><br/> |
| [<span data-ttu-id="5450a-127">**Put \_ LoopbackMode**</span><span class="sxs-lookup"><span data-stu-id="5450a-127">**put\_LoopbackMode**</span></span>](imulticastcontrol-put-loopbackmode.md) | <span data-ttu-id="5450a-128">Establece el modo de bucle invertido de multidifusión.</span><span class="sxs-lookup"><span data-stu-id="5450a-128">Sets the multicast loopback mode.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5450a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5450a-129">Requirements</span></span>



| <span data-ttu-id="5450a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5450a-130">Requirement</span></span> | <span data-ttu-id="5450a-131">Value</span><span class="sxs-lookup"><span data-stu-id="5450a-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5450a-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="5450a-132">TAPI version</span></span><br/> | <span data-ttu-id="5450a-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="5450a-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5450a-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5450a-134">Header</span></span><br/>       | <dl> <span data-ttu-id="5450a-135"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="5450a-135"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="5450a-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5450a-136">Library</span></span><br/>      | <dl> <span data-ttu-id="5450a-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5450a-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5450a-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5450a-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="5450a-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5450a-139"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5450a-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="5450a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5450a-141">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="5450a-141">IPConf MSP</span></span>](ipconf-msp.md)
</dt> </dl>

 

