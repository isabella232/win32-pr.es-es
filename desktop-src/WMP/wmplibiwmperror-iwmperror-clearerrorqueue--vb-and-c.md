---
title: Método IWMPError clearErrorQueue
description: El método clearErrorQueue borra los errores de la cola de errores. | Método IWMPError clearErrorQueue
ms.assetid: a8e8e666-56e4-4e75-9ed5-2714d272ce7c
keywords:
- Método clearErrorQueue Reproductor de Windows Media
- Método clearErrorQueue Reproductor de Windows Media , interfaz IWMPError
- Interfaz IWMPError Reproductor de Windows Media , método clearErrorQueue
topic_type:
- apiref
api_name:
- IWMPError.clearErrorQueue
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f75b4e4d2a0e80a3f55a38744758497abc71f5899498fee95ee3b3db752631c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000455"
---
# <a name="iwmperrorclearerrorqueue-method"></a>IWMPError::clearErrorQueue (método)

El **método clearErrorQueue** borra los errores de la cola de errores.

## <a name="syntax"></a>Sintaxis


```CSharp
public void clearErrorQueue();
```


```VB

Public Sub clearErrorQueue()
Implements IWMPError.clearErrorQueue
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Use este método para borrar la cola de errores después de procesar una serie de errores.

Debe establecer **IWMPSettings.enableErrorDialogs** en **false** si decide mostrar mensajes de error personalizados.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa clearErrorQueue en** un controlador de eventos Error para vaciar la cola de errores después de mostrar todas las descripciones de errores. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
private void player_ErrorEvent_clearErrorQueue(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Loop through the list of errors.
    for (int i = 0; i < max; i++)
    {
        // Get the description for this error.
        string errDesc = player.Error.get_Item(i).errorDescription;

        // Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc);
    }

    // Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue();
}
```


```VB

Public Sub player_ErrorEvent_clearErrorQueue(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Loop through the list of errors.
    For i As Integer = 0 To (max - 1)

        &#39; Get the description for this error.
        Dim errDesc As String = player.Error.Item(i).errorDescription

        &#39; Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc)

    Next i

    &#39; Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue()

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

[**Interfaz IWMPError (VB y C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.enableErrorDialogs (VB y C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





