---
title: MoveTo (método)
description: MoveTo (método)
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6a7f215de9ea6e323870ec7e10967462ab4174
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077753"
---
# <a name="moveto-method"></a><span data-ttu-id="f0428-103">MoveTo (método)</span><span class="sxs-lookup"><span data-stu-id="f0428-103">MoveTo Method</span></span>

<span data-ttu-id="f0428-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f0428-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f0428-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="f0428-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f0428-106">Mueve el carácter especificado a la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="f0428-106">Moves the specified character to the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="f0428-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="f0428-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f0428-108">\*agente ***. Caracteres ("*** CharacterID \* *"). MoveTo* \*  *velocidad x, y* \[ \]</span><span class="sxs-lookup"><span data-stu-id="f0428-108">*agent ***.Characters ("*** CharacterID\*\*\*").MoveTo*\* *x,y*\[*Speed*\]</span></span>



| <span data-ttu-id="f0428-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f0428-109">Part</span></span>    | <span data-ttu-id="f0428-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0428-110">Description</span></span>                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0428-111">*x, y*</span><span class="sxs-lookup"><span data-stu-id="f0428-111">*x,y*</span></span>   | <span data-ttu-id="f0428-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f0428-112">Required.</span></span> <span data-ttu-id="f0428-113">Un valor entero que indica el borde izquierdo (*x*) y el borde superior (*y*) del fotograma de animación.</span><span class="sxs-lookup"><span data-stu-id="f0428-113">An integer value that indicates the left edge (*x*) and top edge (*y*) of the animation frame.</span></span> <span data-ttu-id="f0428-114">Exprese estas coordenadas en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f0428-114">Express these coordinates in pixels.</span></span>                                                   |
| <span data-ttu-id="f0428-115">*Velocidad*</span><span class="sxs-lookup"><span data-stu-id="f0428-115">*Speed*</span></span> | <span data-ttu-id="f0428-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="f0428-116">Optional.</span></span> <span data-ttu-id="f0428-117">Valor entero largo que especifica en milisegundos la rapidez con la que se mueve el marco del carácter.</span><span class="sxs-lookup"><span data-stu-id="f0428-117">A Long integer value specifying in milliseconds how quickly the character's frame moves.</span></span> <span data-ttu-id="f0428-118">El valor predeterminado es 1000.</span><span class="sxs-lookup"><span data-stu-id="f0428-118">The default value is 1000.</span></span> <span data-ttu-id="f0428-119">Si se especifica cero (0), se mueve el marco sin reproducir una animación.</span><span class="sxs-lookup"><span data-stu-id="f0428-119">Specifying zero (0) moves the frame without playing an animation.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0428-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0428-120">Remarks</span></span>

<span data-ttu-id="f0428-121">El servidor reproduce automáticamente la animación adecuada asignada a los Estados **móviles** .</span><span class="sxs-lookup"><span data-stu-id="f0428-121">The server automatically plays the appropriate animation assigned to the **Moving** states.</span></span> <span data-ttu-id="f0428-122">La ubicación de un carácter se basa en la esquina superior izquierda de su marco.</span><span class="sxs-lookup"><span data-stu-id="f0428-122">The location of a character is based on the upper left corner of its frame.</span></span>

<span data-ttu-id="f0428-123">Si declara una variable de objeto y la establece en este método, devolverá un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="f0428-123">If you declare an object variable and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="f0428-124">Además, si la animación asociada no se ha cargado en el equipo local, el servidor establece la propiedad de [**Estado**](status-property.md) del objeto de **solicitud** en "Failed" con un número de error adecuado.</span><span class="sxs-lookup"><span data-stu-id="f0428-124">In addition, if the associated animation has not been loaded on the local machine, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error number.</span></span> <span data-ttu-id="f0428-125">Por consiguiente, si usa el protocolo HTTP para tener acceso a los datos de caracteres o de animación, use el método [**Get**](get-method.md) para cargar las animaciones de estado en **movimiento** antes de llamar al método **moveTo** .</span><span class="sxs-lookup"><span data-stu-id="f0428-125">Therefore, if you are using the HTTP protocol to access character or animation data, use the [**Get**](get-method.md) method to load the **Moving** state animations before calling the **MoveTo** method.</span></span>

<span data-ttu-id="f0428-126">Incluso si la animación no está cargada, el servidor todavía mueve el marco.</span><span class="sxs-lookup"><span data-stu-id="f0428-126">Even if the animation is not loaded, the server still moves the frame.</span></span>

> [!Note]  
> <span data-ttu-id="f0428-127">Si llama a **moveTo** con un valor distinto de cero antes de que se muestre el carácter, devolverá un estado de error si le asignó un objeto de [**solicitud**](/windows/desktop/lwef/the-request-object) , ya que el valor distinto de cero indica que está intentando reproducir una animación cuando el carácter no está visible.</span><span class="sxs-lookup"><span data-stu-id="f0428-127">If you call **MoveTo** with a nonzero value before the character is shown, it will return a failure status if you assigned it a [**Request**](/windows/desktop/lwef/the-request-object) object, because the nonzero value indicates that you are attempting to play an animation when the character is not visible.</span></span>

 

> [!Note]  
> <span data-ttu-id="f0428-128">El efecto real del parámetro de *velocidad* puede variar en función de la velocidad del procesador del equipo y la prioridad de otras tareas que se ejecutan en el sistema.</span><span class="sxs-lookup"><span data-stu-id="f0428-128">The *Speed* parameter's actual effect may vary based on the speed of the processor of the computer and the priority of other tasks running on the system.</span></span>

 

 

 