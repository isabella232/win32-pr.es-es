---
title: Método fastReverse de IWMPControls
description: El método fastReverse inicia la reproducción rápida del elemento multimedia en la dirección inversa.
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- Método fastReverse Reproductor de Windows Media
- Método fastReverse Reproductor de Windows Media , interfaz IWMPControls
- Interfaz IWMPControls Reproductor de Windows Media , método fastReverse
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88bbc1442ca223765b498560d078879c9a7033011117b7f663d4d40ff26bdd93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761085"
---
# <a name="iwmpcontrolsfastreverse-method"></a>IWMPControls::fastReverse (método)

El **método fastReverse** inicia la reproducción rápida del elemento multimedia en la dirección inversa.

## <a name="syntax"></a>Sintaxis


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El **método fastReverse** examina el clip en orden inverso a una velocidad cinco veces mayor que la velocidad normal, mostrando solo los fotogramas clave si es un archivo de vídeo. Llamar **a fastReverse** equivale a especificar -5,0 para la velocidad estableciendo la **propiedad IWMPSettings.rate.** Si posteriormente se cambia la velocidad, o si se llama a **IWMPControls.play** o **IWMPControls.stop,** Reproductor de Windows Media dejará de invertirse rápidamente.

Si el elemento forma parte de una lista de reproducción, **fastReverse** se detiene al principio de la pista actual. Por ejemplo, si la pista 3 está en **fastReverse**, cuando se alcanza el principio de la pista 3, Reproductor de Windows Media no irá a la pista 2. El recuento de reproducción no se incrementa al llamar **a fastReverse**.

Si llama a **IWMPControls.fastForward** mientras se ejecuta **fastReverse,** **fastReverse** se detendrán y **comenzará IWMPControls.fastForward.**

Este método no funciona para difusión en vivo y determinados tipos de medios digitales. Para determinar si puede usar la inversa rápida en un clip, pase el valor **System.String** "FastReverse" a la propiedad **IWMPControls.isAvailable** (el método **IWMPControls.get \_ isAvailable** en C#).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa fastReverse** para invertir el elemento multimedia actual en respuesta al evento Click de un botón. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

    End If

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPControls (VB y C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.fastForward (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls.isAvailable (VB y C#)**](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls.stop (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.rate (VB y C#)**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





