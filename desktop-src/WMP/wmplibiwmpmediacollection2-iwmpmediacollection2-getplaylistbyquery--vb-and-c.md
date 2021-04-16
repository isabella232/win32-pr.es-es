---
title: IWMPMediaCollection2 getPlaylistByQuery, método
description: El método getPlaylistByQuery devuelve una interfaz IWMPPlaylist que proporciona acceso a los elementos multimedia que coinciden con las condiciones de la consulta.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- método getPlaylistByQuery de Windows Media Player
- método getPlaylistByQuery Windows Media Player, interfaz IWMPMediaCollection2
- Interfaz IWMPMediaCollection2 Windows Media Player, método getPlaylistByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getPlaylistByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109f6e49e77d1cfa8c6d3b45bef1d011faf21a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649883"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a>IWMPMediaCollection2:: getPlaylistByQuery (método)

El `getPlaylistByQuery` método devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia que coinciden con las condiciones de la consulta.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylist getPlaylistByQuery(
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getPlaylistByQuery( _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getPlaylistByQuery
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*pQuery* \[ de\]
</dt> <dd>

La interfaz **WMPLib. IWMPQuery** que representa la consulta.

</dd> <dt>

*bstrMediaType* \[ de\]
</dt> <dd>

**System. String** que es el tipo de medio. Debe contener uno de los siguientes valores: "audio", "vídeo", "foto", "lista de reproducción" u "otro".

</dd> <dt>

*bstrSortAttribute* \[ de\]
</dt> <dd>

**System. String** que es el nombre del atributo utilizado para la ordenación. Una cadena de longitud cero ("") significa que no se aplica ninguna ordenación.

</dd> <dt>

*fSortAscending* \[ de\]
</dt> <dd>

El valor **System. Boolean** que indica si la lista de reproducción se debe ordenar en orden ascendente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una interfaz **WMPLib. IWMPPlaylist** para la lista de reproducción recuperada.

## <a name="remarks"></a>Observaciones

Las consultas compuestas que usan **IWMPQuery** no distinguen mayúsculas de minúsculas.

Cuando la consulta compuesta especificada por el parámetro *pQuery* contiene una condición generada en el atributo **mediatype** , se omite esa condición. Siempre se usa el valor del parámetro *bstrMediaType* . Por ejemplo, si la consulta compuesta contiene la condición "MediaType Equals audio" y el valor del parámetro *bstrMediaType* es "video", la lista de reproducción resultante solo contendrá elementos de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPMediaCollection2 (VB y C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPQuery (VB y C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**MediaType (atributo)**](mediatype-attribute.md)
</dt> </dl>

 

 





