---
title: Propiedad AutoPopupMenu
description: Propiedad AutoPopupMenu
ms.assetid: 499092cb-0990-4edb-915c-12e3011de142
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d4ebfc559c88c3750a338f30b5dee4aad66ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357486"
---
# <a name="autopopupmenu-property"></a><span data-ttu-id="83c55-103">Propiedad AutoPopupMenu</span><span class="sxs-lookup"><span data-stu-id="83c55-103">AutoPopupMenu Property</span></span>

<span data-ttu-id="83c55-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="83c55-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="83c55-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="83c55-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="83c55-106">Devuelve o establece si al hacer clic con el botón secundario en el carácter o en el icono de la barra de tareas se muestra automáticamente el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="83c55-106">Returns or sets whether right-clicking the character or its taskbar icon automatically displays the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="83c55-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="83c55-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="83c55-108">\*agente. ***Caracteres \* \* \* \* ("*** CharacterID \* \* *"). AutoPopupMenu* \*  \[  =  *booleano*\]</span><span class="sxs-lookup"><span data-stu-id="83c55-108">*agent.\*\*\*Characters\*\*\*\*("*\*\* CharacterID\***").AutoPopupMenu** \[ = *boolean*\]</span></span>



| <span data-ttu-id="83c55-109">Parte</span><span class="sxs-lookup"><span data-stu-id="83c55-109">Part</span></span>      | <span data-ttu-id="83c55-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="83c55-110">Description</span></span>                                                                                                                                                                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83c55-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="83c55-111">*boolean*</span></span> | <span data-ttu-id="83c55-112">Una expresión booleana que especifica si el servidor muestra automáticamente el menú emergente del carácter al hacer clic con el botón secundario.</span><span class="sxs-lookup"><span data-stu-id="83c55-112">A Boolean expression specifying whether the server automatically displays the character's pop-up menu on right-click.</span></span> <span data-ttu-id="83c55-113">**True** (valor predeterminado) muestra el menú al hacer clic con el botón secundario.</span><span class="sxs-lookup"><span data-stu-id="83c55-113">**True** (Default) Displays the menu on right-click.</span></span> <br/> <span data-ttu-id="83c55-114">**False** No muestra el menú al hacer clic con el botón secundario.</span><span class="sxs-lookup"><span data-stu-id="83c55-114">**False** Does not display the menu on right-click.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83c55-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83c55-115">Remarks</span></span>

<span data-ttu-id="83c55-116">Al establecer esta propiedad en **false**, puede crear su propio comportamiento de control de menús.</span><span class="sxs-lookup"><span data-stu-id="83c55-116">By setting this property to **False**, you can create your own menu-handling behavior.</span></span> <span data-ttu-id="83c55-117">Para mostrar el menú después de establecer esta propiedad en **false**, use el método [**ShowPopupMenu**](showpopupmenu-method.md) .</span><span class="sxs-lookup"><span data-stu-id="83c55-117">To display the menu after setting this property to **False**, use the [**ShowPopupMenu**](showpopupmenu-method.md) method.</span></span>

<span data-ttu-id="83c55-118">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="83c55-118">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="83c55-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="83c55-119">See Also</span></span>

[<span data-ttu-id="83c55-120">**Método ShowPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="83c55-120">**ShowPopupMenu method**</span></span>](showpopupmenu-method.md)


 

 





