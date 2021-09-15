---
title: IWMPError errorCount, propiedad
description: La propiedad errorCount obtiene el número de errores de la cola de errores.
ms.assetid: a30750c8-2025-4087-bd2b-f313ccbde38c
keywords:
- errorCount, propiedad Reproductor de Windows Media
- ErrorCount, propiedad Reproductor de Windows Media interfaz , IWMPError
- Interfaz IWMPError Reproductor de Windows Media , propiedad errorCount
topic_type:
- apiref
api_name:
- IWMPError.errorCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62c16f07260847c91f1c9f18885587444a4ceb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465714"
---
# <a name="iwmperrorerrorcount-property"></a>IWMPError::errorCount, propiedad

La **propiedad errorCount** obtiene el número de errores de la cola de errores.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 errorCount {get; set;}
```


```VB

Public ReadOnly Property errorCount As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32** que es el número de errores.

## <a name="remarks"></a>Observaciones

Si decide mostrar mensajes de error **personalizados, debe establecer IWMPSettings.enableErrorDialogs** en **false.**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa errorCount en** un controlador de eventos Error para alertar al usuario sobre el error más reciente en la cola de errores. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
private void player_ErrorEvent_errorCount(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Get the description of the last error. Error items start at zero,
    // so the item index will always be one less than the error count.
    string errDesc = player.Error.get_Item(max-1).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorCount(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Get the description of the last error. Error items start at zero,
    &#39; so the item index will always be one less than the error count.
    Dim errDesc As String = player.Error.Item(max - 1).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPError (VB y C#)**](iwmperror--vb-and-c.md)
</dt> <dt>

[**IWMPSettings.enableErrorDialogs (VB y C#)**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





