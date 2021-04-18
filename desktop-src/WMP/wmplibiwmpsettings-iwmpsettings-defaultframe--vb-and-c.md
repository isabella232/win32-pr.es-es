---
title: Propiedad defaultFrame de IWMPSettings
description: La propiedad defaultFrame obtiene o establece el nombre del marco que se usa para mostrar una dirección URL que se recibe en \_ un \_ evento AxWindowsMediaPlayer WMPOCXEvents ScriptCommandEvent.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- propiedades de defaultFrame Media Player de Windows
- propiedad defaultFrame de Windows Media Player, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad defaultFrame
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28539640214165ab5b2808762ed854b19b434311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718698"
---
# <a name="iwmpsettingsdefaultframe-property"></a><span data-ttu-id="ca7d1-106">IWMPSettings::d propiedad efaultFrame</span><span class="sxs-lookup"><span data-stu-id="ca7d1-106">IWMPSettings::defaultFrame property</span></span>

<span data-ttu-id="ca7d1-107">La propiedad **defaultFrame** obtiene o establece el nombre del marco que se usa para mostrar una dirección URL que se recibe en un evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** .</span><span class="sxs-lookup"><span data-stu-id="ca7d1-107">The **defaultFrame** property gets or sets the name of the frame used to display a URL that is received in an **AxWindowsMediaPlayer\_WMPOCXEvents\_ScriptCommandEvent** event.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca7d1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca7d1-108">Syntax</span></span>


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a><span data-ttu-id="ca7d1-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ca7d1-109">Property value</span></span>

<span data-ttu-id="ca7d1-110">**System. String** que es el valor del atributo name del elemento de **marco** de destino.</span><span class="sxs-lookup"><span data-stu-id="ca7d1-110">A **System.String** that is the value of the name attribute of the target **FRAME** element.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca7d1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca7d1-111">Remarks</span></span>

<span data-ttu-id="ca7d1-112">Si se especifica un marco de destino en el propio evento **\_ WMPOCXEvents \_ ScriptCommandEvent** , esta propiedad se omite.</span><span class="sxs-lookup"><span data-stu-id="ca7d1-112">If a target frame is specified in the **\_WMPOCXEvents\_ScriptCommandEvent** event itself, this property is ignored.</span></span>

<span data-ttu-id="ca7d1-113">Esta propiedad se omite cuando se usa el applet Java de Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="ca7d1-113">This property is ignored when using the Netscape Navigator Java applet.</span></span> <span data-ttu-id="ca7d1-114">En Netscape Navigator, cada comando de script de dirección URL recibido mostrará la dirección URL en una nueva ventana del explorador, independientemente del valor de **defaultFrame**.</span><span class="sxs-lookup"><span data-stu-id="ca7d1-114">In Netscape Navigator, each URL script command received will display the URL in a new browser window, regardless of the value of **defaultFrame**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca7d1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca7d1-115">Requirements</span></span>



| <span data-ttu-id="ca7d1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca7d1-116">Requirement</span></span> | <span data-ttu-id="ca7d1-117">Value</span><span class="sxs-lookup"><span data-stu-id="ca7d1-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca7d1-118">Versión</span><span class="sxs-lookup"><span data-stu-id="ca7d1-118">Version</span></span><br/>   | <span data-ttu-id="ca7d1-119">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="ca7d1-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ca7d1-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ca7d1-120">Namespace</span></span><br/> | <span data-ttu-id="ca7d1-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ca7d1-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ca7d1-122">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="ca7d1-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ca7d1-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ca7d1-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca7d1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca7d1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca7d1-125">**Evento AxWindowsMediaPlayer. comando (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ca7d1-125">**AxWindowsMediaPlayer.ScriptCommand Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="ca7d1-126">**Interfaz IWMPSettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="ca7d1-126">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





