---
title: Configuración. saldo
description: La propiedad balance especifica o recupera el equilibrio estéreo actual.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Configuración. saldo de Windows Media Player
topic_type:
- apiref
api_name:
- Settings.balance
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248cd3b2bbf735ef54382fb5b1be52755cad3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649557"
---
# <a name="settingsbalance"></a><span data-ttu-id="0d74d-104">Configuración. saldo</span><span class="sxs-lookup"><span data-stu-id="0d74d-104">Settings.balance</span></span>

<span data-ttu-id="0d74d-105">La propiedad **balance** especifica o recupera el equilibrio estéreo actual.</span><span class="sxs-lookup"><span data-stu-id="0d74d-105">The **balance** property specifies or retrieves the current stereo balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d74d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d74d-106">Syntax</span></span>

<span data-ttu-id="0d74d-107">Player. Settings. balance</span><span class="sxs-lookup"><span data-stu-id="0d74d-107">player.settings.balance</span></span>

## <a name="possible-values"></a><span data-ttu-id="0d74d-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="0d74d-108">Possible Values</span></span>

<span data-ttu-id="0d74d-109">Esta propiedad es un **número** de lectura y escritura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="0d74d-109">This property is a read/write **Number** (**long**).</span></span> <span data-ttu-id="0d74d-110">Los valores van de 100 a 100, con un valor predeterminado de cero.</span><span class="sxs-lookup"><span data-stu-id="0d74d-110">Values range from  100 to 100, with a default value of zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d74d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d74d-111">Remarks</span></span>

<span data-ttu-id="0d74d-112">El valor cero indica que el audio se reproduce en el mismo volumen en los canales izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="0d74d-112">The value zero indicates that the audio plays at equal volume on both left and right channels.</span></span> <span data-ttu-id="0d74d-113">Un valor de 100 indica que el audio se reproduce solo en el canal izquierdo.</span><span class="sxs-lookup"><span data-stu-id="0d74d-113">A value of  100 indicates that audio plays only on the left channel.</span></span> <span data-ttu-id="0d74d-114">Un valor de 100 indica que el audio se reproduce solo en el canal derecho.</span><span class="sxs-lookup"><span data-stu-id="0d74d-114">A value of 100 indicates that audio plays only on the right channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d74d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d74d-115">Requirements</span></span>



| <span data-ttu-id="0d74d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d74d-116">Requirement</span></span> | <span data-ttu-id="0d74d-117">Value</span><span class="sxs-lookup"><span data-stu-id="0d74d-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d74d-118">Versión</span><span class="sxs-lookup"><span data-stu-id="0d74d-118">Version</span></span><br/> | <span data-ttu-id="0d74d-119">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="0d74d-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0d74d-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d74d-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="0d74d-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d74d-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d74d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d74d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d74d-123">**Objeto de configuración**</span><span class="sxs-lookup"><span data-stu-id="0d74d-123">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





