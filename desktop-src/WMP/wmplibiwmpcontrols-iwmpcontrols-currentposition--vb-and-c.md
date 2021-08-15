---
title: Propiedad currentPosition de IWMPControls
description: La propiedad currentPosition obtiene o establece la posición actual en el elemento multimedia en segundos desde el principio.
ms.assetid: 48f5241e-7528-485e-bf47-d655ba842af2
keywords:
- propiedad currentPosition Reproductor de Windows Media
- Propiedad currentPosition Reproductor de Windows Media interfaz , IWMPControls
- Interfaz IWMPControls Reproductor de Windows Media , propiedad currentPosition
topic_type:
- apiref
api_name:
- IWMPControls.currentPosition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8eca861240256899fa19513fc1fb64cd540d47acb213f718674ebbda2d5f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053673"
---
# <a name="iwmpcontrolscurrentposition-property"></a>Propiedad IWMPControls::currentPosition

La **propiedad currentPosition** obtiene o establece la posición actual en el elemento multimedia en segundos desde el principio.

## <a name="syntax"></a>Syntax


```CSharp
public System.Double currentPosition {get; set;}
```


```VB

Public Property currentPosition As System.Double
```





## <a name="property-value"></a>Valor de propiedad

**System.Double que** es la posición actual.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa currentPosition** para buscar una posición proporcionada por el usuario. En respuesta a un clic de botón, **currentPosition** se establece en el valor especificado en un cuadro de texto denominado newPosition. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
private void setPosition_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text);
}
```


```VB

Public Sub setPosition_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setPosition.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Set the current position of the media item to the position entered by the user.
    player.Ctlcontrols.currentPosition = Convert.ToDouble(newPosition.Text)

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPControls (VB y C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentPositionString (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-currentpositionstring--vb-and-c.md)
</dt> </dl>

 

 





