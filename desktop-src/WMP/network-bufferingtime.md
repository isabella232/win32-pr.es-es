---
title: Network. bufferingTime
description: La propiedad bufferingTime especifica o recupera la cantidad de tiempo en milisegundos asignados para almacenar en búfer los datos entrantes antes de comenzar la reproducción.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- Windows Media Player de red. bufferingTime
topic_type:
- apiref
api_name:
- Network.bufferingTime
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b805173403268afff473db427b58193382afe6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708306"
---
# <a name="networkbufferingtime"></a><span data-ttu-id="5997d-104">Network. bufferingTime</span><span class="sxs-lookup"><span data-stu-id="5997d-104">Network.bufferingTime</span></span>

<span data-ttu-id="5997d-105">La propiedad **bufferingTime** especifica o recupera la cantidad de tiempo en milisegundos asignados para almacenar en búfer los datos entrantes antes de comenzar la reproducción.</span><span class="sxs-lookup"><span data-stu-id="5997d-105">The **bufferingTime** property specifies or retrieves the amount of time in milliseconds allocated for buffering incoming data before playing begins.</span></span>

## <a name="syntax"></a><span data-ttu-id="5997d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5997d-106">Syntax</span></span>

<span data-ttu-id="5997d-107">*reproductor*. *red*. **bufferingTime**</span><span class="sxs-lookup"><span data-stu-id="5997d-107">*player*.*network*.**bufferingTime**</span></span>

## <a name="possible-values"></a><span data-ttu-id="5997d-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="5997d-108">Possible Values</span></span>

<span data-ttu-id="5997d-109">Esta propiedad es un **número** de lectura y escritura (**Long**) que va desde cero hasta 60.000 con un valor predeterminado de 5.000.</span><span class="sxs-lookup"><span data-stu-id="5997d-109">This property is a read/write **Number** (**long**) ranging from zero to 60,000 with a default value of 5,000.</span></span>

## <a name="examples"></a><span data-ttu-id="5997d-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5997d-110">Examples</span></span>

<span data-ttu-id="5997d-111">En el siguiente ejemplo de JScript se usa *Network*. **bufferingTime** para especificar el número de segundos asignados para almacenar en búfer los datos entrantes.</span><span class="sxs-lookup"><span data-stu-id="5997d-111">The following JScript example uses *Network*.**bufferingTime** to specify the number of seconds allocated for buffering incoming data.</span></span> <span data-ttu-id="5997d-112">La información se recupera de un elemento de entrada de texto HTML creado con ID = "bufText".</span><span class="sxs-lookup"><span data-stu-id="5997d-112">The information is retrieved from an HTML TEXT INPUT element created with ID = "bufText".</span></span> <span data-ttu-id="5997d-113">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5997d-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create a BUTTON element to change the bufferingTime value. -->
<INPUT TYPE = "BUTTON" NAME = "bufTime" ID = "bufTime" 
       VALUE = "Change Buffer Time"

    onClick = "
       /* Test whether the user entered a valid value. */
       if (bufText.value >= 0 & bufText.value <= 60) 
           Player.network.bufferingTime = bufText.value * 1000;
       else
           alert('Buffering time must be between 0 and 60.');
">

```



## <a name="requirements"></a><span data-ttu-id="5997d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5997d-114">Requirements</span></span>



| <span data-ttu-id="5997d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5997d-115">Requirement</span></span> | <span data-ttu-id="5997d-116">Value</span><span class="sxs-lookup"><span data-stu-id="5997d-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5997d-117">Versión</span><span class="sxs-lookup"><span data-stu-id="5997d-117">Version</span></span><br/> | <span data-ttu-id="5997d-118">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5997d-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5997d-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5997d-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="5997d-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5997d-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5997d-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="5997d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5997d-122">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="5997d-122">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





