---
title: IWMPNetwork lostPackets, propiedad
description: La propiedad lostPackets obtiene el número de paquetes perdidos.
ms.assetid: 611218d3-c4d3-4d4e-835c-1e7a956b2718
keywords:
- lostPackets, propiedad Reproductor de Windows Media
- Interfaz de la propiedad lostPackets Reproductor de Windows Media , IWMPNetwork
- Interfaz IWMPNetwork Reproductor de Windows Media , propiedad lostPackets
topic_type:
- apiref
api_name:
- IWMPNetwork.lostPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a60c85920d647f99ed8ba8478da51183c3ba63efa733c0bc627c16b040b70965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745916"
---
# <a name="iwmpnetworklostpackets-property"></a>IWMPNetwork::lostPackets, propiedad

La **propiedad lostPackets** obtiene el número de paquetes perdidos.

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 lostPackets {get; set;}
```


```VB

Public ReadOnly Property lostPackets As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el número de paquetes perdidos.

## <a name="remarks"></a>Comentarios

Esta propiedad incluye solo paquetes multimedia de streaming y devolverá cero cuando se use el protocolo HTTP, que no tiene pérdidas.

Los paquetes se pueden perder por diversos motivos, como el tipo y la calidad de la conexión de red.

Cada vez que se detiene y reinicia la reproducción, esta propiedad se restablece en cero. El valor no se restablece si la reproducción está en pausa. Esta propiedad obtiene información válida solo durante el tiempo de ejecución cuando se establece la dirección URL para la reproducción mediante la **propiedad AxWindowsMediaPlayer.URL.**

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se **usa lostPackets para** mostrar el número total de paquetes perdidos durante la reproducción. La información se muestra en una etiqueta cuando el usuario hace clic en un botón. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
private void showLostPackets_Click(object sender, System.EventArgs e)
{
    lostPacketsLabel.Text = ("Packets lost: " + player.network.lostPackets.ToString());
}
```


```VB

Public Sub showLostPackets_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showLostPackets.Click

    lostPacketsLabel.Text = (&quot;Packets lost: &quot; + player.network.lostPackets.ToString())

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

[**Interfaz IWMPNetwork (VB y C#)**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB y C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> </dl>

 

 





