---
title: Método getMarkerTime de IWMPMedia
description: El método getMarkerTime devuelve la hora del marcador en el índice especificado.
ms.assetid: 1c617e3a-0978-479c-a636-b655082232c1
keywords:
- Método getMarkerTime Reproductor de Windows Media
- Método getMarkerTime Reproductor de Windows Media , interfaz IWMPMedia
- Interfaz IWMPMedia Reproductor de Windows Media método , getMarkerTime
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293ad08137df1b87f47f614781d92be2b7c310fa7282cc234b38e1f3e0e63586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115702"
---
# <a name="iwmpmediagetmarkertime-method"></a>IWMPMedia::getMarkerTime (método)

El **método getMarkerTime** devuelve la hora del marcador en el índice especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Double getMarkerTime(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerTime( _
  ByVal MarkerNum As System.Int32 _
) As System.Double
Implements IWMPMedia.getMarkerTime
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*MarkerNum* \[ En\]
</dt> <dd>

**System.Int32 que** es el índice de marcador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.Double que** es la hora del marcador.

## <a name="remarks"></a>Comentarios

Este método devuelve **NULL** si el marcador especificado no existe.

Algunos elementos multimedia no contienen marcadores. Use **markerCount** para averiguar cuántos marcadores hay en el elemento multimedia actual.

Los números de índice de marcador comienzan en 1.

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se **usa getMarkerTime** para rellenar un cuadro de texto de varias líneas con la ubicación de cada marcador. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker times.
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker information in the array.
        markers[i] = "Marker number " + i + " occurs at ";
        markers[i] += player.currentMedia.getMarkerTime(i).ToString();
        markers[i] += " second(s).";
    }

    // Display the marker times in the text box.
    markerTimes.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker times.
Dim markers(mcount) As String

&#39; Verify that at least one marker exists in the current media.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker information in the array.
        markers(i) = (&quot;Marker number &quot; + i + &quot; occurs at &quot;)
        markers(i) += player.currentMedia.getMarkerTime(i).ToString()
        markers(i) += &quot; second(s).&quot;

    Next i

    &#39; Display the marker times in the text box.
    markerTimes.Lines = markers

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

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.markerCount (VB y C#)**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





