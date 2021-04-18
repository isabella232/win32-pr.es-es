---
title: Propiedad currentMarker de IWMPControls
description: La propiedad currentMarker obtiene o establece el número de marcador actual.
ms.assetid: faf8c32a-66de-47ce-aa3d-6699d9f9bdda
keywords:
- propiedades de currentMarker Media Player de Windows
- propiedad currentMarker de Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, propiedad currentMarker
topic_type:
- apiref
api_name:
- IWMPControls.currentMarker
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfbcea42594b15b8da08248d38b5d8f72a1de29d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690890"
---
# <a name="iwmpcontrolscurrentmarker-property"></a>IWMPControls:: currentMarker (propiedad)

La propiedad **currentMarker** obtiene o establece el número de marcador actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 currentMarker {get; set;}
```


```VB

Public Property currentMarker As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System. Int32** que es el número del marcador.

## <a name="remarks"></a>Observaciones

La configuración de **currentMarker** hace que la reproducción se inicie desde el marcador especificado. Antes de intentar establecer **currentMarker**, determine si un archivo tiene marcadores y cuántos tiene con **IWMPMedia. markerCount**. Si un archivo no tiene marcadores, si se establece **currentMarker** en cualquier cosa pero cero, se produce un error. Establecer **currentMarker** en un número mayor que **markerCount** también produce un error.

La propiedad **currentMarker** siempre devuelve el marcador actual o el último, lo que significa que la posición del archivo real puede estar en el marcador actual o antes del marcador siguiente. Los marcadores se numeran a partir de 1, por lo que si un archivo tiene marcadores, puede establecer **currentMarker** en cero para cambiar la posición del archivo a cero.

Hasta que se establezca el elemento multimedia actual (mediante **AxWindowsMediaPlayer. URL** o **AxWindowsMediaPlayer. CurrentMedia**), **currentMarker** devuelve cero.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **currentMarker** para iniciar la reproducción de vídeo desde el marcador que corresponde a la propiedad SelectedIndex de un cuadro de lista que se ha rellenado con identificadores de marcador. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
// Fill the list box with the marker identifiers of the current media item.
markers.Items.Add("Begining");
markers.Items.Add("Sunrise");
markers.Items.Add("Car chase");
markers.Items.Add("Happy ending");

// Set the currentMarker to the marker selected from the list box.
private void markers_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedMarker = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    player.Ctlcontrols.currentMarker = selectedMarker;
}
```


```VB

' Fill the list box with the marker identifiers of the current media item.
markers.Items.Add(&quot;Begining&quot;)
markers.Items.Add(&quot;Sunrise&quot;)
markers.Items.Add(&quot;Car chase&quot;)
markers.Items.Add(&quot;Happy ending&quot;)

&#39; Set the currentMarker to the marker selected from the list box.
Public Sub markers_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles markers.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedMarker As Integer = lb.SelectedIndex

    player.Ctlcontrols.currentMarker = selectedMarker

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

[**AxWindowsMediaPlayer. currentMedia (VB y C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB y C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPControls (VB y C#)**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. markerCount (VB y C#)**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





