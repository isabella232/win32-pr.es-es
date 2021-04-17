---
title: StopAll (método)
description: StopAll (método)
ms.assetid: 2ce32ff8-4908-45b1-9b83-4d558f67417c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76c99a687c2481d9686e84b7fa5c198e7a4273a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105704937"
---
# <a name="stopall-method"></a><span data-ttu-id="ed882-103">StopAll (método)</span><span class="sxs-lookup"><span data-stu-id="ed882-103">StopAll Method</span></span>

<span data-ttu-id="ed882-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ed882-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ed882-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="ed882-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ed882-106">Detiene todas las solicitudes de animación o los tipos de solicitudes especificados para el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="ed882-106">Stops all animation requests or specified types of requests for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="ed882-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="ed882-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ed882-108">\*agente ***. Caracteres ("*** CharacterID \* *"). StopAll*( \*  \[ *tipo* )\]</span><span class="sxs-lookup"><span data-stu-id="ed882-108">*agent ***.Characters ("*** CharacterID\*\*\*").StopAll*\* \[*Type*\]</span></span>



| <span data-ttu-id="ed882-109">Parte</span><span class="sxs-lookup"><span data-stu-id="ed882-109">Part</span></span>   | <span data-ttu-id="ed882-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ed882-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed882-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="ed882-111">*Type*</span></span> | <span data-ttu-id="ed882-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ed882-112">Optional.</span></span> <span data-ttu-id="ed882-113">Para usar este parámetro, puede usar cualquiera de los siguientes valores.</span><span class="sxs-lookup"><span data-stu-id="ed882-113">To use this parameter you can use any of the following values.</span></span> <span data-ttu-id="ed882-114">También puede especificar varios tipos separándolos con comas.</span><span class="sxs-lookup"><span data-stu-id="ed882-114">You can also specify multiple types by separating them with commas.</span></span> <br/> <span data-ttu-id="ed882-115">"**Obtener**"</span><span class="sxs-lookup"><span data-stu-id="ed882-115">"**Get**"</span></span> <br/> <span data-ttu-id="ed882-116">Para detener todas las solicitudes [**Get**](get-method.md) en cola.</span><span class="sxs-lookup"><span data-stu-id="ed882-116">To stop all queued [**Get**](get-method.md) requests.</span></span><br/> <span data-ttu-id="ed882-117">"**NonQueuedGet**"</span><span class="sxs-lookup"><span data-stu-id="ed882-117">"**NonQueuedGet**"</span></span> <br/> <span data-ttu-id="ed882-118">Para detener todas las solicitudes [**Get**](get-method.md) no en cola (método **Get** con el parámetro **Queue** establecido en **false**).</span><span class="sxs-lookup"><span data-stu-id="ed882-118">To stop all non-queued [**Get**](get-method.md) requests (**Get** method with **Queue** parameter set to **False**).</span></span><br/> <span data-ttu-id="ed882-119">"**Movimiento**"</span><span class="sxs-lookup"><span data-stu-id="ed882-119">"**Move**"</span></span> <br/> <span data-ttu-id="ed882-120">Para detener todas las solicitudes en cola [**moveTo**](moveto-method.md) .</span><span class="sxs-lookup"><span data-stu-id="ed882-120">To stop all queued [**MoveTo**](moveto-method.md) requests.</span></span><br/> <span data-ttu-id="ed882-121">"**Reproducir**"</span><span class="sxs-lookup"><span data-stu-id="ed882-121">"**Play**"</span></span> <br/> <span data-ttu-id="ed882-122">Para detener todas las solicitudes de [**reproducción**](play-method.md) en cola.</span><span class="sxs-lookup"><span data-stu-id="ed882-122">To stop all queued [**Play**](play-method.md) requests.</span></span><br/> <span data-ttu-id="ed882-123">"**Hablar**"</span><span class="sxs-lookup"><span data-stu-id="ed882-123">"**Speak**"</span></span> <br/> <span data-ttu-id="ed882-124">Para detener todas las solicitudes de [**voz**](speak-method.md) en cola.</span><span class="sxs-lookup"><span data-stu-id="ed882-124">To stop all queued [**Speak**](speak-method.md) requests.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed882-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed882-125">Remarks</span></span>

<span data-ttu-id="ed882-126">Si no establece el parámetro de **tipo** , el servidor detiene todas las animaciones para el carácter, incluidas las solicitudes [**Get**](get-method.md) en cola y no en cola, y borra su cola de animaciones.</span><span class="sxs-lookup"><span data-stu-id="ed882-126">If you don't set the **Type** parameter, the server stops all animations for the character, including queued and non-queued [**Get**](get-method.md) requests, and clears its animation queue.</span></span> <span data-ttu-id="ed882-127">También detiene la reproducción de la animación que oculta o muestra un carácter.</span><span class="sxs-lookup"><span data-stu-id="ed882-127">It also stops playing a character's Hiding or Showing animation.</span></span>

<span data-ttu-id="ed882-128">Este método no generará un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="ed882-128">This method will not generate a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed882-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ed882-129">See Also</span></span>

[<span data-ttu-id="ed882-130">**Método Stop**</span><span class="sxs-lookup"><span data-stu-id="ed882-130">**Stop method**</span></span>](stop-method.md)


 

