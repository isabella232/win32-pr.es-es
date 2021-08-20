---
title: Método IWMPMedia3 getItemInfoByType
description: El método getItemInfoByType devuelve el valor del atributo correspondiente al tipo de atributo y al índice especificados.
ms.assetid: e4cf14b4-3c59-485f-a573-734a0076647b
keywords:
- Método getItemInfoByType Reproductor de Windows Media
- Método getItemInfoByType Reproductor de Windows Media , interfaz IWMPMedia3
- Interfaz IWMPMedia3 Reproductor de Windows Media , método getItemInfoByType
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
ms.openlocfilehash: fdcfd965af6ac6201687ca8c7ecc7584085b7810a2c0ca11bbc70c1b04403c5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929869"
---
# <a name="iwmpmedia3getiteminfobytype-method"></a>IWMPMedia3::getItemInfoByType (método)

El **método getItemInfoByType** devuelve el valor del atributo correspondiente al tipo de atributo y al índice especificados.

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

*bstrType* \[ En\]
</dt> <dd>

**System.String que** es el tipo de atributo.

</dd> <dt>

*bstrLanguage* \[ En\]
</dt> <dd>

**System.String que** es el idioma. Si el valor se establece en null o en una cadena de longitud cero (""), se usa la cadena de configuración regional actual. De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-us".

</dd> <dt>

*lIndex* \[ En\]
</dt> <dd>

**System.Int32 que** es el índice de atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto **System.Object** que es el valor del atributo. El tipo al que se va a convertir este objeto depende del tipo del atributo.

## <a name="remarks"></a>Comentarios

Este método devuelve los metadatos de un elemento multimedia digital individual o un elemento multimedia que forma parte de una lista de reproducción.

Este método admite atributos con varios valores y atributos con valores complejos. El **método getItemInfo** no admite atributos con varios valores y atributos con valores complejos.

La **propiedad attributeCount** obtiene el número de nombres de atributo disponibles para un elemento multimedia determinado. Los números de índice se pueden usar con el **método getAttributeName** para determinar el nombre de cada atributo disponible. Los nombres de atributo individuales se pueden pasar al *parámetro name* **de getItemInfoByType**.

El **método getAttributeCountByType** devuelve el número de atributos que corresponden a un nombre de atributo determinado para un elemento multimedia determinado. A continuación, se pueden pasar números de índice al *parámetro index* **de getItemInfoByType**. Esto resulta útil cuando un elemento multimedia se ha clasificado en varios géneros, por ejemplo.

Si el elemento multimedia provenía de una biblioteca recuperada mediante una llamada a [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el conjunto de atributos disponibles será diferente de los que se pueden consultar desde la biblioteca local recuperada mediante una llamada a [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md). Por ejemplo, los atributos disponibles de la biblioteca local recuperados mediante **IWMPLibrary** serán un subconjunto de los atributos disponibles de la biblioteca local recuperados mediante **AxWindowsMediaPlayer**. El conjunto de atributos disponibles en otros orígenes (bibliotecas remotas, dispositivos portátiles o CDs lo definen los demás orígenes).

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPMedia3 (VB y C#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.attributeCount (VB y C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.getAttributeName (VB y C#)**](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.getItemInfo (VB y C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getAttributeCountByType (VB y C#)**](wmplibiwmpmedia3-iwmpmedia3-getattributecountbytype--vb-and-c.md)
</dt> </dl>

 

 





