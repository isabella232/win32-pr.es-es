---
title: IWMPError. Item (VB y C)
description: La propiedad Item (el \_ método get item en C \) obtiene una interfaz IWMPErrorItem en el índice especificado de la cola de errores.
ms.assetid: acfaaaa5-eb13-4ba0-8417-4229adc62c5d
keywords:
- IWMPError. Item (VB y C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPError.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9217ec772512171c828dd0dad06ec8fe3704dba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690497"
---
# <a name="iwmperroritem-vb-and-c"></a>IWMPError. Item (VB y C#)

La propiedad **Item** (el método **Get \_ Item** en C#) obtiene una interfaz **IWMPErrorItem** en el índice especificado de la cola de errores.


```
[Visual Basic]
ReadOnly Property Item(
  dwIndex As System.Integer
) As IWMPErrorItem
```




```
[C#]
IWMPErrorItem get_Item (
  System.Int32 dwIndex
);
```



## <a name="parameters"></a>Parámetros

*dwIndex*

**System. Int32** que es el índice de base cero de una interfaz **IWMPErrorItem** en la cola de errores.

## <a name="property-value"></a>Valor de propiedad

Una interfaz **WMPLib. IWMPErrorItem** .

## <a name="remarks"></a>Observaciones

Windows Media Player puede generar una serie de errores en respuesta a una condición de error. Esta propiedad obtiene un error específico en la cola mediante un número de índice. Los números de índice de la cola de errores comienzan por cero.

Debe establecer **IWMPSettings. enableErrorDialogs** en **false** si elige mostrar mensajes de error personalizados.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa la propiedad **Item** (el método **Get \_ Item** en C#) en un controlador de eventos de error para recuperar y Mostrar información sobre el error más reciente en la cola de errores. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
private void player_ErrorEvent_get_Item(object sender, System.EventArgs e)
{
    // Store the index of the most recent error.
    int max = (player.Error.errorCount - 1);

    // Get an interface for the most recent error item. Cast it to
    // a WMPLib.IWMPErrorItem2 interface to get all of the available functionality.
    WMPLib.IWMPErrorItem2 errItem = (WMPLib.IWMPErrorItem2)player.Error.get_Item(max);

    // Use the interface to access and store the error info.
    int errNum = errItem.errorCode;
    string errDesc = errItem.errorDescription;

    // Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + ":  " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_get_Item(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the index of the most recent error.
    Dim max As Integer = (player.Error.errorCount - 1)

    &#39; Get an interface for the most recent error item. 
    Dim errItem As WMPLib.IWMPErrorItem2 = player.Error.Item(max)

    &#39; Use the interface to access and store the error info.
    Dim errNum As Integer = errItem.errorCode
    Dim errDesc As String = errItem.errorDescription

    &#39; Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + &quot;:  &quot; + errDesc)

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

[**Interfaz IWMPError (VB y C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPErrorItem (VB y C#)**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. enableErrorDialogs (VB y C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





