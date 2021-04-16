---
title: IWMPMedia getItemInfoByAtom, método
description: El método getItemInfoByAtom devuelve el valor del atributo con el número de índice especificado.
ms.assetid: d9a4b737-add1-4bbd-8e03-e58f45d65a62
keywords:
- método getItemInfoByAtom de Windows Media Player
- método getItemInfoByAtom Windows Media Player, interfaz IWMPMedia
- Interfaz IWMPMedia Windows Media Player, método getItemInfoByAtom
topic_type:
- apiref
api_name:
- IWMPMedia.getItemInfoByAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb37243960360120fbfe508a39db31e37728ac39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671585"
---
# <a name="iwmpmediagetiteminfobyatom-method"></a>IWMPMedia:: getItemInfoByAtom (método)

El método **getItemInfoByAtom** devuelve el valor del atributo con el número de índice especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String getItemInfoByAtom(
  System.Int32 lAtom
);
```


```VB

Public Function getItemInfoByAtom( _
  ByVal lAtom As System.Int32 _
) As System.String
Implements IWMPMedia.getItemInfoByAtom
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*lAtom* \[ de\]
</dt> <dd>

**System. Int32** que especifica el índice en el que reside el atributo solicitado dentro del conjunto de atributos disponibles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. String** que es el valor del atributo.

## <a name="remarks"></a>Observaciones

Este método se puede utilizar para recuperar los metadatos de un elemento multimedia específico mediante un número de índice de atributo. La propiedad **attributeCount** se puede utilizar para determinar el número de atributos disponibles para el elemento multimedia.

También se puede usar el método **getMediaAtom** de la interfaz **IWMPMediaCollection** para recuperar el índice de un atributo determinado. Esta técnica suele ser más eficaz que los métodos **getItemInfo** o **getItemInfoByType** al trabajar con listas de reproducción grandes.

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

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

[**IWMPMedia. attributeCount (VB y C#)**](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfo (VB y C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. setItemInfo (VB y C#)**](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB y C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection. getMediaAtom (VB y C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getmediaatom--vb-and-c.md)
</dt> </dl>

 

 





