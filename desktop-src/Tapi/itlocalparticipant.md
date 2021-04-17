---
description: La interfaz ITLocalParticipant se expone en el objeto de secuencia cuando IPConf MSP admite la llamada.
ms.assetid: 64965ae2-e30b-4353-a502-f96018da71a5
title: Interfaz ITLocalParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4017837a0b970cb791cdf454437fe2d48720028
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690647"
---
# <a name="itlocalparticipant-interface"></a><span data-ttu-id="7015a-103">Interfaz ITLocalParticipant</span><span class="sxs-lookup"><span data-stu-id="7015a-103">ITLocalParticipant interface</span></span>

<span data-ttu-id="7015a-104">La interfaz **ITLocalParticipant** se expone en el objeto de secuencia cuando IPConf MSP admite la llamada.</span><span class="sxs-lookup"><span data-stu-id="7015a-104">The **ITLocalParticipant** interface is exposed on the stream object when the IPConf MSP supports the call.</span></span> <span data-ttu-id="7015a-105">El MSP implementa métodos que permiten a una aplicación obtener y establecer la información de los participantes.</span><span class="sxs-lookup"><span data-stu-id="7015a-105">The MSP implements methods that allow an application to get and set participant information.</span></span> <span data-ttu-id="7015a-106">La interfaz **ITLocalParticipant** se crea llamando a **QueryInterface** en [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span><span class="sxs-lookup"><span data-stu-id="7015a-106">The **ITLocalParticipant** interface is created by calling **QueryInterface** on [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span>

## <a name="members"></a><span data-ttu-id="7015a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7015a-107">Members</span></span>

<span data-ttu-id="7015a-108">La interfaz **ITLocalParticipant** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7015a-108">The **ITLocalParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7015a-109">**ITLocalParticipant** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7015a-109">**ITLocalParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="7015a-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="7015a-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7015a-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="7015a-111">Methods</span></span>

<span data-ttu-id="7015a-112">La interfaz **ITLocalParticipant** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="7015a-112">The **ITLocalParticipant** interface has these methods.</span></span>



| <span data-ttu-id="7015a-113">Método</span><span class="sxs-lookup"><span data-stu-id="7015a-113">Method</span></span>                                                                                     | <span data-ttu-id="7015a-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7015a-114">Description</span></span>                                                                            |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="7015a-115">**obtener \_ LocalParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="7015a-115">**get\_LocalParticipantTypedInfo**</span></span>](itlocalparticipant-get-localparticipanttypedinfo.md) | <span data-ttu-id="7015a-116">Obtiene la información de los participantes, como el nombre de correo electrónico o la ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="7015a-116">Gets participant information, such as e-mail name or geographical location.</span></span><br/> |
| [<span data-ttu-id="7015a-117">**Put \_ LocalParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="7015a-117">**put\_LocalParticipantTypedInfo**</span></span>](itlocalparticipant-put-localparticipanttypedinfo.md) | <span data-ttu-id="7015a-118">Establece la información del participante.</span><span class="sxs-lookup"><span data-stu-id="7015a-118">Sets participant information.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="7015a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7015a-119">Requirements</span></span>



| <span data-ttu-id="7015a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7015a-120">Requirement</span></span> | <span data-ttu-id="7015a-121">Value</span><span class="sxs-lookup"><span data-stu-id="7015a-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7015a-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="7015a-122">TAPI version</span></span><br/> | <span data-ttu-id="7015a-123">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7015a-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7015a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7015a-124">Header</span></span><br/>       | <dl> <span data-ttu-id="7015a-125"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="7015a-125"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="7015a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7015a-126">Library</span></span><br/>      | <dl> <span data-ttu-id="7015a-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7015a-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7015a-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7015a-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="7015a-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7015a-129"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7015a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7015a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7015a-131">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="7015a-131">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

