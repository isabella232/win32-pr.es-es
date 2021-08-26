---
title: Método createQuery de IWMPMediaCollection2
description: El método createQuery devuelve una interfaz IWMPQuery que representa una nueva consulta.
ms.assetid: a12da325-e77e-4e44-93d1-5e9c5733ea44
keywords:
- Método createQuery Reproductor de Windows Media
- Método createQuery Reproductor de Windows Media , interfaz IWMPMediaCollection2
- Interfaz IWMPMediaCollection2 Reproductor de Windows Media , método createQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.createQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1644748008e2b222fef0101a96892d480ad4723b9892b94e0e69c387b54e53d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000095"
---
# <a name="iwmpmediacollection2createquery-method"></a>IWMPMediaCollection2::createQuery (método)

El `createQuery` método devuelve una interfaz **IWMPQuery** que representa una nueva consulta.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPQuery createQuery();
```


```VB

Public Function createQuery() As IWMPQuery
Implements IWMPMediaCollection2.createQuery
```





## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPQuery** que representa una nueva consulta vacía.

## <a name="remarks"></a>Comentarios

La creación de una nueva consulta es el primer paso para crear una consulta compuesta.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente `createQuery` se usa para obtener una interfaz **IWMPQuery** que se inicializa en null. Dado que esta consulta no tiene ninguna condición agregada, cuando se usa como argumento en el método **getStringCollectionByQuery,** el método devolverá una colección de cadenas que contiene todos los elementos multimedia del tipo de medio especificado. A continuación, la colección de cadenas se muestra en un cuadro de lista.


```CSharp
// Get an IWMPMediaCollection2 interface so that you can access the createQuery and
// getStringCollectionByQuery methods.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

// Create an IWMPQuery interface with no conditions added to it.
WMPLib.IWMPQuery nullQuery = mc.createQuery();

// Get a string collection that contains the titles of all the audio items in the media
// collection.
WMPLib.IWMPStringCollection2 allTitles = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", nullQuery, "audio", "", false);

// Display the titles by adding them to a list box.
for (int i = 0; i < allTitles.count; i++)
{
    queryResults.Items.Add(allTitles.Item(i));
}
```


```VB

' Get an IWMPMediaCollection2 interface so that you can access
&#39; the createQuery and getStringCollectionByQuery methods.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection

&#39; Create an IWMPQuery interface with no conditions added to it.
Dim nullQuery As WMPLib.IWMPQuery = mc.createQuery()

&#39; Get a string collection that contains the titles of all the audio items in the media
&#39; collection
Dim allTitles As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, nullQuery, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the titles by adding them to a ListBox
For i As Integer = 0 To (allTitles.count - 1)

    queryResults.Items.Add(allTitles.Item(i))

Next i
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPMediaCollection2 (VB y C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPQuery (VB y C#)**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





