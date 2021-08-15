---
title: Método IWMPMediaCollection getAttributeStringCollection
description: El método getAttributeStringCollection devuelve una interfaz IWMPStringCollection que representa el conjunto de todos los valores de un atributo especificado dentro de un tipo de medio.
ms.assetid: 5ac19c04-75db-4618-9c4e-b20e2f709024
keywords:
- Método getAttributeStringCollection Reproductor de Windows Media
- Método getAttributeStringCollection Reproductor de Windows Media , interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Reproductor de Windows Media , método getAttributeStringCollection
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAttributeStringCollection
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 508630ee8a377e1542f823c1afb21521206369aa3ce489c58afae47efa268880
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118331947"
---
# <a name="iwmpmediacollectiongetattributestringcollection-method"></a>IWMPMediaCollection::getAttributeStringCollection (método)

El **método getAttributeStringCollection** devuelve una interfaz **IWMPStringCollection** que representa el conjunto de todos los valores de un atributo especificado dentro de un tipo de medio.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPStringCollection getAttributeStringCollection(
  System.String bstrAttribute,
  System.String bstrMediaType
);
```


```VB

Public Function getAttributeStringCollection( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPStringCollection
Implements IWMPMediaCollection.getAttributeStringCollection
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrAttribute* \[ En\]
</dt> <dd>

**System.String que** es el atributo para el que se recuperan los valores.

</dd> <dt>

*bstrMediaType* \[ En\]
</dt> <dd>

**System.String que** es el tipo de medio para el que se recuperan los valores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPStringCollection** para los valores recuperados.

## <a name="remarks"></a>Comentarios

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la [Referencia de atributos](attribute-reference.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa getAttributeStringCollection para** mostrar una lista de valores que corresponden a un atributo determinado para los elementos de audio de la colección multimedia. Un cuadro de lista permite al usuario seleccionar un atributo, como Artist, Genre o Album, y un cuadro de texto de varias líneas muestra el resultado. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
private void audioAttributes_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Retrieve the attribute type from the ListBox
    string attributeType = (string)((System.Windows.Forms.ListBox)sender).SelectedItem;

    // Get an interface to the mediaCollection.  
    WMPLib.IWMPMediaCollection2 library = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

    // Get an interface to the string collection for the attribute type the user selects.
    WMPLib.IWMPStringCollection2 all = (WMPLib.IWMPStringCollection2)library.getAttributeStringCollection(attributeType, "Audio");

    // Clear the text box of previous results.
    attributeValues.Clear();

    // Create an array to hold the attribute values.
    string[] attributeArray = new string[all.count];
    
    // Loop through the string collection.
    for (int i = 0; i < all.count; i++)
    {
        // Store the items in the array.
        attributeArray[i] = all.Item(i);
    }

    // Display the items in the text box.
    attributeValues.Lines = attributeArray;
}
```


```VB

Public Sub audioAttributes_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles audioAttributes.SelectedIndexChanged

    &#39; Retrieve the attribute type from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim attributeType As String = lb.SelectedItem

    &#39; Get an interface to the mediaCollection.  
    Dim library As WMPLib.IWMPMediaCollection2 = player.mediaCollection

    &#39; Get an interface to the string collection for the attribute type the user selects.
    Dim all As WMPLib.IWMPStringCollection2 = library.getAttributeStringCollection(attributeType, &quot;Audio&quot;)

    &#39; Clear the text box of previous results.
    attributeValues.Clear()

    &#39; Create an array to hold the attribute values.
    Dim attributeArray(all.count) As String

    &#39; Loop through the string collection.
    For i As Integer = 0 To (all.count - 1)

        &#39; Store the items in the array.
        attributeArray(i) = all.Item(i)

    Next i

    &#39; Display the items in the text box.
    attributeValues.Lines = attributeArray

End Sub
```





## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPStringCollection (VB y C#)**](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





