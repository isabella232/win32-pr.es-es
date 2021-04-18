---
description: El MSP de H323 implementa la interfaz IH323LineEx y solo está disponible en los objetos de dirección H. 323. Esta interfaz expone métodos que permiten la creación y la manipulación de terminales que pueden comunicarse entre clientes H323 y SDP.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: Interfaz IH323LineEx (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41888b16f645a3af1eefd9df61623cb28684bfdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680526"
---
# <a name="ih323lineex-interface"></a><span data-ttu-id="86b4a-104">Interfaz IH323LineEx</span><span class="sxs-lookup"><span data-stu-id="86b4a-104">IH323LineEx interface</span></span>

<span data-ttu-id="86b4a-105">\[**IH323LineEx** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="86b4a-105">\[**IH323LineEx** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="86b4a-106">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="86b4a-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="86b4a-107">El [MSP de H323](h323-msp.md) implementa la interfaz **IH323LineEx** y solo está disponible en los objetos de dirección H. 323.</span><span class="sxs-lookup"><span data-stu-id="86b4a-107">The **IH323LineEx** interface is implemented by the [H323 MSP](h323-msp.md) and is available only on H.323 address objects.</span></span> <span data-ttu-id="86b4a-108">Esta interfaz expone métodos que permiten la creación y la manipulación de terminales que pueden comunicarse entre clientes H323 y SDP.</span><span class="sxs-lookup"><span data-stu-id="86b4a-108">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span>

> [!Note]  
> <span data-ttu-id="86b4a-109">Solo se debe llamar a todos los métodos de esta interfaz después de registrarse para las llamadas entrantes en esta dirección.</span><span class="sxs-lookup"><span data-stu-id="86b4a-109">All methods in this interface should be called only after registering for incoming calls on this address.</span></span>

 

## <a name="members"></a><span data-ttu-id="86b4a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="86b4a-110">Members</span></span>

<span data-ttu-id="86b4a-111">La interfaz **IH323LineEx** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="86b4a-111">The **IH323LineEx** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="86b4a-112">**IH323LineEx** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="86b4a-112">**IH323LineEx** also has these types of members:</span></span>

-   [<span data-ttu-id="86b4a-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="86b4a-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="86b4a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="86b4a-114">Methods</span></span>

<span data-ttu-id="86b4a-115">La interfaz **IH323LineEx** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="86b4a-115">The **IH323LineEx** interface has these methods.</span></span>



| <span data-ttu-id="86b4a-116">Método</span><span class="sxs-lookup"><span data-stu-id="86b4a-116">Method</span></span>                                                                                 | <span data-ttu-id="86b4a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="86b4a-117">Description</span></span>                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="86b4a-118">**SetAlias**</span><span class="sxs-lookup"><span data-stu-id="86b4a-118">**SetAlias**</span></span>](ih323lineex-setalias.md)                                               | <span data-ttu-id="86b4a-119">Configura un alias H. 323 predeterminado para la dirección.</span><span class="sxs-lookup"><span data-stu-id="86b4a-119">Configures a default H.323 alias for the address.</span></span><br/>             |
| [<span data-ttu-id="86b4a-120">**SetDefaultCapabilityPreferrence**</span><span class="sxs-lookup"><span data-stu-id="86b4a-120">**SetDefaultCapabilityPreferrence**</span></span>](ih323lineex-setdefaultcapabilitypreferrence.md) | <span data-ttu-id="86b4a-121">Configura la ponderación de las preferencias para las funciones predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="86b4a-121">Configures the preference weighting for default capabilities.</span></span><br/> |
| [<span data-ttu-id="86b4a-122">**SetExternalT120Address**</span><span class="sxs-lookup"><span data-stu-id="86b4a-122">**SetExternalT120Address**</span></span>](ih323lineex-setexternalt120address.md)                   | <span data-ttu-id="86b4a-123">Configura una dirección T. 120 externa para el intercambio de datos.</span><span class="sxs-lookup"><span data-stu-id="86b4a-123">Configures an external T.120 address for data exchange.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="86b4a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86b4a-124">Requirements</span></span>



| <span data-ttu-id="86b4a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="86b4a-125">Requirement</span></span> | <span data-ttu-id="86b4a-126">Value</span><span class="sxs-lookup"><span data-stu-id="86b4a-126">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86b4a-127">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="86b4a-127">TAPI version</span></span><br/> | <span data-ttu-id="86b4a-128">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="86b4a-128">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="86b4a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86b4a-129">Header</span></span><br/>       | <dl> <span data-ttu-id="86b4a-130"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="86b4a-130"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="86b4a-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86b4a-131">Library</span></span><br/>      | <dl> <span data-ttu-id="86b4a-132"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86b4a-132"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="86b4a-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="86b4a-133">DLL</span></span><br/>          | <dl> <span data-ttu-id="86b4a-134"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86b4a-134"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="86b4a-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="86b4a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86b4a-136">H323 MSP</span><span class="sxs-lookup"><span data-stu-id="86b4a-136">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

