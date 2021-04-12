---
title: Idleon (propiedad)
description: Idleon (propiedad)
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7fcec4bd6e163baab7722e4d893146819408a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356652"
---
# <a name="idleon-property"></a><span data-ttu-id="deb56-103">Idleon (propiedad)</span><span class="sxs-lookup"><span data-stu-id="deb56-103">IdleOn Property</span></span>

<span data-ttu-id="deb56-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="deb56-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="deb56-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="deb56-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="deb56-106">Devuelve o establece un valor booleano que determina si el servidor administra las animaciones de estado de **ralentí** del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="deb56-106">Returns or sets a Boolean value that determines whether the server manages the specified character's **Idling** state animations.</span></span>

</dd> <dt>

<span data-ttu-id="deb56-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="deb56-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="deb56-108">\*agente ***. Caracteres ("*** CharacterID \* *"). Idleon* \*  \[  =  *Boolean*\]</span><span class="sxs-lookup"><span data-stu-id="deb56-108">*agent ***.Characters ("*** CharacterID\*\*\*").IdleOn*\* \[ = *boolean*\]</span></span>

</dd> </dl> 

| <span data-ttu-id="deb56-109">Parte</span><span class="sxs-lookup"><span data-stu-id="deb56-109">Part</span></span>      | <span data-ttu-id="deb56-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="deb56-110">Description</span></span>                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="deb56-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="deb56-111">*boolean*</span></span> | <span data-ttu-id="deb56-112">Una expresión booleana que especifica si el servidor administra el modo de inactividad.</span><span class="sxs-lookup"><span data-stu-id="deb56-112">A Boolean expression specifying whether the server manages idle mode.</span></span> <span data-ttu-id="deb56-113">**True** (valor predeterminado) el control de servidor del estado de inactividad está habilitado.</span><span class="sxs-lookup"><span data-stu-id="deb56-113">**True** (Default) Server handling of the idle state is enabled.</span></span> <br/> <span data-ttu-id="deb56-114">**False** El control de servidor del estado de inactividad está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="deb56-114">**False** Server handling of the idle state is disabled.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="deb56-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="deb56-115">Remarks</span></span>

<span data-ttu-id="deb56-116">El servidor establece automáticamente un tiempo de espera después de la última animación reproducida para un carácter.</span><span class="sxs-lookup"><span data-stu-id="deb56-116">The server automatically sets a time-out after the last animation played for a character.</span></span> <span data-ttu-id="deb56-117">Una vez completado el intervalo de este temporizador, el servidor inicia el estado de **ralentí** para un carácter y reproduce sus animaciones de inactiva **asociadas a intervalos** regulares.</span><span class="sxs-lookup"><span data-stu-id="deb56-117">When this timer's interval is complete, the server begins the **Idling** state for a character, playing its associated **Idling** animations at regular intervals.</span></span> <span data-ttu-id="deb56-118">Si desea deshabilitar el servidor para que reproduzca automáticamente las animaciones de estado de **ralentí** , establezca la propiedad en **false** y reproduzca una animación o llame al método [**Stop**](stop-method.md) .</span><span class="sxs-lookup"><span data-stu-id="deb56-118">If you want to disable the server from automatically playing the **Idling** state animations, set the property to **False** and play an animation or call the [**Stop**](stop-method.md) method.</span></span> <span data-ttu-id="deb56-119">El establecimiento de este valor no afecta al estado de animación actual del carácter.</span><span class="sxs-lookup"><span data-stu-id="deb56-119">Setting this value does not affect the current animation state of the character.</span></span>

<span data-ttu-id="deb56-120">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="deb56-120">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 





