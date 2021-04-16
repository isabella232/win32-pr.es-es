---
title: Propiedad invokeURLs de IWMPSettings
description: La propiedad invokeURLs obtiene o establece un valor que indica si los eventos de dirección URL deben iniciar un explorador Web.
ms.assetid: e16c968d-a1b7-4c3a-9c1a-5748ed44cdac
keywords:
- propiedades de invokeURLs Media Player de Windows
- propiedad invokeURLs de Windows Media Player, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad invokeURLs
topic_type:
- apiref
api_name:
- IWMPSettings.invokeURLs
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbdd68d797b54f4e9365f381b2b5c705dffc419b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105719026"
---
# <a name="iwmpsettingsinvokeurls-property"></a><span data-ttu-id="9595e-106">IWMPSettings:: invokeURLs (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9595e-106">IWMPSettings::invokeURLs property</span></span>

<span data-ttu-id="9595e-107">La propiedad **invokeURLs** obtiene o establece un valor que indica si los eventos de dirección URL deben iniciar un explorador Web.</span><span class="sxs-lookup"><span data-stu-id="9595e-107">The **invokeURLs** property gets or sets a value indicating whether URL events should launch a Web browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="9595e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9595e-108">Syntax</span></span>


```CSharp
public System.Boolean invokeURLs {get; set;}
```


```VB

Public Property invokeURLs As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="9595e-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9595e-109">Property value</span></span>

<span data-ttu-id="9595e-110">Un valor **System. Boolean** que indica si los eventos de dirección URL deben iniciar un explorador Web.</span><span class="sxs-lookup"><span data-stu-id="9595e-110">A **System.Boolean** value indicating whether URL events should launch a Web browser.</span></span> <span data-ttu-id="9595e-111">El valor predeterminado es **true**.</span><span class="sxs-lookup"><span data-stu-id="9595e-111">The default is **true**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9595e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9595e-112">Remarks</span></span>

<span data-ttu-id="9595e-113">Los archivos multimedia digitales y las secuencias pueden contener comandos de script de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="9595e-113">Digital media files and streams can contain URL script commands.</span></span> <span data-ttu-id="9595e-114">Cuando se envía un comando de script de dirección URL al control Media Player de Windows, se pasa primero al controlador de eventos **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** , independientemente del valor recuperado por **invokeURLs**.</span><span class="sxs-lookup"><span data-stu-id="9595e-114">When a URL script command is sent to the Windows Media Player control, it is passed first to the **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event handler regardless of the value retrieved by **invokeURLs**.</span></span> <span data-ttu-id="9595e-115">Después de que **\_ WMPOCXEvents \_ ScriptCommandEvent** se cierre, Windows Media Player comprueba **invokeURLs** para determinar si se debe iniciar el explorador Web predeterminado con la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="9595e-115">After **\_WMPOCXEvents\_ScriptCommandEvent** exits, Windows Media Player checks **invokeURLs** to determine whether to launch the default Web browser with the URL.</span></span> <span data-ttu-id="9595e-116">Puede mostrar las direcciones URL de forma selectiva al comprobarlas en **\_ WMPOCXEvents \_ ScriptCommandEvent** y establecer **invokeURLs** como desee.</span><span class="sxs-lookup"><span data-stu-id="9595e-116">You can selectively display URLs by checking them in **\_WMPOCXEvents\_ScriptCommandEvent** and setting **invokeURLs** as desired.</span></span>

## <a name="requirements"></a><span data-ttu-id="9595e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9595e-117">Requirements</span></span>



| <span data-ttu-id="9595e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9595e-118">Requirement</span></span> | <span data-ttu-id="9595e-119">Value</span><span class="sxs-lookup"><span data-stu-id="9595e-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9595e-120">Versión</span><span class="sxs-lookup"><span data-stu-id="9595e-120">Version</span></span><br/>   | <span data-ttu-id="9595e-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="9595e-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9595e-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9595e-122">Namespace</span></span><br/> | <span data-ttu-id="9595e-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9595e-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9595e-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="9595e-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9595e-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9595e-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9595e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="9595e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9595e-127">**Evento AxWindowsMediaPlayer. comando (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="9595e-127">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="9595e-128">**Interfaz IWMPSettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="9595e-128">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





