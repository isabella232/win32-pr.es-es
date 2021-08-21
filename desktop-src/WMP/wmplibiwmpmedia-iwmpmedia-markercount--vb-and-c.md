---
title: Propiedad IWMPMedia markerCount
description: La propiedad markerCount obtiene el número de marcadores del elemento multimedia.
ms.assetid: d1ccaa9b-98fb-4c53-8064-ee4bf718d18a
keywords:
- propiedad markerCount Reproductor de Windows Media
- Propiedad markerCount Reproductor de Windows Media , interfaz IWMPMedia
- Interfaz IWMPMedia Reproductor de Windows Media , propiedad markerCount
topic_type:
- apiref
api_name:
- IWMPMedia.markerCount
- IWMPMedia.get_markerCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8afbc402858452c987bb6f2dcce0e1ad0428b8c67b81d2369de2a8cdbc6a7dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053633"
---
# <a name="iwmpmediamarkercount-property"></a>Propiedad IWMPMedia::markerCount

La **propiedad markerCount** obtiene el número de marcadores del elemento multimedia.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 markerCount {get;}
```


```VB

Public ReadOnly Property markerCount As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el recuento de marcadores.

## <a name="remarks"></a>Comentarios

Esta propiedad devuelve cero si un archivo no tiene marcadores o si el elemento multimedia no es el mismo que el especificado en AxWindowsMediaPlayer.currentMedia.

Los números de marcador comienzan en 1.

Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa markerCount** para recuperar el número de marcadores del elemento multimedia actual. A continuación, ese valor se usa como límite superior para una estructura de bucle, que recorre en iteración la lista de marcadores para recuperar cada nombre de marcador y mostrarlo en un cuadro de texto de varias líneas. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of markers.
string[] markerNames = new string[mcount];

// Verify that at least one marker exists in the current media item.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markerNames[i]= player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerList.Lines = markerNames;            
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of markers.
Dim markerNames(mcount) As String

&#39; Verify that at least one marker exists in the current media item.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker name in the array.
        markerNames(i) = player.currentMedia.getMarkerName(i)

    Next i

    &#39; Display the marker names in the text box.
    markerList.Lines = markerNames

End If
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AxWindowsMediaPlayer.currentMedia (VB y C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





