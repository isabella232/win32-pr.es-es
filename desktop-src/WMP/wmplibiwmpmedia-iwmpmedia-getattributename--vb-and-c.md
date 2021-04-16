---
title: IWMPMedia getAttributeName, método
description: El método getAttributeName devuelve el nombre del atributo correspondiente al índice especificado.
ms.assetid: d2496484-34cc-4222-9bc3-1d3ebb9a4173
keywords:
- método getAttributeName de Windows Media Player
- método getAttributeName Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, método getAttributeName
topic_type:
- apiref
api_name:
- IWMPMedia.getAttributeName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb40ef8c0c984258dc11dd00c80807db2f4eb64a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671589"
---
# <a name="iwmpmediagetattributename-method"></a>IWMPMedia:: getAttributeName (método)

El método **getAttributeName** devuelve el nombre del atributo correspondiente al índice especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String getAttributeName(
  System.Int32 lIndex
);
```


```VB

Public Function getAttributeName( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPMedia.getAttributeName
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*lIndex* \[ de\]
</dt> <dd>

**System. Int32** que es el índice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. String** que es el nombre del atributo.

## <a name="remarks"></a>Observaciones

El nombre de atributo devuelto se puede usar junto con **getItemInfo** para recuperar el valor de un atributo con nombre específico.

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

Para obtener información sobre los atributos que admite Windows Media Player, vea la [referencia de atributo](attribute-reference.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **getAttributeName** para rellenar un cuadro de texto de varias líneas con el índice y el nombre de cada atributo del elemento multimedia actual. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
// Store an IWMPMedia3 interface for the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes for the current media item. 
int attCount = cm.attributeCount;

// Create an array of strings to hold the index and name for each attribute.
string[] attInfo = new string[attCount];

// Loop through the attribute list.
for (int i = 0; i < attCount; i++)
{
    // Store the attribute index and name in the array.
    attInfo[i] = ("Attribute " + i + ": " + cm.getAttributeName(i));
}

// Display the attribute information in the text box.
attributeNames.Lines = attInfo;
```


```VB

' Store an IWMPMedia3 interface for the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes for the current media. 
Dim attCount As Integer = cm.attributeCount

&#39; Create an array of strings to hold the index and name for each attribute.
Dim attInfo(attCount) As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (attCount - 1)

    &#39; Store the attribute index and name in the array.
    attInfo(i) = (&quot;Attribute &quot; + i.ToString() + &quot;: &quot; + cm.getAttributeName(i))

Next i

&#39; Display the attribute information in the text box.
attributeNames.Lines = attInfo
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfo (VB y C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





