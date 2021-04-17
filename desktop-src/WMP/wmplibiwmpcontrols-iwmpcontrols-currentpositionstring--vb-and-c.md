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
# <a name="iwmpcontrolscurrentpositionstring-property"></a>IWMPControls:: currentPositionString (propiedad)

La propiedad **currentPositionString** obtiene la posición actual en el elemento multimedia como una cadena con el formato HH: mm: SS (horas, minutos y segundos).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String currentPositionString {get;}
```


```VB

Public ReadOnly Property currentPositionString As System.String
```





## <a name="property-value"></a>Valor de propiedad

Una **cadena System. String** con formato que es la posición actual.

## <a name="remarks"></a>Observaciones

Si el elemento multimedia tiene una longitud inferior a una hora, la posición actual tiene el formato MM: SS (minutos y segundos).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se inicia un temporizador que desencadena un evento a intervalos de un segundo. En el controlador de eventos Timer, se actualiza una etiqueta con **currentPositionString**. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


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





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPControls (VB y C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls. currentPosition (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





