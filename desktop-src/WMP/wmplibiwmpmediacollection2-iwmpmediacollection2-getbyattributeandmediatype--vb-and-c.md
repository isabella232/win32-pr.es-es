---
title: IWMPMediaCollection2 getByAttributeAndMediaType (método)
description: El método getByAttributeAndMediaType devuelve una interfaz IWMPPlaylist que proporciona acceso a los elementos multimedia que tienen un atributo y un tipo de medio especificados.
ms.assetid: dce9cef4-1d12-4bee-a75d-42274556c5bc
keywords:
- Método getByAttributeAndMediaType Reproductor de Windows Media
- Método getByAttributeAndMediaType Reproductor de Windows Media interfaz , IWMPMediaCollection2
- Interfaz IWMPMediaCollection2 Reproductor de Windows Media método , getByAttributeAndMediaType
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.getByAttributeAndMediaType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb1ee4e9421b4546cdc8ace6173dacab5034b905
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359258"
---
# <a name="iwmpmediacollection2getbyattributeandmediatype-method"></a>IWMPMediaCollection2::getByAttributeAndMediaType (método)

El `getByAttributeAndMediaType` método devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia que tienen un atributo y un tipo de medio especificados.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPPlaylist getByAttributeAndMediaType(
  System.String bstrAttribute,
  System.String bstrValue,
  System.String bstrMediaType
);
```


```VB

Public Function getByAttributeAndMediaType( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection2.getByAttributeAndMediaType
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrAttribute* \[ En\]
</dt> <dd>

**System.String que** es el atributo especificado.

</dd> <dt>

*bstrValue* \[ En\]
</dt> <dd>

**System.String que** es el valor especificado para el atributo especificado en *bstrAttribute.*

</dd> <dt>

*bstrMediaType* \[ En\]
</dt> <dd>

**System.String que** es el tipo de medio especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Interfaz **WMPLib.IWMPPlaylist** para la lista de reproducción recuperada.

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

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





