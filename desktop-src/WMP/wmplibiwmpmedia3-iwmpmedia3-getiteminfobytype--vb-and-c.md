---
title: IWMPMedia3 getItemInfoByType, método
description: El método getItemInfoByType devuelve el valor del atributo correspondiente al tipo de atributo y el índice especificados.
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- método getItemInfoByType de Windows Media Player
- método getItemInfoByType Windows Media Player, interfaz IWMPMedia3
- Interfaz IWMPMedia3 Windows Media Player, método getItemInfoByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getItemInfoByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f37992201d5d19397724071f8c2a4b8e851aac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670363"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a>IWMPMedia3:: getItemInfoByType (método)

El método **getItemInfoByType** devuelve el valor del atributo correspondiente al tipo de atributo y el índice especificados.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Object getItemInfoByType(
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lIndex
);
```


```VB

Public Function getItemInfoByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lIndex As System.Int32 _
) As System.Object
Implements IWMPMedia3.getItemInfoByType
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrType* \[ de\]
</dt> <dd>

**System. String** que es el tipo de atributo.

</dd> <dt>

*bstrLanguage* \[ de\]
</dt> <dd>

**System. String** que es el idioma. Si el valor se establece en null o en una cadena de longitud cero (""), se usa la cadena de configuración regional actual. De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-US".

</dd> <dt>

*lIndex* \[ de\]
</dt> <dd>

**System. Int32** que es el índice de atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**Objeto System. Object** que es el valor del atributo. El tipo al que se va a convertir este objeto depende del tipo de atributo.

## <a name="remarks"></a>Observaciones

Este método devuelve los metadatos de un elemento multimedia o elemento multimedia individual que forma parte de una lista de reproducción.

Este método admite atributos con varios valores y atributos con valores complejos. El método **getItemInfo** no admite atributos con varios valores y atributos con valores complejos.

La propiedad **attributeCount** obtiene el número de nombres de atributo disponibles para un elemento multimedia determinado. Los números de índice se pueden usar con el método **getAttributeName** para determinar el nombre de cada atributo disponible. Los nombres de atributo individuales se pueden pasar al parámetro *Name* de **getItemInfoByType**.

El método **getAttributeCountByType** devuelve el número de atributos que corresponden a un nombre de atributo determinado para un elemento multimedia determinado. Los números de índice se pueden pasar al parámetro de *Índice* de **getItemInfoByType**. Esto resulta útil cuando un elemento multimedia se ha clasificado en varios géneros, por ejemplo.

Si el elemento multimedia procede de una biblioteca que se ha recuperado mediante una llamada a [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el conjunto de atributos disponibles será distinto de los que se pueden consultar desde la biblioteca local recuperada mediante una llamada a [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md). Por ejemplo, los atributos disponibles en la biblioteca local recuperada mediante **IWMPLibrary** serán un subconjunto de los atributos disponibles en la biblioteca local recuperada mediante **AxWindowsMediaPlayer**. El conjunto de atributos disponibles de otros orígenes (bibliotecas remotas, dispositivos portátiles o CDs está definido por otros orígenes.

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPMedia3 (VB y C#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB y C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getAttributeName (VB y C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfo (VB y C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getAttributeCountByType (VB y C#)**](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 





