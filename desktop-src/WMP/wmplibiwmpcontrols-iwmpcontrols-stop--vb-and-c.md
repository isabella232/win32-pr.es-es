---
title: IWMPControls STOP (método)
description: El método Stop detiene la reproducción del elemento multimedia. | IWMPControls STOP (método)
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- detener el método Windows Media Player
- método STOP Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, método STOP
topic_type:
- apiref
api_name:
- IWMPControls.stop
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73271098340ea0cf0a645472b5ef6333ae0f4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690872"
---
# <a name="iwmpcontrolsstop-method"></a>IWMPControls:: STOP (método)

El método **Stop** detiene la reproducción del elemento multimedia.

## <a name="syntax"></a>Sintaxis


```CSharp
public void stop();
```


```VB

Public Sub stop()
Implements IWMPControls.stop
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método hace que Windows Media Player libere cualquier recurso del sistema que esté usando, como el dispositivo de audio. Sin embargo, el elemento multimedia actual no se libera.

Cuando se detiene Windows Media Player, la posición de reproducción actual en el elemento multimedia se restablece al principio del elemento. Después de llamar a **IWMPControls. Play** se iniciará la reproducción desde el principio del elemento multimedia. Para detener una operación de reproducción sin cambiar la posición actual, use el método **IWMPControls. PAUSE** .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **Stop** para detener el elemento multimedia actual en respuesta al evento click de un botón. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void stopButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("stop"))
    {
        controls.stop();
    }
}
```


```VB

Public Sub stopButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles stopButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;stop&quot;)) Then

        controls.stop()

    End If

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

[**IWMPControls. Next (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[**IWMPControls. PAUSE (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Previous (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





