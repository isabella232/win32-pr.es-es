---
title: IWMPMedia getItemInfo, método
description: El método getItemInfo devuelve el valor del atributo especificado para el elemento multimedia.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- método getItemInfo de Windows Media Player
- método getItemInfo Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523e57e68d13df55395cd4deca6e09904723bbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671588"
---
# <a name="iwmpmediagetiteminfo-method"></a>IWMPMedia:: getItemInfo (método)

El método **getItemInfo** devuelve el valor del atributo especificado para el elemento multimedia.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String getItemInfo(
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPMedia.getItemInfo
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrItemName* \[ de\]
</dt> <dd>

**System. String** que es el nombre del atributo. Para obtener información sobre los atributos que admite Windows Media Player, vea la [referencia de atributo](attribute-reference.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. String** que es el valor del atributo especificado.

## <a name="remarks"></a>Observaciones

Este método devuelve los metadatos de un elemento multimedia individual o de un elemento multimedia que forma parte de una lista de reproducción.

La propiedad **attributeCount** obtiene el número de nombres de atributo disponibles para un elemento multimedia determinado. Los números de índice se pueden usar con el método **getAttributeName** para determinar el nombre de cada atributo disponible. Los nombres de atributo individuales se pueden pasar a **getItemInfo**.

Para recuperar los atributos con varios valores y atributos con valores complejos, use el método **getItemInfoByType** .

Si el elemento multimedia procede de una biblioteca que se ha recuperado mediante una llamada a [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el conjunto de atributos disponibles será distinto de los que se pueden consultar desde la biblioteca local recuperada mediante una llamada a [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md). Por ejemplo, los atributos disponibles en la biblioteca local recuperada mediante **IWMPLibrary** serán un subconjunto de los atributos disponibles en la biblioteca local recuperada mediante **IWMPCore**. Los demás orígenes definen el conjunto de atributos disponibles de otros orígenes (bibliotecas remotas, dispositivos portátiles o CDs).

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia de atributo**](attribute-reference.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. attributeCount (VB y C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getAttributeName (VB y C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. setItemInfo (VB y C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB y C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





