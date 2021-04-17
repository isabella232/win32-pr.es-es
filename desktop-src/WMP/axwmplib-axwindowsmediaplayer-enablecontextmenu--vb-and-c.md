---
title: Propiedad AxWindowsMediaPlayer. enableContextMenu
description: La propiedad enableContextMenu obtiene o establece un valor que indica si se debe habilitar el menú contextual, que aparece al hacer clic con el botón secundario del mouse.
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- propiedades de enableContextMenu Media Player de Windows
- propiedad enableContextMenu Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad enableContextMenu
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.enableContextMenu
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09c705fd45b9b994863ab4f93df1c3ae10858930
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698554"
---
# <a name="axwindowsmediaplayerenablecontextmenu-property"></a><span data-ttu-id="b5065-106">Propiedad AxWindowsMediaPlayer. enableContextMenu</span><span class="sxs-lookup"><span data-stu-id="b5065-106">AxWindowsMediaPlayer.enableContextMenu property</span></span>

<span data-ttu-id="b5065-107">La propiedad enableContextMenu obtiene o establece un valor que indica si se debe habilitar el menú contextual, que aparece al hacer clic con el botón secundario del mouse.</span><span class="sxs-lookup"><span data-stu-id="b5065-107">The enableContextMenu property gets or sets a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5065-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5065-108">Syntax</span></span>


```CSharp
public System.Boolean enableContextMenu {get; set;}
```


```VB

Public Property enableContextMenu As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="b5065-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b5065-109">Property value</span></span>

<span data-ttu-id="b5065-110">Valor System. Boolean que indica si se debe habilitar el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="b5065-110">A System.Boolean value that indicates whether to enable the context menu.</span></span> <span data-ttu-id="b5065-111">El valor predeterminado es true.</span><span class="sxs-lookup"><span data-stu-id="b5065-111">The default value is true.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5065-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5065-112">Remarks</span></span>

<span data-ttu-id="b5065-113">Durante la reproducción a pantalla completa, Windows Media Player oculta el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a "none".</span><span class="sxs-lookup"><span data-stu-id="b5065-113">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="requirements"></a><span data-ttu-id="b5065-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5065-114">Requirements</span></span>



| <span data-ttu-id="b5065-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5065-115">Requirement</span></span> | <span data-ttu-id="b5065-116">Value</span><span class="sxs-lookup"><span data-stu-id="b5065-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5065-117">Versión</span><span class="sxs-lookup"><span data-stu-id="b5065-117">Version</span></span><br/>   | <span data-ttu-id="b5065-118">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="b5065-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="b5065-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b5065-119">Namespace</span></span><br/> | <span data-ttu-id="b5065-120">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="b5065-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b5065-121">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="b5065-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b5065-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b5065-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5065-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5065-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5065-124">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b5065-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





