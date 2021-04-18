---
title: Método ShowPopupMenu
description: Método ShowPopupMenu
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0325a552cc3c1f91a64c1240964f1d0c329292c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704583"
---
# <a name="showpopupmenu-method"></a><span data-ttu-id="67bb7-103">Método ShowPopupMenu</span><span class="sxs-lookup"><span data-stu-id="67bb7-103">ShowPopupMenu Method</span></span>

<span data-ttu-id="67bb7-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="67bb7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="67bb7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="67bb7-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="67bb7-106">Muestra el menú emergente del carácter situado en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="67bb7-106">Displays the character's pop-up menu at the specified location.</span></span>

</dd> <dt>

<span data-ttu-id="67bb7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="67bb7-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="67bb7-108">*directivas. ***Caracteres ("*** CharacterID ***"). ShowPopupMenu*** x, y*</span><span class="sxs-lookup"><span data-stu-id="67bb7-108">*agent.\*\*\*Characters("*\*\* CharacterID ***").ShowPopupMenu*** x, y\*</span></span>



| <span data-ttu-id="67bb7-109">Parte</span><span class="sxs-lookup"><span data-stu-id="67bb7-109">Part</span></span> | <span data-ttu-id="67bb7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="67bb7-110">Description</span></span>                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67bb7-111">*x*</span><span class="sxs-lookup"><span data-stu-id="67bb7-111">*x*</span></span>  | <span data-ttu-id="67bb7-112">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="67bb7-112">Required.</span></span> <span data-ttu-id="67bb7-113">Valor entero que indica la coordenada de pantalla horizontal (*x*) para mostrar el menú.</span><span class="sxs-lookup"><span data-stu-id="67bb7-113">An integer value that indicates the horizontal (*x*) screen coordinate to display the menu.</span></span> <span data-ttu-id="67bb7-114">Estas coordenadas se deben especificar en píxeles.</span><span class="sxs-lookup"><span data-stu-id="67bb7-114">These coordinates must be specified in pixels.</span></span> |
| <span data-ttu-id="67bb7-115">*y*</span><span class="sxs-lookup"><span data-stu-id="67bb7-115">*y*</span></span>  | <span data-ttu-id="67bb7-116">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="67bb7-116">Required.</span></span> <span data-ttu-id="67bb7-117">Valor entero que indica la coordenada de pantalla vertical (*y*) para mostrar el menú.</span><span class="sxs-lookup"><span data-stu-id="67bb7-117">An integer value that indicates the vertical (*y*) screen coordinate to display the menu.</span></span> <span data-ttu-id="67bb7-118">Estas coordenadas se deben especificar en píxeles.</span><span class="sxs-lookup"><span data-stu-id="67bb7-118">These coordinates must be specified in pixels.</span></span>   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67bb7-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67bb7-119">Remarks</span></span>

<span data-ttu-id="67bb7-120">El agente muestra automáticamente el menú emergente del carácter cuando el usuario hace clic con el botón secundario en el carácter.</span><span class="sxs-lookup"><span data-stu-id="67bb7-120">Agent automatically displays the character's pop-up menu when the user right-clicks the character.</span></span> <span data-ttu-id="67bb7-121">Si establece [**AutoPopupMenu**](autopopupmenu-property.md) en **false**, puede usar este método para mostrar el menú.</span><span class="sxs-lookup"><span data-stu-id="67bb7-121">If you set [**AutoPopupMenu**](autopopupmenu-property.md) to **False**, you can use this method to display the menu.</span></span>

<span data-ttu-id="67bb7-122">El menú permanecerá en pantalla hasta que el usuario seleccione un comando o muestre otro menú.</span><span class="sxs-lookup"><span data-stu-id="67bb7-122">The menu remains displayed until the user selects a command or displays another menu.</span></span> <span data-ttu-id="67bb7-123">Solo se puede mostrar un menú emergente a la vez; por lo tanto, las llamadas a este método cancelarán (quitará) el menú anterior.</span><span class="sxs-lookup"><span data-stu-id="67bb7-123">Only one pop-up menu can be displayed at a time; therefore, calls to this method will cancel (remove) the former menu.</span></span>

<span data-ttu-id="67bb7-124">Solo se debe llamar a este método cuando la aplicación cliente es el cliente activo del carácter; en caso contrario, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="67bb7-124">This method should be called only when your client application is the active client of the character; otherwise it fails.</span></span> <span data-ttu-id="67bb7-125">Para determinar si este método se ha ejecutado correctamente, puede llamarlo como una función y devolverá un valor booleano que indica si el método se ha ejecutado correctamente.</span><span class="sxs-lookup"><span data-stu-id="67bb7-125">To determine the success of this method you can call it as a function and it will return a Boolean value indicating whether the method succeeded.</span></span>


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a><span data-ttu-id="67bb7-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="67bb7-126">See Also</span></span>

[<span data-ttu-id="67bb7-127">**Propiedad AutoPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="67bb7-127">**AutoPopupMenu property**</span></span>](autopopupmenu-property.md)


 

 




