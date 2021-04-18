---
title: IWMPQuery beginNextGroup, método
description: El método beginNextGroup comienza un nuevo grupo de condiciones. | IWMPQuery beginNextGroup, método
ms.assetid: 15d20c9f-2ce7-4a86-9054-b7317ebe1a0a
keywords:
- método beginNextGroup de Windows Media Player
- método beginNextGroup Windows Media Player, interfaz IWMPQuery
- Interfaz IWMPQuery Windows Media Player, método beginNextGroup
topic_type:
- apiref
api_name:
- IWMPQuery.beginNextGroup
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866727f821fb40b6bf09f3ee2cf0231c4ffc3005
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718881"
---
# <a name="iwmpquerybeginnextgroup-method"></a>IWMPQuery:: beginNextGroup (método)

El método **beginNextGroup** comienza un nuevo grupo de condiciones.

## <a name="syntax"></a>Sintaxis


```CSharp
public void beginNextGroup();
```


```VB

Public Sub beginNextGroup()
Implements IWMPQuery.beginNextGroup
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El inicio de un nuevo grupo de condiciones implica que se ha completado el grupo de condiciones actual. El nuevo grupo de condiciones siempre se concatena al grupo de condiciones anterior mediante la lógica **o** .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea una consulta compleja mediante la combinación de dos grupos, cada uno de los cuales contiene una condición. Los resultados de la consulta se extraen como una colección de cadenas y se muestran en un cuadro de lista. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");

// Begin another Query group.
q.beginNextGroup();

// Add a condition to the new group understanding that it will be combined with the
// first group using OR logic.
q.addCondition("Title", "Contains", "Capriol");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    complexQueryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

' Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi")

' Begin another Query group.
q.beginNextGroup()

' Add a condition to the new group understanding that it will be combined with the
' first group using OR logic.
q.addCondition("Title", "Contains", "Capriol")

' Query the media collection and get a string collection containing the result.
' In this case, the string collection will contain the titles of all audio items that
' match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery("Title", q, "audio", "", False)

' Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    complexQueryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMPMediaCollection2. createQuery (VB y C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getPlaylistByQuery (VB y C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2. getStringCollectionByQuery (VB y C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPQuery (VB y C#)**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





