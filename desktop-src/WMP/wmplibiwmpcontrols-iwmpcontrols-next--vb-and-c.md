---
title: Método next de IWMPControls
description: El método siguiente establece el siguiente elemento de la lista de reproducción como el elemento actual.
ms.assetid: 3f82ef25-a1e0-4845-b0ed-dd6463719577
keywords:
- siguiente método Reproductor de Windows Media
- Next method Reproductor de Windows Media , IWMPControls (interfaz)
- Interfaz IWMPControls Reproductor de Windows Media , método next
topic_type:
- apiref
api_name:
- IWMPControls.next
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7b2fcb4a05078f1eefe90c266d636ec80cff219226246c622ce6040824c45d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031285"
---
# <a name="iwmpcontrolsnext-method"></a>IWMPControls::next (método)

El **método siguiente** establece el siguiente elemento de la lista de reproducción como el elemento actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public void next();
```


```VB

Public Sub next()
Implements IWMPControls.next
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si la lista de reproducción  está en la última entrada cuando se invoca la siguiente, la primera entrada de la lista de reproducción se convertirá en la actual.

En el caso de las listas de reproducción del lado servidor, este método omite el siguiente elemento de la lista de reproducción del lado servidor, no la lista de reproducción del cliente.

Al reproducir un DVD, este método omite el siguiente capítulo lógico de la secuencia de reproducción, que puede no ser el siguiente capítulo de la lista de reproducción. Al reproducir imágenes fijas de DVD, este método omite la siguiente imagen.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa next** para desplazarse al siguiente elemento de la lista de reproducción actual en respuesta al evento Click de un botón. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
private void nextButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("next"))
    {
        controls.next();
    }
}
```


```VB

Public Sub nextButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles nextButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;next&quot;)) Then

        controls.next()

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

[**IWMPControls.previous (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> <dt>

[**IWMPControls.stop (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





