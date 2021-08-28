---
title: IWMPControls.isAvailable (VB y C )
description: La propiedad isAvailable (el método get isAvailable en C\) obtiene un valor que indica si un tipo especificado de información está disponible o si se puede realizar una \_ acción especificada.
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- IWMPControls.isAvailable (VB y C ) Reproductor de Windows Media
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
ms.openlocfilehash: d73562fb4f96731216c30ada33db8e13d1468b31fb6fcefe7eedef6dd7892348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054853"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a>IWMPControls.isAvailable (VB y C#)

La **propiedad isAvailable** (el método **get \_ isAvailable** en C#) obtiene un valor que indica si un tipo especificado de información está disponible o si se puede realizar una acción especificada.


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

System.String que es uno de los siguientes valores.



| Valor           | Descripción                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Currentitem     | Detecta si el usuario puede establecer la **propiedad IWMPControls.currentItem.**                                                                                     |
| currentMarker   | Detecta si el usuario puede buscar un marcador específico.                                                                                                         |
| currentPosition | Detecta si el usuario puede buscar una posición específica en el archivo. Algunos archivos no admiten búsquedas.                                                        |
| fastForward     | Detecta si el archivo admite el reenvío rápido y si se puede invocar esa funcionalidad. Muchos tipos de archivo (y secuencias en vivo) no admiten fastForward. |
| fastReverse     | Detecta si el archivo admite fastReverse y si se puede invocar esa funcionalidad. Muchos tipos de archivo (y secuencias en vivo) no admiten fastReverse.     |
| Siguiente            | Detecta si el usuario puede buscar en la siguiente entrada de una lista de reproducción.                                                                                              |
| pause           | Detecta si el **método IWMPControls.pause** está disponible.                                                                                                 |
| Jugar            | Detecta si el **método IWMPControls.play** está disponible.                                                                                                  |
| previous        | Detecta si el usuario puede buscar en la entrada anterior de una lista de reproducción.                                                                                          |
| paso            | Detecta si el **método IWMPControls2.step** está disponible durante la reproducción.                                                                                 |
| stop            | Detecta si el **método IWMPControls.stop** está disponible.                                                                                                  |



 

## <a name="property-value"></a>Valor de propiedad

**System.Boolean**

**System.Boolean** que indica si un tipo especificado de información está disponible o si se puede realizar una acción especificada.

## <a name="remarks"></a>Comentarios

**IWMPControls.isAvailable es** una propiedad de Visual Basic que toma un parámetro . En C# se conoce como el **método IWMPControls.get \_ isAvailable.**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa la **propiedad isAvailable** (el método **get \_ isAvailable** en C#) para comprobar que el elemento multimedia actual admite la **propiedad currentPosition.** El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


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
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPControls (VB y C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPControls.currentItem (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[**IWMPControls.pause (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**IWMPControls.stop (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[**IWMPControls2.step (VB y C#)**](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





