---
title: IWMPMedia.isIdentical (VB y C )
description: La propiedad isIdentical (el método get isIdentical en C\) obtiene un valor que indica si el elemento multimedia especificado es el mismo que \_ el actual.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- IWMPMedia.isIdentical (VB y C ) Reproductor de Windows Media
topic_type:
- apiref
api_name:
- IWMPMedia.isIdentical (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e8de133003bdddcf0438e5a13dc3fa74227ede7bf42350e2b7c3c96f2c197e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003585"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a>IWMPMedia.isIdentical (VB y C#)

La **propiedad isIdentical** (el método **get \_ isIdentical** en C#) obtiene un valor que indica si el elemento multimedia especificado es el mismo que el actual.


```
[Visual Basic]
ReadOnly Property isIdentical(
  pIWMPMedia As IWMPMedia
) As System.Boolean
```




```
[C#]
System.Boolean get_isIdentical (
  IWMPMedia pIWMPMedia
);
```



## <a name="parameters"></a>Parámetros

*pIWMPMedia*

Interfaz **WMPLib.IWMPMedia** al elemento multimedia que se va a comparar con el elemento multimedia actual.

## <a name="property-value"></a>Valor de propiedad

Valor **System.Boolean** que indica si los dos elementos multimedia son idénticos.

## <a name="remarks"></a>Comentarios

**IWMPMedia.isIdentical es** una propiedad de Visual Basic que toma un parámetro . En C# se conoce como el **método IWMPMedia.get \_ isIdentical.**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa la propiedad **isIdentical** (el método **get \_ isIdentical** en C#) para comprobar si un elemento multimedia denominado newMedia es el mismo que el elemento multimedia actual. Si no son iguales, se reproduce el nuevo elemento multimedia. De lo contrario, los medios actuales siguen reprobando sin interrupciones. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
if (newMedia.get_isIdentical(player.currentMedia) != true)
{
    // Change the current media to the new media item.
    player.currentMedia = newMedia;

    // Play the new media item.
    player.Ctlcontrols.play();
}
```


```VB

If (newMedia.isIdentical(player.currentMedia) <> True) Then

    &#39; Change the current media to the new media item.
    player.currentMedia = newMedia

    &#39; Play the new media item.
    player.Ctlcontrols.play()

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

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





