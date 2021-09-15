---
title: Método IWMPPlaylist getItemInfo
description: El método getItemInfo devuelve el valor de un atributo de lista de reproducción especificado por nombre.
ms.assetid: 62e882d6-66bb-450c-9700-b99d30dd42fa
keywords:
- Método getItemInfo Reproductor de Windows Media
- Método getItemInfo Reproductor de Windows Media , interfaz IWMPPlaylist
- Interfaz IWMPPlaylist Reproductor de Windows Media , método getItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced433b13f5af2d1df8c12dba023b7fbb55c5f7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467009"
---
# <a name="iwmpplaylistgetiteminfo-method"></a>IWMPPlaylist::getItemInfo (método)

El **método getItemInfo** devuelve el valor de un atributo de lista de reproducción especificado por nombre.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.String getItemInfo(
  System.String bstrName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrName As System.String _
) As System.String
Implements IWMPPlaylist.getItemInfo
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrName* \[ En\]
</dt> <dd>

**System.String que** es el nombre del atributo de lista de reproducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.String que** es el valor del atributo de lista de reproducción.

## <a name="remarks"></a>Observaciones

Antes de usar este método, debe tener acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

Vea la [propiedad attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) para obtener código de ejemplo que usa esta propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.setItemInfo (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





