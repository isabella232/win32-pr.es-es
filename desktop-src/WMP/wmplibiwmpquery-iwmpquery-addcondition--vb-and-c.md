---
title: Método addCondition de IWMPQuery
description: El método addCondition agrega una condición a la consulta compuesta mediante la lógica AND.
ms.assetid: 4594ee6f-b153-4d53-b3ee-cd1718a4d5dc
keywords:
- Método addCondition Reproductor de Windows Media
- Método addCondition Reproductor de Windows Media , interfaz IWMPQuery
- Interfaz IWMPQuery Reproductor de Windows Media , método addCondition
topic_type:
- apiref
api_name:
- IWMPQuery.addCondition
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de3015ef0389fef82934cbd8e9326b6f9ec2307
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580168"
---
# <a name="iwmpqueryaddcondition-method"></a>IWMPQuery::addCondition (método)

El **método addCondition** agrega una condición a la consulta compuesta mediante la **lógica AND.**

## <a name="syntax"></a>Sintaxis


```CSharp
public void addCondition(
  System.String bstrAttribute,
  System.String bstrOperator,
  System.String bstrValue
);
```


```VB

Public Sub addCondition( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrOperator As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPQuery.addCondition
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrAttribute* \[ En\]
</dt> <dd>

**System.String que** es el nombre del atributo que se va a agregar a la consulta.

</dd> <dt>

*bstrOperator* \[ En\]
</dt> <dd>

**System.String que** es el operador . Consulte Comentarios para ver los valores admitidos.

</dd> <dt>

*bstrValue* \[ En\]
</dt> <dd>

**System.String que** es el valor del atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Las condiciones contenidas en una consulta compuesta se organizan en grupos de condiciones. Varias condiciones dentro de un grupo de condiciones siempre se concatenan mediante la **lógica AND.** Los grupos de condiciones siempre se concatenan entre sí mediante la **lógica OR.** Para iniciar un nuevo grupo de condiciones, llame [a IWMPQuery.beginNextGroup](wmplibiwmpquery-iwmpquery-beginnextgroup--vb-and-c.md).

Las consultas compuestas **que usan IWMPQuery** no distinguen mayúsculas de minúsculas.

Puede encontrar una lista de valores para *el parámetro bstrAttribute* en [Referencia alfabética de atributos](alphabetical-attribute-reference.md).

En la tabla siguiente se enumeran los valores admitidos *para bstrOperator*.



| String              | Se aplica a     |
|---------------------|----------------|
| BeginsWith          | Cadenas        |
| Contiene            | Cadenas        |
| es igual a              | Todos los tipos      |
| GreaterThan         | Números, fechas |
| GreaterThanOrEquals | Números, fechas |
| LessThan            | Números, fechas |
| LessThanOrEquals    | Números, fechas |
| NotBeginsWith       | Cadenas        |
| NotContains         | Cadenas        |
| NotEquals           | Todos los tipos      |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea una consulta, se le agregan dos condiciones y se usa esa consulta para extraer los resultados de la consulta como una colección de cadenas. A continuación, los resultados se muestran en un cuadro de lista. El **objeto AxWMPLib.AxWindowsMediaPlayer** se representa mediante la variable denominada player.


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add two conditions to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");
q.addCondition("Title", "Contains", "Trio");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    queryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

&#39; Add two conditions to the Query. 
q.addCondition(&quot;WM/Composer&quot;, &quot;Equals&quot;, &quot;Antonio Vivaldi&quot;)
q.addCondition(&quot;Title&quot;, &quot;Contains&quot;, &quot;Trio&quot;)

&#39; Query the media collection and get a string collection containing the result.
&#39; In this case, the string collection will contain the titles of all audio items that
&#39; match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, q, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    queryResults.Items.Add(result.Item(i))

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

[**Referencia alfabética de atributos**](alphabetical-attribute-reference.md)
</dt> <dt>

[**IWMPMediaCollection2.createQuery (VB y C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2.getPlaylistByQuery (VB y C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2.getStringCollectionByQuery (VB y C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPQuery (interfaz)**](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





