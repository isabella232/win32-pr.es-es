---
title: IWMPMedia. isIdentical (VB y C)
description: La propiedad isIdentical (el \_ método get isIdentical de C \) obtiene un valor que indica si el elemento multimedia especificado es igual que el actual.
ms.assetid: 1406a0ff-2dc8-4cde-8b71-4a39b8608fb1
keywords:
- IWMPMedia. isIdentical (VB y C) Windows Media Player
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
ms.openlocfilehash: b3a488ad300362c1f8dccfd0fa6f6c7e4dee7676
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690771"
---
# <a name="iwmpmediaisidentical-vb-and-c"></a>IWMPMedia. isIdentical (VB y C#)

La propiedad **isIdentical** (el método **Get \_ isIdentical** en C#) obtiene un valor que indica si el elemento multimedia especificado es igual que el actual.


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

Una interfaz **WMPLib. IWMPMedia** para el elemento multimedia que se va a comparar con el elemento multimedia actual.

## <a name="property-value"></a>Valor de propiedad

Valor **System. Boolean** que indica si los dos elementos multimedia son idénticos.

## <a name="remarks"></a>Observaciones

**IWMPMedia. isIdentical** es una propiedad de Visual Basic que toma un parámetro. En C#, se hace referencia a él como el método **IWMPMedia. Get \_ isIdentical** .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa la propiedad **isIdentical** (el método **Get \_ isIdentical** en C#) para comprobar si un elemento multimedia denominado newMedia es igual que el elemento multimedia actual. Si no son iguales, se reproduce el nuevo elemento multimedia. De lo contrario, el medio actual sigue reproduciéndose sin interrupciones. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


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
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





