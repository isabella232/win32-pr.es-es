---
title: Propiedad AttributeCount de IWMPMedia
description: La propiedad attributeCount obtiene el número de atributos que se pueden consultar o establecer para el elemento multimedia.
ms.assetid: 527298ff-365d-41b0-90dd-e236d6adf6fa
keywords:
- attributeCount, propiedad Reproductor de Windows Media
- Propiedad attributeCount Reproductor de Windows Media , interfaz IWMPMedia
- Interfaz IWMPMedia Reproductor de Windows Media , propiedad attributeCount
topic_type:
- apiref
api_name:
- IWMPMedia.attributeCount
- IWMPMedia.get_attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5a56d06a54590afd315f04a90aa582f3a364db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473305"
---
# <a name="iwmpmediaattributecount-property"></a>Propiedad IWMPMedia::attributeCount

La **propiedad attributeCount** obtiene el número de atributos que se pueden consultar o establecer para el elemento multimedia.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 attributeCount {get;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a>Valor de propiedad

**System.Int32 que** es el recuento.

## <a name="remarks"></a>Observaciones

Antes de usar esta propiedad, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la [Referencia de atributos](attribute-reference.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa attributeCount** para determinar el número de atributos disponibles en el elemento multimedia actual. El código usa ese valor para mostrar una lista de nombres de atributo y valores en un cuadro de texto. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Store an IWMPMedia3 interface to the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Store the number of attributes in the current media item using attributeCount.
int numAttributes = cm.attributeCount;

// Create strings to hold each attribute name and value.
string atName;
string atValue;

// Create an array to hold the attribute list.
string [] atList = new string[numAttributes];

// Loop through the attribute list.   
for (int i = 0; i < numAttributes; i++)
{
    // Fill the strings with the attribute information.
    atName = cm.getAttributeName(i);
    atValue = cm.getItemInfo(atName);

    // Store the attribute information in an array.
    atList[i] = (atName + ": " + atValue);
}

// Display the attribute information in the text box.
attributeList.Lines = atList;
```


```VB

' Store an IWMPMedia3 interface to the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Store the number of attributes in the current media item using attributeCount.
Dim numAttributes As Integer = cm.attributeCount

&#39; Create strings to hold each attribute name and value.
Dim atName As String
Dim atValue As String

&#39; Create an array to hold the attribute list.
Dim atList(numAttributes) As String

&#39; Loop through the attribute list.   
For i As Integer = 0 To (numAttributes - 1)

    &#39; Fill the strings with the attribute information.
    atName = cm.getAttributeName(i)
    atValue = cm.getItemInfo(atName)

    &#39; Store the attribute information in an array.
    atList(i) = (atName + &quot;: &quot; + atValue)

Next i

&#39; Display the attribute information in the text box.
attributeList.Lines = atList
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





