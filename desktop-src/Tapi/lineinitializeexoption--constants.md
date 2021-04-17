---
description: Las \_ constantes LINEINITIALIZEEXOPTION especifican qué mecanismo de notificación de eventos se debe usar al inicializar una sesión.
ms.assetid: 77674a45-7133-4518-af47-a9d58392b80b
title: Constantes de LINEINITIALIZEEXOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86543c367877d74562cc0af13261881b7df19982
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690738"
---
# <a name="lineinitializeexoption_-constants"></a><span data-ttu-id="7cbf8-103">Constantes de LINEINITIALIZEEXOPTION \_</span><span class="sxs-lookup"><span data-stu-id="7cbf8-103">LINEINITIALIZEEXOPTION\_ Constants</span></span>

<span data-ttu-id="7cbf8-104">Las **constantes \_ LINEINITIALIZEEXOPTION** especifican qué mecanismo de notificación de eventos se debe usar al inicializar una sesión.</span><span class="sxs-lookup"><span data-stu-id="7cbf8-104">The **LINEINITIALIZEEXOPTION\_** constants specify which event notification mechanism to use when initializing a session.</span></span>

<dl> <dt>

<span data-ttu-id="7cbf8-105"><span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION \_ CALLHUBTRACKING**</span><span class="sxs-lookup"><span data-stu-id="7cbf8-105"><span id="LINEINITIALIZEEXOPTION_CALLHUBTRACKING"></span><span id="lineinitializeexoption_callhubtracking"></span>**LINEINITIALIZEEXOPTION\_CALLHUBTRACKING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7cbf8-106">La aplicación desea utilizar el mecanismo de notificación de eventos de seguimiento del centro de llamadas.</span><span class="sxs-lookup"><span data-stu-id="7cbf8-106">The application desires to use the call hub tracking event notification mechanism.</span></span> <span data-ttu-id="7cbf8-107">Esta constante solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="7cbf8-107">This constant is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7cbf8-108"><span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION \_ USECOMPLETIONPORT**</span><span class="sxs-lookup"><span data-stu-id="7cbf8-108"><span id="LINEINITIALIZEEXOPTION_USECOMPLETIONPORT"></span><span id="lineinitializeexoption_usecompletionport"></span>**LINEINITIALIZEEXOPTION\_USECOMPLETIONPORT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7cbf8-109">La aplicación desea utilizar el mecanismo de notificación de eventos del puerto de finalización.</span><span class="sxs-lookup"><span data-stu-id="7cbf8-109">The application desires to use the Completion Port event notification mechanism.</span></span> <span data-ttu-id="7cbf8-110">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="7cbf8-110">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7cbf8-111"><span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION \_ USEEVENT**</span><span class="sxs-lookup"><span data-stu-id="7cbf8-111"><span id="LINEINITIALIZEEXOPTION_USEEVENT"></span><span id="lineinitializeexoption_useevent"></span>**LINEINITIALIZEEXOPTION\_USEEVENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7cbf8-112">La aplicación desea utilizar el mecanismo de notificación de eventos de controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="7cbf8-112">The application desires to use the Event Handle event notification mechanism.</span></span> <span data-ttu-id="7cbf8-113">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="7cbf8-113">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7cbf8-114"><span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION \_ USEHIDDENWINDOW**</span><span class="sxs-lookup"><span data-stu-id="7cbf8-114"><span id="LINEINITIALIZEEXOPTION_USEHIDDENWINDOW"></span><span id="lineinitializeexoption_usehiddenwindow"></span>**LINEINITIALIZEEXOPTION\_USEHIDDENWINDOW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="7cbf8-115">La aplicación desea utilizar el mecanismo de notificación de eventos de ventana oculta.</span><span class="sxs-lookup"><span data-stu-id="7cbf8-115">The application desires to use the Hidden Window event notification mechanism.</span></span> <span data-ttu-id="7cbf8-116">Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,0 o superior.</span><span class="sxs-lookup"><span data-stu-id="7cbf8-116">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7cbf8-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7cbf8-117">Remarks</span></span>

<span data-ttu-id="7cbf8-118">Vea [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) para obtener más detalles sobre el funcionamiento de estas opciones.</span><span class="sxs-lookup"><span data-stu-id="7cbf8-118">See [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cbf8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cbf8-119">Requirements</span></span>



| <span data-ttu-id="7cbf8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cbf8-120">Requirement</span></span> | <span data-ttu-id="7cbf8-121">Value</span><span class="sxs-lookup"><span data-stu-id="7cbf8-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7cbf8-122">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="7cbf8-122">TAPI version</span></span><br/> | <span data-ttu-id="7cbf8-123">Requiere TAPI 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7cbf8-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="7cbf8-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7cbf8-124">Header</span></span><br/>       | <dl> <span data-ttu-id="7cbf8-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cbf8-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




