---
title: IWMPControls. isAvailable (VB y C)
description: La propiedad isAvailable (el \_ método get isavailable en C \) obtiene un valor que indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- IWMPControls. isAvailable (VB y C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPControls.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d5d9ffcd6cad6eefb7cdff25fd2cf34b76ccc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690425"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a>IWMPControls. isAvailable (VB y C#)

La propiedad **isavailable** (el método **Get \_ isavailable** en C#) obtiene un valor que indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
bool get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a>Parámetros

*bstrItem*

System. String que es uno de los valores siguientes.



| Value           | Descripción                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| currentItem     | Detecta si el usuario puede establecer la propiedad **IWMPControls. CurrentItem** .                                                                                     |
| currentMarker   | Detecta si el usuario puede buscar un marcador específico.                                                                                                         |
| currentPosition | Detecta si el usuario puede buscar una posición específica en el archivo. Algunos archivos no admiten búsquedas.                                                        |
| fastForward     | Detecta si el archivo admite el reenvío rápido y si se puede invocar la funcionalidad. Muchos tipos de archivo (y secuencias en directo) no admiten fastForward. |
| fastReverse     | Detecta si el archivo admite fastReverse y si se puede invocar esa funcionalidad. Muchos tipos de archivo (y secuencias en directo) no admiten fastReverse.     |
| Siguiente            | Detecta si el usuario puede buscar la siguiente entrada en una lista de reproducción.                                                                                              |
| pause           | Detecta si el método **IWMPControls. PAUSE** está disponible.                                                                                                 |
| reproducción            | Detecta si el método **IWMPControls. Play** está disponible.                                                                                                  |
| previous        | Detecta si el usuario puede buscar la entrada anterior en una lista de reproducción.                                                                                          |
| paso            | Detecta si el método **IWMPControls2. Step** está disponible durante la reproducción.                                                                                 |
| stop            | Detecta si el método **IWMPControls. Stop** está disponible.                                                                                                  |



 

## <a name="property-value"></a>Valor de propiedad

**System.Boolean**

**System. Boolean** que indica si un tipo de información especificado está disponible o se puede realizar una acción especificada.

## <a name="remarks"></a>Observaciones

**IWMPControls. isavailable** es una propiedad de Visual Basic que toma un parámetro. En C#, se hace referencia a él como el método **IWMPControls. Get \_ isavailable** .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa la propiedad **isavailable** (el método **Get \_ isavailable** en C#) para comprobar que el elemento multimedia actual admite la propiedad **currentPosition** . El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
// If the currentPosition property is supported, seek to position 0.
if (player.Ctlcontrols.get_isAvailable("currentPosition"))
{
    player.Ctlcontrols.currentPosition = 0;
}
```


```VB

' If the currentPosition property is supported, seek to position 0.
If (player.Ctlcontrols.isAvailable(&quot;currentPosition&quot;)) Then

    player.Ctlcontrols.currentPosition = 0

End If
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

[**IWMPControls. currentItem (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**IWMPControls. PAUSE (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls. STOP (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPControls2. Step (VB y C#)**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





