---
title: Propiedad rate de IWMPSettings
description: La propiedad rate obtiene o establece la velocidad de reproducción actual del vídeo.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- propiedad rate Reproductor de Windows Media
- rate property Reproductor de Windows Media , IWMPSettings (interfaz)
- Interfaz IWMPSettings Reproductor de Windows Media , propiedad rate
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
ms.openlocfilehash: cc053861b9061df676455e10b011cd0ffe0fe9f06052b129ec163e00d4c8d71f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999705"
---
# <a name="iwmpsettingsrate-property"></a>Propiedad IWMPSettings::rate

La **propiedad rate** obtiene o establece la velocidad de reproducción actual del vídeo.

## <a name="syntax"></a>Syntax


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a>Valor de propiedad

**System.Double que** es la velocidad de reproducción, con un valor predeterminado de 1,0.

## <a name="remarks"></a>Comentarios

El valor recuperado por esta propiedad actúa como un valor multiplicador que permite reproducir un elemento multimedia a una velocidad más rápida o más lenta. El valor predeterminado de 1,0 indica la velocidad de creación.

Tenga en cuenta que una pista de audio resulta difícil de entender a velocidades inferiores a 0,5 o superiores a 1,5. Una velocidad de reproducción de 2 indica el doble de la velocidad de reproducción normal.

Reproductor de Windows Media intentará usar el más eficaz de los cuatro modos de reproducción diferentes siguientes

-   Reproducción de vídeo fluida con el tono de audio mantenido
-   Reproducción de vídeo sin problemas con el tono de audio no mantenido
-   Reproducción de vídeo sin problemas sin audio
-   Reproducción de vídeo fotograma clave sin audio

El modo elegido por Reproductor de Windows Media depende de numerosos factores, como el tipo de archivo y la ubicación, el sistema operativo, la red y el servidor.

También se aplican otras consideraciones, en función del formato multimedia digital usado para crear el contenido:

-   **Windows Vídeo multimedia (WMV) y ASF.** Los valores óptimos para **la propiedad rate** son de 1 a 10, o de 1 a 10 para el juego inverso. Los valores de 0,5 a 1,0 o de -0,5 a -1,0 también pueden funcionar bien en los casos en los que se puede mantener el tono de audio, como cuando se reproducen archivos ubicados en el equipo local. Se permiten valores con una magnitud absoluta mayor que 10, pero no son muy significativos.
-   **Otros formatos de vídeo.** La **propiedad rate** puede oscilar entre 0 y 9. No se permiten valores negativos. Los valores menores que 1 representan el movimiento lento. Se permiten valores por encima de 9, pero no son muy significativos.

El **método IWMPControls.fastForward** cambia el valor de **rate** a 5,0, mientras que el método **IWMPControls.fastReverse** cambia el valor de **rate** a 5,0.

No se puede modificar la velocidad de reproducción de algunos formatos multimedia digitales. Use la **propiedad IWMPSettings.isAvailable** (en C# el método **IWMPSettings.get \_ isAvailable)** para detectar si esta propiedad se puede especificar para un elemento multimedia determinado.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa un control numérico updown que permite al usuario cambiar la velocidad de reproducción del medio actual. Cuando el usuario hace clic en las flechas arriba o abajo del control, la propiedad **rate** se establece en el nuevo valor. El intervalo posible de valores del control es de 0,5 (media velocidad) a 2,0 (doble velocidad). El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


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
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMPControls.fastForward (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[**IWMPControls.fastReverse (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.isAvailable (VB y C#)**](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.mute (VB y C#)**](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





