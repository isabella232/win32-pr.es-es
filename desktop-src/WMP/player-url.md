---
title: Player. URL
description: La propiedad URL especifica o recupera el nombre del elemento multimedia que se va a reproducir.
ms.assetid: 74987ffd-c625-4d30-9f5f-5170119158f9
keywords:
- Reproductor. URL de Windows Media Player
topic_type:
- apiref
api_name:
- Player.URL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d4f0c75ac0dddeeaced0f1a3a6f1247df4ae36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708760"
---
# <a name="playerurl"></a><span data-ttu-id="0b460-104">Player. URL</span><span class="sxs-lookup"><span data-stu-id="0b460-104">Player.URL</span></span>

<span data-ttu-id="0b460-105">La propiedad **URL** especifica o recupera el nombre del elemento multimedia que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="0b460-105">The **URL** property specifies or retrieves the name of the media item to play.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b460-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b460-106">Syntax</span></span>

<span data-ttu-id="0b460-107">*reproductor* . **Dirección URL**</span><span class="sxs-lookup"><span data-stu-id="0b460-107">*player* .**URL**</span></span>

## <a name="possible-values"></a><span data-ttu-id="0b460-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="0b460-108">Possible Values</span></span>

<span data-ttu-id="0b460-109">Esta propiedad es una **cadena** de lectura/escritura sin ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0b460-109">This property is a read/write **String** with no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b460-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b460-110">Remarks</span></span>

<span data-ttu-id="0b460-111">Esta propiedad solo se puede establecer en una dirección URL en una zona de seguridad que sea igual o menos restrictiva que la zona de seguridad del programa o la página web que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="0b460-111">This property can only be set to a URL in a security zone that is the same or is less restrictive than the security zone of the calling program or webpage.</span></span>

<span data-ttu-id="0b460-112">Las aplicaciones que abren elementos multimedia de detrás de un firewall tendrán un mejor rendimiento si la dirección se especifica mediante el nombre del servidor de nombres de dominio (DNS) en lugar de la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="0b460-112">Applications that open media items from behind a firewall will have better performance if the address is specified using the domain name server (DNS) name instead of the IP address.</span></span>

<span data-ttu-id="0b460-113">No llame a este método desde el código del controlador de eventos.</span><span class="sxs-lookup"><span data-stu-id="0b460-113">Do not call this method from event handler code.</span></span> <span data-ttu-id="0b460-114">Llamando al *reproductor*. La **dirección URL** de un controlador de eventos puede producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="0b460-114">Calling *Player*.**URL** from an event handler may yield unexpected results.</span></span>

## <a name="examples"></a><span data-ttu-id="0b460-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0b460-115">Examples</span></span>

<span data-ttu-id="0b460-116">En el ejemplo siguiente se crea un elemento de entrada de texto HTML y un elemento de entrada de botón HTML.</span><span class="sxs-lookup"><span data-stu-id="0b460-116">The following example creates an HTML TEXT input element and an HTML BUTTON input element.</span></span> <span data-ttu-id="0b460-117">El elemento de texto permite al usuario escribir una ruta de acceso para especificar un archivo multimedia digital que se va a reproducir.</span><span class="sxs-lookup"><span data-stu-id="0b460-117">The TEXT element allows the user to type a path to specify a digital media file to play.</span></span> <span data-ttu-id="0b460-118">El elemento BUTTON ejecuta JScript que abre el archivo e inicia Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0b460-118">The BUTTON element executes JScript that opens the file and starts Windows Media Player.</span></span> <span data-ttu-id="0b460-119">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="0b460-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an INPUT control to get a file path from the user. -->
<INPUT Type = "TEXT" ID = "inputURL">

<!-- Create a BUTTON control to execute the script. -->
<INPUT  Type = "BUTTON"  ID = "openMedia"  VALUE = "Open Media"
    onClick = "
        /* Specify the URL obtained from user input. */
        Player.URL = inputURL.value;

        /* Start the Player. */
        Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="0b460-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b460-120">Requirements</span></span>



| <span data-ttu-id="0b460-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b460-121">Requirement</span></span> | <span data-ttu-id="0b460-122">Value</span><span class="sxs-lookup"><span data-stu-id="0b460-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0b460-123">Versión</span><span class="sxs-lookup"><span data-stu-id="0b460-123">Version</span></span><br/> | <span data-ttu-id="0b460-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="0b460-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0b460-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b460-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="0b460-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b460-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b460-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b460-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b460-128">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="0b460-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





