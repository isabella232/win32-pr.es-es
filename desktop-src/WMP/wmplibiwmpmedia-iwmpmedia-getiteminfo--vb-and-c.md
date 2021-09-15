---
title: Método IWMPMedia getItemInfo
description: El método getItemInfo devuelve el valor del atributo especificado para el elemento multimedia.
ms.assetid: b95fa61d-a600-4f31-a930-d80516204034
keywords:
- Método getItemInfo Reproductor de Windows Media
- Método getItemInfo Reproductor de Windows Media , interfaz IWMPMedia
- Interfaz IWMPMedia Reproductor de Windows Media método , getItemInfo
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258719"
---
# <a name="iwmpmediagetiteminfo-method"></a>IWMPMedia::getItemInfo (método)

El **método getItemInfo** devuelve el valor del atributo especificado para el elemento multimedia.

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

*bstrItemName* \[ En\]
</dt> <dd>

**System.String que** es el nombre del atributo. Para obtener información sobre los atributos admitidos por Reproductor de Windows Media, vea la [Referencia de atributos](attribute-reference.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.String que** es el valor del atributo especificado.

## <a name="remarks"></a>Observaciones

Este método devuelve los metadatos de un elemento multimedia individual o un elemento multimedia que forma parte de una lista de reproducción.

La **propiedad attributeCount** obtiene el número de nombres de atributo disponibles para un elemento multimedia determinado. A continuación, los números de índice se pueden usar **con el método getAttributeName** para determinar el nombre de cada atributo disponible. Los nombres de atributo individuales se pueden pasar **a getItemInfo.**

Para recuperar atributos con varios valores y atributos con valores complejos, use el **método getItemInfoByType.**

Si el elemento multimedia provenía de una biblioteca recuperada mediante una llamada a [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el conjunto de atributos disponibles será diferente de los que se pueden consultar desde la biblioteca local recuperada mediante una llamada a [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md). Por ejemplo, los atributos disponibles de la biblioteca local recuperados mediante **IWMPLibrary** serán un subconjunto de los atributos disponibles en la biblioteca local recuperada mediante **IWMPCore**. Los demás orígenes definen el conjunto de atributos disponibles en otros orígenes (bibliotecas remotas, dispositivos portátiles o CD).

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Referencia de atributos**](attribute-reference.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.attributeCount (VB y C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.getAttributeName (VB y C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.setItemInfo (VB y C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getItemInfoByType (VB y C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





