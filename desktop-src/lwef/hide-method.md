---
title: Hide (método)
description: Hide (método)
ms.assetid: c30eda78-0951-43b4-8ae1-daccbd41170d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd50c3f7b8e3d2e60ebe4c00c42375737c05eb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149236"
---
# <a name="hide-method"></a><span data-ttu-id="d0683-103">Hide (método)</span><span class="sxs-lookup"><span data-stu-id="d0683-103">Hide Method</span></span>

<span data-ttu-id="d0683-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0683-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d0683-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="d0683-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d0683-106">Oculta el carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="d0683-106">Hides the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="d0683-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="d0683-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d0683-108">\*agente ***. Caracteres ("*** CharacterID \* *"). Ocultar* \*  \[ *rápidamente*\]</span><span class="sxs-lookup"><span data-stu-id="d0683-108">*agent ***.Characters ("*** CharacterID\*\*\*").Hide*\* \[*Fast*\]</span></span>



| <span data-ttu-id="d0683-109">Parte</span><span class="sxs-lookup"><span data-stu-id="d0683-109">Part</span></span>   | <span data-ttu-id="d0683-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0683-110">Description</span></span>                                                                                                                                                                                                                                      |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0683-111">*Rápido*</span><span class="sxs-lookup"><span data-stu-id="d0683-111">*Fast*</span></span> | <span data-ttu-id="d0683-112">Opcional.</span><span class="sxs-lookup"><span data-stu-id="d0683-112">Optional.</span></span> <span data-ttu-id="d0683-113">Un valor booleano que indica si se va a omitir la animación asociada al estado de ocultación del carácter **true** no reproduce la animación de **ocultación** .</span><span class="sxs-lookup"><span data-stu-id="d0683-113">A Boolean value that indicates whether to skip the animation associated with the character's Hiding state **True** Does not play the **Hiding** animation.</span></span> <br/> <span data-ttu-id="d0683-114">**False** (valor predeterminado) reproduce la animación de **ocultación** .</span><span class="sxs-lookup"><span data-stu-id="d0683-114">**False** (Default) Plays the **Hiding** animation.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0683-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0683-115">Remarks</span></span>

<span data-ttu-id="d0683-116">El servidor pone en cola las acciones del método **Hide** en la cola del carácter, por lo que puede usarla para ocultar el carácter después de una secuencia de otras animaciones.</span><span class="sxs-lookup"><span data-stu-id="d0683-116">The server queues the actions of the **Hide** method in the character's queue, so you can use it to hide the character after a sequence of other animations.</span></span> <span data-ttu-id="d0683-117">Puede reproducir la acción inmediatamente mediante el método [**Stop**](stop-method.md) antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="d0683-117">You can play the action immediately by using the [**Stop**](stop-method.md) method before calling this method.</span></span>

<span data-ttu-id="d0683-118">Si declara una referencia de objeto y la establece en este método, devuelve un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="d0683-118">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="d0683-119">Además, si la animación de **ocultación** asociada no se ha cargado y no se ha especificado el parámetro **Fast** como **true**, el servidor establece la propiedad de [**Estado**](status-property.md) de objeto de **solicitud** en "Failed" con un número de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="d0683-119">In addition, if the associated **Hiding** animation has not been loaded and you have not specified the **Fast** parameter as **True**, the server sets the **Request** object [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="d0683-120">Por lo tanto, si usa el protocolo HTTP para tener acceso a los datos de caracteres o de animación, use el método [**Get**](get-method.md) y especifique el estado de **ocultación** para cargar la animación antes de llamar al método **Hide** .</span><span class="sxs-lookup"><span data-stu-id="d0683-120">Therefore, if you are using the HTTP protocol to access character or animation data, use the [**Get**](get-method.md) method and specify the **Hiding** state to load the animation before calling the **Hide** method.</span></span>

<span data-ttu-id="d0683-121">Ocultar un carácter también puede producir el desencadenamiento del evento [**ActivateInput**](activateinput-event.md) de otro cliente.</span><span class="sxs-lookup"><span data-stu-id="d0683-121">Hiding a character can also result in triggering the [**ActivateInput**](activateinput-event.md) event of another client.</span></span>

> [!Note]  
> <span data-ttu-id="d0683-122">Los caracteres ocultos no pueden tener acceso al canal de audio.</span><span class="sxs-lookup"><span data-stu-id="d0683-122">Hidden characters cannot access the audio channel.</span></span> <span data-ttu-id="d0683-123">El servidor devolverá un estado de error en el evento [**RequestComplete**](requestcomplete-event.md) si genera una solicitud de animación y el carácter está oculto.</span><span class="sxs-lookup"><span data-stu-id="d0683-123">The server will pass back a failure status in the [**RequestComplete**](requestcomplete-event.md) event if you generate an animation request and the character is hidden.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="d0683-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d0683-124">See Also</span></span>

[<span data-ttu-id="d0683-125">**Show (método)**</span><span class="sxs-lookup"><span data-stu-id="d0683-125">**Show method**</span></span>](show-method.md)


 

