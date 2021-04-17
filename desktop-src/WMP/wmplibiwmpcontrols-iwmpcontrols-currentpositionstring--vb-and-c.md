---
title: Propiedad currentPositionString de IWMPControls
description: La propiedad currentPositionString obtiene la posición actual en el elemento multimedia como una cadena con el formato HH MM SS (horas, minutos y segundos).
ms.assetid: cd28dafa-b6a4-4bed-aa5d-7e7be6af1426
keywords:
- propiedades de currentPositionString Media Player de Windows
- propiedad currentPositionString de Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, propiedad currentPositionString
topic_type:
- apiref
api_name:
- IWMPControls.currentPositionString
- IWMPControls.get_currentPositionString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e941fceb61e4f00393b05f96489ec7ac8e950f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690889"
---
# <a name="iwmpcontrolscurrentpositionstring-property"></a><span data-ttu-id="4c233-106">IWMPControls:: currentPositionString (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4c233-106">IWMPControls::currentPositionString property</span></span>

<span data-ttu-id="4c233-107">La propiedad **currentPositionString** obtiene la posición actual en el elemento multimedia como una cadena con el formato HH: mm: SS (horas, minutos y segundos).</span><span class="sxs-lookup"><span data-stu-id="4c233-107">The **currentPositionString** property gets the current position in the media item as a string formatted as HH:MM:SS (hours, minutes, and seconds).</span></span>

<span data-ttu-id="4c233-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4c233-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c233-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c233-109">Syntax</span></span>


```CSharp
public System.String currentPositionString {get;}
```


```VB

Public ReadOnly Property currentPositionString As System.String
```





## <a name="property-value"></a><span data-ttu-id="4c233-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4c233-110">Property value</span></span>

<span data-ttu-id="4c233-111">Una **cadena System. String** con formato que es la posición actual.</span><span class="sxs-lookup"><span data-stu-id="4c233-111">A formatted **System.String** that is the current position.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c233-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c233-112">Remarks</span></span>

<span data-ttu-id="4c233-113">Si el elemento multimedia tiene una longitud inferior a una hora, la posición actual tiene el formato MM: SS (minutos y segundos).</span><span class="sxs-lookup"><span data-stu-id="4c233-113">If the media item is less than an hour long, the current position is formatted as MM:SS (minutes and seconds).</span></span>

## <a name="examples"></a><span data-ttu-id="4c233-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4c233-114">Examples</span></span>

<span data-ttu-id="4c233-115">En el ejemplo siguiente se inicia un temporizador que desencadena un evento a intervalos de un segundo.</span><span class="sxs-lookup"><span data-stu-id="4c233-115">The following example starts a timer that triggers an event at one-second intervals.</span></span> <span data-ttu-id="4c233-116">En el controlador de eventos Timer, se actualiza una etiqueta con **currentPositionString**.</span><span class="sxs-lookup"><span data-stu-id="4c233-116">In the timer event handler, a label is updated with the **currentPositionString**.</span></span> <span data-ttu-id="4c233-117">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="4c233-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 
   
// Update the text of the label with the currentPositionString.
private void TimerEventProcessor(object sender, System.EventArgs e)
{
    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString;
}
```


```VB

' Set the timer to fire an event every second and start the timer.
timer.Interval = 1000
timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
&#39; determine when to start and stop the timer. 

&#39; Update the text of the label with the currentPositionString.
Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4c233-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c233-118">Requirements</span></span>



| <span data-ttu-id="4c233-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c233-119">Requirement</span></span> | <span data-ttu-id="4c233-120">Value</span><span class="sxs-lookup"><span data-stu-id="4c233-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c233-121">Versión</span><span class="sxs-lookup"><span data-stu-id="4c233-121">Version</span></span><br/>   | <span data-ttu-id="4c233-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="4c233-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4c233-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4c233-123">Namespace</span></span><br/> | <span data-ttu-id="4c233-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4c233-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4c233-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="4c233-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4c233-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4c233-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c233-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c233-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c233-128">**Interfaz IWMPControls (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4c233-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4c233-129">**IWMPControls. currentPosition (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="4c233-129">**IWMPControls.currentPosition (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





