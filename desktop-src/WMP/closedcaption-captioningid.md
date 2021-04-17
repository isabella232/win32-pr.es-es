---
title: ClosedCaption.captioningID
description: La propiedad captioningID especifica o recupera el nombre del elemento que muestra los subtítulos.
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- ClosedCaption. captioningID Windows Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.captioningID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faadae626dd5ac0314c4140e3f9d82ab645ef9b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698471"
---
# <a name="closedcaptioncaptioningid"></a><span data-ttu-id="4c3bc-104">ClosedCaption.captioningID</span><span class="sxs-lookup"><span data-stu-id="4c3bc-104">ClosedCaption.captioningID</span></span>

<span data-ttu-id="4c3bc-105">La propiedad **captioningID** especifica o recupera el nombre del elemento que muestra los subtítulos.</span><span class="sxs-lookup"><span data-stu-id="4c3bc-105">The **captioningID** property specifies or retrieves the name of the element displaying the captioning.</span></span>

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a><span data-ttu-id="4c3bc-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="4c3bc-106">Possible Values</span></span>

<span data-ttu-id="4c3bc-107">Esta propiedad es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="4c3bc-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c3bc-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c3bc-108">Remarks</span></span>

<span data-ttu-id="4c3bc-109">El nombre de elemento especificado puede ser cualquier elemento HTML de la página web siempre que admita el atributo innerHTML.</span><span class="sxs-lookup"><span data-stu-id="4c3bc-109">The element name specified can be any HTML element in the webpage as long as it supports the innerHTML attribute.</span></span> <span data-ttu-id="4c3bc-110">Si la página web contiene varios marcos, el nombre del elemento solo puede hacer referencia a un elemento en el mismo marco que el control Player.</span><span class="sxs-lookup"><span data-stu-id="4c3bc-110">If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Player control.</span></span>

<span data-ttu-id="4c3bc-111">**Windows Media Player 10 Mobile:** Esta propiedad es de solo lectura y siempre devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="4c3bc-111">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="4c3bc-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4c3bc-112">Examples</span></span>

<span data-ttu-id="4c3bc-113">En el siguiente ejemplo de Microsoft JScript se usa *ClosedCaption*. **captioningID** para elegir el área de una página web que se usa para mostrar los subtítulos.</span><span class="sxs-lookup"><span data-stu-id="4c3bc-113">The following Microsoft JScript example uses *ClosedCaption*.**captioningID** to choose the area of a webpage used to display captions.</span></span> <span data-ttu-id="4c3bc-114">Se crearon dos elementos HTML DIV, con ID = CC1 e ID = CC2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4c3bc-114">Two HTML DIV elements were created, with ID = CC1 and ID = CC2, respectively.</span></span> <span data-ttu-id="4c3bc-115">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="4c3bc-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create two HTML BUTTON elements to allow the user to choose a display region. -->
<INPUT TYPE = "BUTTON"  NAME = "SET1"  VALUE = "Move Caption to CC1"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC2.innerHTML = 'This is the CC2 DIV';

           /* Show the captions in the DIV named CC1. */ 
           Player.ClosedCaption.captioningID = 'CC1';
          ">

<INPUT TYPE = "BUTTON" NAME = "SET2" VALUE = "Move Caption to CC2"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC1.innerHTML = 'This is the CC1 DIV';

           /* Show the captions in the DIV named CC2. */
           Player.ClosedCaption.captioningID = 'CC2';
          ">

```



## <a name="requirements"></a><span data-ttu-id="4c3bc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c3bc-116">Requirements</span></span>



| <span data-ttu-id="4c3bc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c3bc-117">Requirement</span></span> | <span data-ttu-id="4c3bc-118">Value</span><span class="sxs-lookup"><span data-stu-id="4c3bc-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c3bc-119">Versión</span><span class="sxs-lookup"><span data-stu-id="4c3bc-119">Version</span></span><br/> | <span data-ttu-id="4c3bc-120">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="4c3bc-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4c3bc-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4c3bc-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="4c3bc-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c3bc-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c3bc-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c3bc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c3bc-124">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="4c3bc-124">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="4c3bc-125">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="4c3bc-125">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





