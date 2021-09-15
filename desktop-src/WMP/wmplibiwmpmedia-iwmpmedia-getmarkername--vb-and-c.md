---
title: IWMPMedia getMarkerName (método)
description: El método getMarkerName devuelve el nombre del marcador en el índice especificado.
ms.assetid: 77f893cf-1669-41e3-9f62-8a1081e37add
keywords:
- Método getMarkerName Reproductor de Windows Media
- Método getMarkerName Reproductor de Windows Media , interfaz IWMPMedia
- Interfaz IWMPMedia Reproductor de Windows Media método , getMarkerName
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ba6a7bb640a397cce9c7dfd22b5f9b6203c47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258700"
---
# <a name="iwmpmediagetmarkername-method"></a>IWMPMedia::getMarkerName (método)

El **método getMarkerName** devuelve el nombre del marcador en el índice especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String getMarkerName(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerName( _
  ByVal MarkerNum As System.Int32 _
) As System.String
Implements IWMPMedia.getMarkerName
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*MarkerNum* \[ En\]
</dt> <dd>

**System.Int32 que** es el índice de marcador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.String que** es el nombre del marcador.

## <a name="remarks"></a>Observaciones

Este método devuelve **NULL** si el marcador especificado no existe.

Algunos elementos multimedia no contienen marcadores. Use **markerCount** para averiguar cuántos marcadores hay en el elemento multimedia actual.

Los números de índice de marcador comienzan en 1.

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se **usa getMarkerName** para rellenar un cuadro de texto de varias líneas con los nombres de los marcadores del elemento multimedia actual. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker names
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markers[i] = player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerNames.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mCount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker names
Dim markers(mCount) As String

&#39; Verify that at least one marker exists in the current media.
If (mCount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mCount

        &#39; Store the marker name in the array.
        markers(i) = player.currentMedia.getMarkerName(i)

    Next i

End If

&#39; Display the marker names in the text box.
markerNames.Lines = markers
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.markerCount (VB y C#)**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





