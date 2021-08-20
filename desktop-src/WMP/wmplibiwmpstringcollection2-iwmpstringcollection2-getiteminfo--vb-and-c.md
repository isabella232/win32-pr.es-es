---
title: IWMPStringCollection2 getItemInfo (método)
description: El método getItemInfo devuelve la cadena correspondiente al índice y el nombre del elemento de colección de cadenas especificado.
ms.assetid: 4a107e85-9eb7-42be-b1f9-8e9e92e6e509
keywords:
- Método getItemInfo Reproductor de Windows Media
- Método getItemInfo Reproductor de Windows Media , interfaz IWMPStringCollection2
- Interfaz IWMPStringCollection2 Reproductor de Windows Media método , getItemInfo
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f3f5371d55384544e4135e702b686cc7ce36707d204529ca7a4e68a3734d8ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899845"
---
# <a name="iwmpstringcollection2getiteminfo-method"></a>IWMPStringCollection2::getItemInfo (método)

El **método getItemInfo** devuelve la cadena correspondiente al índice y el nombre del elemento de colección de cadenas especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String getItemInfo(
  System.Int32 lCollectionIndex,
  System.String bstrItemName
);
```


```VB

Public Function getItemInfo( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrItemName As System.String _
) As System.String
Implements IWMPStringCollection2.getItemInfo
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*lCollectionIndex* \[ En\]
</dt> <dd>

**System.Int32 que especifica** el índice de base cero del elemento de colección de cadenas del que se va a obtener el atributo.

</dd> <dt>

*bstrItemName* \[ En\]
</dt> <dd>

**System.String que** es el nombre del atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.String que** es el nombre del elemento de colección de cadenas. Para los atributos cuyo valor subyacente **es System.Boolean,** devuelve la cadena "true" o "false".

## <a name="remarks"></a>Comentarios

Para recuperar atributos con varios valores y atributos con valores complejos, use el **método getItemInfoByType.**

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMPStringCollection2 (Interfaz)**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2.getItemInfoByType (VB y C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





