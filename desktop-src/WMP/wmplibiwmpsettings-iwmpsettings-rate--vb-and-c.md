---
title: IWMPSettings Rate (propiedad)
description: La propiedad Rate obtiene o establece la velocidad de reproducción actual del vídeo.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- Media Player de la propiedad Rate de Windows
- propiedad Rate Media Player de Windows, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad Rate
topic_type:
- apiref
api_name:
- IWMPSettings.rate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f502bebdbd22523858637f8abccbe203db104cbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718697"
---
# <a name="iwmpsettingsrate-property"></a>IWMPSettings:: Rate (propiedad)

La propiedad **Rate** obtiene o establece la velocidad de reproducción actual del vídeo.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a>Valor de propiedad

**System. Double** que es la velocidad de reproducción, con un valor predeterminado de 1,0.

## <a name="remarks"></a>Observaciones

El valor recuperado por esta propiedad actúa como un valor de multiplicador que permite reproducir un elemento multimedia a una velocidad mayor o menor. El valor predeterminado de 1,0 indica la velocidad de creación.

Tenga en cuenta que una pista de audio es difícil de comprender a las tarifas inferiores a 0,5 o superior a 1,5. Una velocidad de reproducción de 2 indica dos veces la velocidad de reproducción normal.

Windows Media Player intentará usar los siguientes cuatro modos de reproducción diferentes:

-   Reproducción fluida de vídeo con el paso de audio mantenido
-   Reproducción fluida de vídeo con el tono de audio no mantenido
-   Reproducción fluida de vídeo sin audio
-   Reproducción de vídeo de fotogramas clave sin audio

El modo elegido por Windows Media Player depende de numerosos factores, como el tipo de archivo y la ubicación, el sistema operativo, la red y el servidor.

También se aplican otras consideraciones, dependiendo del formato de medios digitales utilizado para crear el contenido:

-   **Windows Media Video (WMV) y ASF.** Los valores óptimos para la propiedad **Rate** son de 1 a 10, o de 1 a 10 para la reproducción inversa. Los valores de 0,5 a 1,0 o de-0,5 a-1,0 también pueden funcionar bien en los casos en los que se pueda mantener el tono de audio, como al reproducir archivos ubicados en el equipo local. Se permiten los valores con una magnitud absoluta mayor que 10, pero no son muy significativos.
-   **Otros formatos de vídeo.** La propiedad **Rate** puede oscilar entre 0 y 9. No se permiten valores negativos. Los valores menores que 1 representan un movimiento lento. Los valores por encima de 9 están permitidos, pero no son muy significativos.

El método **IWMPControls. fastForward** cambia el valor de **Rate** a 5,0, mientras que el método **IWMPControls. fastReverse** cambia el valor de **Rate** a 5,0.

No se puede modificar la velocidad de reproducción de algunos formatos de medios digitales. Use la propiedad **IWMPSettings. isavailable** (en C# el método **IWMPSettings. Get \_ isavailable** ) para detectar si esta propiedad se puede especificar para un elemento multimedia determinado.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa un control numérico de flechas que permite al usuario cambiar la velocidad de reproducción del medio actual. Cuando el usuario hace clic en las flechas arriba o abajo del control, la propiedad **Rate** se establece en el nuevo valor. El intervalo posible de valores del control es 0,5 (velocidad media) a 2,0 (velocidad doble). El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void playbackRate_Click(object sender, System.EventArgs e)
{
    // Get the new value of the control, and cast it from decimal to double.
    double newRate = (double)((System.Windows.Forms.NumericUpDown)sender).Value;

    // Test whether playback rate can be set. 
    if( player.settings.get_isAvailable("Rate") )
    {
        // Set the playback rate to the new value.
        player.settings.rate = newRate;
    }
}
```


```VB

Public Sub playbackRate_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playbackRate.Click

    &#39;  Get the new value of the control as a double.
    Dim nUpDown As System.Windows.Forms.NumericUpDown = sender
    Dim newRate As Double = nUpDown.Value

    &#39;  Test whether playback rate can be set. 
    If (player.settings.isAvailable(&quot;Rate&quot;)) Then

        &#39;  Set the playback rate to the new value.
        player.settings.rate = newRate

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

[**IWMPControls. fastForward (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls. fastReverse (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. isAvailable (VB y C#)**](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. MUTE (VB y C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





