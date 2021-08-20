---
title: Método IWMPMediaCollection getMediaAtom
description: El método getMediaAtom devuelve el índice de un atributo especificado dentro del conjunto de atributos disponibles.
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- Método getMediaAtom Reproductor de Windows Media
- Método getMediaAtom Reproductor de Windows Media , interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Reproductor de Windows Media método , getMediaAtom
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getMediaAtom
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39bd626537defe07fd214c61e29aac67f8c125034817f8a9041a586ab3b24e35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929778"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a>IWMPMediaCollection::getMediaAtom (método)

El `getMediaAtom` método devuelve el índice de un atributo especificado dentro del conjunto de atributos disponibles.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 getMediaAtom(
  System.String bstrItemName
);
```


```VB

Public Function getMediaAtom( _
  ByVal bstrItemName As System.String _
) As System.Int32
Implements IWMPMediaCollection.getMediaAtom
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrItemName* \[ En\]
</dt> <dd>

**System.String que** es el nombre del elemento para el que se debe recuperar el índice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.Int32 que** es el índice.

## <a name="remarks"></a>Comentarios

El número de índice recuperado con este método se puede pasar a **IWMPMedia.getItemInfoByAtom para** tener acceso a los valores de atributo. Esta técnica suele ser más eficaz cuando se trabaja con listas de reproducción grandes que al acceder a un valor de atributo por nombre a través **de IWMPMedia.getItemInfo**.

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMPMedia.getItemInfo (VB y C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia.getItemInfoByAtom (VB y C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





