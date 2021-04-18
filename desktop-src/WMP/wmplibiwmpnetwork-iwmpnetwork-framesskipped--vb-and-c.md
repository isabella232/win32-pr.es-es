---
title: Propiedad framesSkipped de IWMPNetwork
description: La propiedad framesSkipped obtiene el número total de fotogramas omitidos durante la reproducción.
ms.assetid: eedecfa9-0c82-4800-979e-ca85fb78c480
keywords:
- propiedades de framesSkipped Media Player de Windows
- propiedad framesSkipped de Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad framesSkipped
topic_type:
- apiref
api_name:
- IWMPNetwork.framesSkipped
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8409cec50089111184f96e4463f57cc9c4fbae07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670885"
---
# <a name="iwmpnetworkframesskipped-property"></a>IWMPNetwork:: framesSkipped (propiedad)

La propiedad **framesSkipped** obtiene el número total de fotogramas omitidos durante la reproducción.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 framesSkipped {get; set;}
```


```VB

Public ReadOnly Property framesSkipped As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System. Int32** que es el número de fotogramas omitidos.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se usa **framesSkipped** para mostrar el número total de fotogramas omitidos durante la reproducción. La información se muestra en una etiqueta cuando el usuario hace clic en un botón. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void showFramesSkipped_Click(object sender, System.EventArgs e)
{
    framesSkippedLabel.Text = ("Frames skipped: " + player.network.framesSkipped.ToString());
}
```


```VB

Public Sub showFramesSkipped_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showFramesSkipped.Click

    framesSkippedLabel.Text = (&quot;Frames skipped: &quot; + player.network.framesSkipped.ToString())

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

 

 





