---
title: Propiedad bufferingTime de IWMPNetwork
description: La propiedad bufferingTime obtiene o establece la cantidad de tiempo en milisegundos asignados para almacenar en búfer los datos entrantes antes de que empiece la reproducción.
ms.assetid: b5936b21-a17b-4801-a5fc-c6d6521e05aa
keywords:
- propiedades de bufferingTime Media Player de Windows
- propiedad bufferingTime de Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad bufferingTime
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8594d53797b028dd74a8ef11cb8f2fa64b3654cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698573"
---
# <a name="iwmpnetworkbufferingtime-property"></a>IWMPNetwork:: bufferingTime (propiedad)

La propiedad **bufferingTime** obtiene o establece la cantidad de tiempo en milisegundos asignados para almacenar en búfer los datos entrantes antes de que empiece la reproducción.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 bufferingTime {get; set;}
```


```VB

Public Property bufferingTime As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System. Int32** que es el tiempo de almacenamiento en milisegundos, que oscila entre cero y 60.000 con un valor predeterminado de 5.000.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se usa **bufferingTime** para especificar el número de segundos asignados para almacenar en búfer los datos entrantes. Un cuadro de texto permite al usuario especificar un nuevo valor para **bufferingTime**, y la propiedad se actualiza en respuesta al evento click de un botón. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void setBufTime_Click(object sender, System.EventArgs e)
{
    // Retrieve input from the user and convert it to an integer.
    int newTime = System.Convert.ToInt32(bufText.Text);

    // Test whether the integer is within the valid range. 
    if (newTime >= 0 & newTime <= 60) 
    {
        // Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000);
    }
    else
    {
        System.Windows.Forms.MessageBox.Show("Buffering time must be between 0 and 60.");
    }
}
```


```VB

Public Sub setBufTime_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setBufTime.Click

    &#39; Retrieve input from the user and convert it to an integer.
    Dim newTime As Integer = System.Convert.ToInt32(bufText.Text)

    &#39; Test whether the integer is within the valid range. 
    If (newTime >= 0 And newTime <= 60) Then

        &#39; Set the new bufferingTime in miliseconds.
        player.network.bufferingTime = (newTime * 1000)

    Else

        System.Windows.Forms.MessageBox.Show(&quot;Buffering time must be between 0 and 60.&quot;)

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

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





