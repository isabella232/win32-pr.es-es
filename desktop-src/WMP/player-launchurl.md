---
title: Player. launchURL (método)
description: El método launchURL envía una dirección URL al explorador predeterminado del usuario que se va a representar. | Player. launchURL (método)
ms.assetid: 2b445e59-f884-4519-9acb-f349319429d2
keywords:
- método launchURL de Windows Media Player
- método launchURL Windows Media Player, clase Player
- Clase Player Media Player Windows, método launchURL
topic_type:
- apiref
api_name:
- Player.launchURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c496e8f40f4d7c8a21e718b820e438d3ce32ad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690156"
---
# <a name="playerlaunchurl-method"></a><span data-ttu-id="04086-107">Player. launchURL (método)</span><span class="sxs-lookup"><span data-stu-id="04086-107">Player.launchURL method</span></span>

<span data-ttu-id="04086-108">El método **launchURL** envía una dirección URL al explorador predeterminado del usuario que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="04086-108">The **launchURL** method sends a URL to the user's default browser to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="04086-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04086-109">Syntax</span></span>


```JScript
Player.launchURL(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="04086-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04086-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04086-111">*Dirección URL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="04086-111">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04086-112">Valor de **cadena** que representa la dirección URL que se va a iniciar.</span><span class="sxs-lookup"><span data-stu-id="04086-112">**String** value representing the URL to launch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04086-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04086-113">Return value</span></span>

<span data-ttu-id="04086-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="04086-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04086-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04086-115">Remarks</span></span>

<span data-ttu-id="04086-116">Este método solo abre páginas web mediante los protocolos HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="04086-116">This method only opens webpages using the HTTP or HTTPS protocols.</span></span>

<span data-ttu-id="04086-117">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="04086-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="04086-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="04086-118">Examples</span></span>

<span data-ttu-id="04086-119">En el ejemplo siguiente se crea un elemento de botón HTML que, cuando se hace clic en él, muestra el sitio web de Microsoft en una nueva ventana del explorador.</span><span class="sxs-lookup"><span data-stu-id="04086-119">The following example creates an HTML BUTTON element that, when clicked, displays the Microsoft website in a new browser window.</span></span> <span data-ttu-id="04086-120">El elemento **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="04086-120">The **Player** element was created with ID = "Player".</span></span>


```JScript
<INPUT  TYPE = "BUTTON"  ID = "GOTOMS"  VALUE = "Microsoft.com"  onClick = "

    /* Open the Microsoft website. */
    Player.launchURL('https://www.microsoft.com');
">

```



## <a name="requirements"></a><span data-ttu-id="04086-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04086-121">Requirements</span></span>



| <span data-ttu-id="04086-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="04086-122">Requirement</span></span> | <span data-ttu-id="04086-123">Value</span><span class="sxs-lookup"><span data-stu-id="04086-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04086-124">Versión</span><span class="sxs-lookup"><span data-stu-id="04086-124">Version</span></span><br/> | <span data-ttu-id="04086-125">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="04086-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="04086-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="04086-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="04086-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04086-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04086-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="04086-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04086-129">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="04086-129">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





