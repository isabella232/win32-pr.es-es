---
title: Método IWMPMediaCollection2 getStringCollectionByQuery
description: El método getStringCollectionByQuery devuelve una interfaz IWMPStringCollection que proporciona acceso al conjunto de todos los valores de cadena de un atributo especificado que coinciden con las condiciones de consulta.
ms.assetid: 2d3b29af-0b6c-4405-8334-9a47a30ff6de
keywords:
- Método getStringCollectionByQuery Reproductor de Windows Media
- Método getStringCollectionByQuery Reproductor de Windows Media , interfaz IWMPMediaCollection2
- Interfaz IWMPMediaCollection2 Reproductor de Windows Media , método getStringCollectionByQuery
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getStringCollectionByQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322781bc9ddec3e6f8d74d7229f16ce38e519f05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466009"
---
# <a name="iwmpmediacollection2getstringcollectionbyquery-method"></a>IWMPMediaCollection2::getStringCollectionByQuery (método)

El `getStringCollectionByQuery` método devuelve una interfaz **IWMPStringCollection** que proporciona acceso al conjunto de todos los valores de cadena para un atributo especificado que coinciden con las condiciones de consulta.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPStringCollection getStringCollectionByQuery(
  System.String bstrAttribute,
  IWMPQuery pQuery,
  System.String bstrMediaType,
  System.String bstrSortAttribute,
  System.Boolean fSortAscending
);
```


```VB

Public Function getStringCollectionByQuery( _
  ByVal bstrAttribute As System.String, _
  ByVal pQuery As IWMPQuery, _
  ByVal bstrMediaType As System.String, _
  ByVal bstrSortAttribute As System.String, _
  ByVal fSortAscending As System.Boolean _
) As IWMPStringCollection
Implements IWMPMediaCollection2.getStringCollectionByQuery
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrAttribute* \[ En\]
</dt> <dd>

**System.String que** es el nombre del atributo.

</dd> <dt>

*pQuery* \[ En\]
</dt> <dd>

Interfaz **WMPLib.IWMPQuery** que es la consulta que define las condiciones usadas para recuperar la colección de cadenas.

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

Valor **System.Boolean** que indica si el conjunto de valores de cadena debe ordenarse en orden ascendente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPStringCollection** para el conjunto recuperado de valores de cadena.

## <a name="remarks"></a>Observaciones

Las consultas compuestas **que usan IWMPQuery** no distinguen mayúsculas de minúsculas.

Cuando la consulta compuesta especificada por el parámetro *pQuery* contiene una condición creada en el **atributo MediaType,** esa condición se omite. Siempre se usa el valor del *parámetro bstrMediaType.* Por ejemplo, si la consulta compuesta contiene la condición "MediaType Equals audio" y el valor del parámetro *bstrMediaType* es "video", la lista de reproducción resultante solo contendrá elementos de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPMediaCollection2 (VB y C#)**](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPQuery (VB y C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPStringCollection (VB y C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**Atributo MediaType**](mediatype-attribute.md)
</dt> </dl>

 

 





