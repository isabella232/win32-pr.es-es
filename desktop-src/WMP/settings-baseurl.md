---
title: Settings. baseURL
description: La propiedad baseURL especifica o recupera la dirección URL base que se usa para la resolución de la ruta de acceso relativa con comandos de script de dirección URL que están incrustados en elementos multimedia.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- Settings. baseURL Windows Media Player
topic_type:
- apiref
api_name:
- Settings.baseURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed77d90c8ffadc4dd8da0951f7e6a477db3f9de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649555"
---
# <a name="settingsbaseurl"></a><span data-ttu-id="76ff7-104">Settings. baseURL</span><span class="sxs-lookup"><span data-stu-id="76ff7-104">Settings.baseURL</span></span>

<span data-ttu-id="76ff7-105">La propiedad **baseurl** especifica o recupera la dirección URL base que se usa para la resolución de la ruta de acceso relativa con comandos de script de dirección URL que están incrustados en elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="76ff7-105">The **baseURL** property specifies or retrieves the base URL used for relative path resolution with URL script commands that are embedded in media items.</span></span>

## <a name="syntax"></a><span data-ttu-id="76ff7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76ff7-106">Syntax</span></span>

<span data-ttu-id="76ff7-107">Player. Settings. baseURL</span><span class="sxs-lookup"><span data-stu-id="76ff7-107">player.settings.baseURL</span></span>

## <a name="possible-values"></a><span data-ttu-id="76ff7-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="76ff7-108">Possible Values</span></span>

<span data-ttu-id="76ff7-109">Esta propiedad es una **cadena** de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="76ff7-109">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="76ff7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76ff7-110">Remarks</span></span>

<span data-ttu-id="76ff7-111">Esta propiedad especifica la dirección URL HTTP base que el evento **comando** pasa como parámetro de comando.</span><span class="sxs-lookup"><span data-stu-id="76ff7-111">This property specifies the base HTTP URL that is passed as the command parameter by the **ScriptCommand** event.</span></span> <span data-ttu-id="76ff7-112">La dirección URL base se concatena con la dirección URL relativa como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="76ff7-112">The base URL is concatenated with the relative URL as follows:</span></span>

1.  <span data-ttu-id="76ff7-113">Se agrega una barra diagonal final (/) al valor de la propiedad **baseurl** .</span><span class="sxs-lookup"><span data-stu-id="76ff7-113">A trailing forward slash (/) is added to the value of the **baseURL** property.</span></span>
2.  <span data-ttu-id="76ff7-114">Un punto inicial, una barra diagonal inversa o una barra diagonal (., \\ y/) se eliminan de la dirección URL relativa.</span><span class="sxs-lookup"><span data-stu-id="76ff7-114">A leading period, backward slash, or forward slash (., \\, and /) are deleted from the relative URL.</span></span>
3.  <span data-ttu-id="76ff7-115">La dirección URL relativa se agrega al final de la dirección URL base.</span><span class="sxs-lookup"><span data-stu-id="76ff7-115">The relative URL is added to the end of the base URL.</span></span>
4.  <span data-ttu-id="76ff7-116">Todas las barras diagonales de la dirección URL completa resultante se señalan en la misma dirección (convertida en barras diagonales o hacia delante) en función de la dirección del primer carácter de barra diagonal que se encuentre en la nueva dirección URL.</span><span class="sxs-lookup"><span data-stu-id="76ff7-116">All slashes in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</span></span>

<span data-ttu-id="76ff7-117">**Note**</span><span class="sxs-lookup"><span data-stu-id="76ff7-117">**Note**</span></span>

<span data-ttu-id="76ff7-118">El control Player no admite el uso de dos puntos (..) en la dirección URL relativa para indicar el elemento primario de la ubicación actual.</span><span class="sxs-lookup"><span data-stu-id="76ff7-118">The player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.</span></span>

<span data-ttu-id="76ff7-119">**Windows Media Player 10 Mobile**: esta propiedad es de solo lectura y siempre devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="76ff7-119">**Windows Media Player 10 Mobile**: This property is read-only, and always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="76ff7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76ff7-120">Requirements</span></span>



| <span data-ttu-id="76ff7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="76ff7-121">Requirement</span></span> | <span data-ttu-id="76ff7-122">Value</span><span class="sxs-lookup"><span data-stu-id="76ff7-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76ff7-123">Versión</span><span class="sxs-lookup"><span data-stu-id="76ff7-123">Version</span></span><br/> | <span data-ttu-id="76ff7-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="76ff7-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="76ff7-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="76ff7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="76ff7-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76ff7-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76ff7-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="76ff7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ff7-128">**Evento Player. comando**</span><span class="sxs-lookup"><span data-stu-id="76ff7-128">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="76ff7-129">**Objeto de configuración**</span><span class="sxs-lookup"><span data-stu-id="76ff7-129">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





