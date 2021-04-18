---
title: IWMPMediaCollection getMediaAtom, método
description: El método getMediaAtom devuelve el índice de un atributo especificado en el conjunto de atributos disponibles.
ms.assetid: 01e3d073-677b-4939-96d3-63ae96eaa25d
keywords:
- método getMediaAtom de Windows Media Player
- método getMediaAtom Windows Media Player, interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Windows Media Player, método getMediaAtom
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
ms.openlocfilehash: 08487cf60c351ff4f8e0741209655cb78c30c3f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700337"
---
# <a name="iwmpmediacollectiongetmediaatom-method"></a>IWMPMediaCollection:: getMediaAtom (método)

El `getMediaAtom` método devuelve el índice de un atributo especificado en el conjunto de atributos disponibles.

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

*bstrItemName* \[ de\]
</dt> <dd>

**System. String** que es el nombre del elemento para el que se debe recuperar el índice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. Int32** que es el índice.

## <a name="remarks"></a>Observaciones

El número de índice recuperado con este método se puede pasar a **IWMPMedia. getItemInfoByAtom** para tener acceso a los valores de atributo. Esta técnica suele ser más eficaz al trabajar con listas de reproducción de gran tamaño que el acceso a un valor de atributo por nombre a través de **IWMPMedia. getItemInfo**.

Antes de llamar a este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMPMedia. getItemInfo (VB y C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. getItemInfoByAtom (VB y C#)**](wmplibiwmpmedia-iwmpmedia-getiteminfobyatom--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMediaCollection (VB y C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





