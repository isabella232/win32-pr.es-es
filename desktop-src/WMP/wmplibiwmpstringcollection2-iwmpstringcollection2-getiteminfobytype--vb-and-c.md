---
title: IWMPStringCollection2 getItemInfobyType (método)
description: El método getItemInfoByType devuelve el valor correspondiente al índice del elemento de colección de cadenas, el nombre, el idioma y el índice de atributo especificados.
ms.assetid: 51035fed-51ce-4cd2-a936-4c99802128f2
keywords:
- Método getItemInfobyType Reproductor de Windows Media
- Método getItemInfobyType Reproductor de Windows Media interfaz , IWMPStringCollection2
- Interfaz IWMPStringCollection2 Reproductor de Windows Media método , getItemInfobyType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfobyType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2894faedc8e2573fad5beaa7744216fbb53fbd1b090e4be2122a3194827f43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899765"
---
# <a name="iwmpstringcollection2getiteminfobytype-method"></a>IWMPStringCollection2::getItemInfobyType (método)

El **método getItemInfoByType** devuelve el valor correspondiente al índice del elemento de colección de cadenas, el nombre, el idioma y el índice de atributo especificados.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Object getItemInfobyType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage,
  System.Int32 lAttributeIndex
);
```


```VB

Public Function getItemInfobyType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String, _
  ByVal lAttributeIndex As System.Int32 _
) As System.Object
Implements IWMPStringCollection2.getItemInfobyType
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*lCollectionIndex* \[ En\]
</dt> <dd>

**System.Int32 que** es el índice de base cero del elemento de colección de cadenas del que se va a obtener el atributo.

</dd> <dt>

*bstrType* \[ En\]
</dt> <dd>

**System.String que** es el nombre del atributo.

</dd> <dt>

*bstrLanguage* \[ En\]
</dt> <dd>

**System.String que** indica el idioma. Si el valor se establece en null o en una cadena de longitud cero (""), se usa la cadena de configuración regional actual. De lo contrario, el valor debe ser una cadena de lenguaje RFC 1766 válida, como "en-us".

</dd> <dt>

*lAttributeIndex* \[ En\]
</dt> <dd>

**System.Int32** que es el índice de base cero del atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Objeto **System.Object que** es el elemento de colección de cadenas.

## <a name="remarks"></a>Comentarios

Este método admite atributos con varios valores y atributos con valores complejos. El **método getItemInfo** no admite atributos con varios valores o atributos con valores complejos.

Al pasar el valor "ChildList" en el parámetro *bstrType,* puede recuperar una nueva colección de cadenas que contenga los elementos secundarios de uno de los elementos de la colección de cadenas primarias. Por ejemplo, si la colección primaria contiene una lista de AlbumIDs, puede usar este método para obtener una colección de cadenas secundaria que contenga todas las pistas de uno de los álbumes. Este enfoque es más rápido y eficaz que llamar dos veces al método **IWMPMediaCollection2.getStringCollectionByQuery.** una vez para obtener una colección de AlbumID y una segunda vez para obtener una colección de pistas para un AlbumID determinado. Para usar ChildList de la manera que se acaba de describir, la colección de cadenas primarias debe obtenerse de una colección de medios a través de **IWMPLibraryServices** y no mediante la propiedad **AxWindowsMediaPlayer.mediaCollection.**

Cuando use ChildList, pase el valor "ChildList" en el *parámetro bstrType* y el valor 0 en el *parámetro lAttributeIndex.* A continuación, puede convertir el objeto que se devuelve a una **interfaz IWMPStringCollection2** para tener acceso a la lista secundaria.

Para usar este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Atributo AlbumID**](albumid-attribute.md)
</dt> <dt>

[**Interfaz IWMPLibraryServices (VB y C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection2.getStringCollectionByQuery (VB y C#)**](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2 (interfaz)**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2.getItemInfo (VB y C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





