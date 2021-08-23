---
title: IWMPMediaCollection2 getPlaylistByQuery (método)
description: El método getPlaylistByQuery devuelve una interfaz IWMPPlaylist que proporciona acceso a elementos multimedia que coinciden con las condiciones de consulta.
ms.assetid: ebbb631f-1faa-4c89-8c1d-cc2b128126b8
keywords:
- Método getPlaylistByQuery Reproductor de Windows Media
- Método getPlaylistByQuery Reproductor de Windows Media , interfaz IWMPMediaCollection2
- Interfaz IWMPMediaCollection2 Reproductor de Windows Media método , getPlaylistByQuery
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
ms.openlocfilehash: acd80467c78aac832c5ac2784281abcf07975a1956ee304c734b2b45b82901fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053583"
---
# <a name="iwmpmediacollection2getplaylistbyquery-method"></a>IWMPMediaCollection2::getPlaylistByQuery (método)

El `getPlaylistByQuery` método devuelve una interfaz **IWMPPlaylist** que proporciona acceso a elementos multimedia que coinciden con las condiciones de consulta.

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

*pQuery* \[ En\]
</dt> <dd>

Interfaz **WMPLib.IWMPQuery** que representa la consulta.

</dd> <dt>

*bstrMediaType* \[ En\]
</dt> <dd>

**System.String que** es el tipo de medio. Debe contener uno de los siguientes valores: "audio", "vídeo", "foto", "lista de reproducción" u "otro".

</dd> <dt>

*bstrSortAttribute* \[ En\]
</dt> <dd>

**System.String que** es el nombre de atributo utilizado para la ordenación. Una cadena de longitud cero ("") significa que no se aplica ninguna ordenación.

</dd> <dt>

*fSortAscending* \[ En\]
</dt> <dd>

Valor **System.Boolean** que indica si la lista de reproducción debe ordenarse en orden ascendente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPPlaylist** para la lista de reproducción recuperada.

## <a name="remarks"></a>Comentarios

Las consultas compuestas **que usan IWMPQuery** no distinguen mayúsculas de minúsculas.

Cuando la consulta compuesta especificada por el *parámetro pQuery* contiene una condición creada en el **atributo MediaType,** esa condición se omite. Siempre se usa el valor del *parámetro bstrMediaType.* Por ejemplo, si la consulta compuesta contiene la condición "MediaType Equals audio" y el valor del parámetro *bstrMediaType* es "video", la lista de reproducción resultante solo contendrá elementos de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
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

[**Atributo MediaType**](mediatype-attribute.md)
</dt> </dl>

 

 





