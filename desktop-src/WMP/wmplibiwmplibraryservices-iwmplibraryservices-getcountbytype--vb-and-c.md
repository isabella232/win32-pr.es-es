---
title: Método IWMPLibraryServices getCountByType
description: El método getCountByType devuelve el recuento de bibliotecas disponibles de un tipo especificado.
ms.assetid: 75f22e21-fbaf-45dc-b64f-1f687a3cf241
keywords:
- Método getCountByType Reproductor de Windows Media
- Método getCountByType Reproductor de Windows Media , interfaz IWMPLibraryServices
- Interfaz IWMPLibraryServices Reproductor de Windows Media método , getCountByType
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473306"
---
# <a name="iwmplibraryservicesgetcountbytype-method"></a>IWMPLibraryServices::getCountByType (método)

El **método getCountByType** devuelve el recuento de bibliotecas disponibles de un tipo especificado.

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

*wmplt* \[ En\]
</dt> <dd>

Valor de la **enumeración WMPLib.WMPLibraryType** que especifica el tipo de biblioteca que se debe contar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**System.Int32 que** es el recuento de bibliotecas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media 11.<br/>                                                                                    |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPLibraryServices (VB y C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





