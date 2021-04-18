---
title: IWMPLibraryServices getCountByType, método
description: El método getCountByType devuelve el número de bibliotecas disponibles de un tipo especificado.
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- método getCountByType de Windows Media Player
- método getCountByType Windows Media Player, interfaz IWMPLibraryServices
- Interfaz IWMPLibraryServices Windows Media Player, método getCountByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbd874c06c2557102011c63ee1abb895d092656
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671595"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a>IWMPLibraryServices:: getCountByType (método)

El método **getCountByType** devuelve el número de bibliotecas disponibles de un tipo especificado.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Int32 getCountByType(
  WMPLibraryType wmplt
);
```


```VB

Public Function getCountByType( _
  ByVal wmplt As WMPLibraryType _
) As System.Int32
Implements IWMPLibraryServices.getCountByType
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*wmplt* \[ de\]
</dt> <dd>

Un valor de la enumeración **WMPLib. WMPLibraryType** que especifica el tipo de biblioteca que se va a contar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System. Int32** que es el número de bibliotecas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPLibraryServices (VB y C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





