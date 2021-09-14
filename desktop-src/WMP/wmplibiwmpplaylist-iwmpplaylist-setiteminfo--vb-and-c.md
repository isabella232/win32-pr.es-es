---
title: Método IWMPPlaylist setItemInfo
description: El método setItemInfo establece el valor de un atributo de la lista de reproducción actual.
ms.assetid: b3874298-8fbe-47a4-b696-cef0382aec7c
keywords:
- Método setItemInfo Reproductor de Windows Media
- Método setItemInfo Reproductor de Windows Media , interfaz IWMPPlaylist
- Interfaz IWMPPlaylist Reproductor de Windows Media método , setItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce882d050f1ce7839fe3589fced3a87d9052fec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360886"
---
# <a name="iwmpplaylistsetiteminfo-method"></a>IWMPPlaylist::setItemInfo (método)

El **método setItemInfo** establece el valor de un atributo de la lista de reproducción actual.

## <a name="syntax"></a>Sintaxis


```CSharp
public void setItemInfo(
  System.String bstrName,
  System.String bstrValue
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrName As System.String, _
  ByVal bstrValue As System.String _
)
Implements IWMPPlaylist.setItemInfo
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrName* \[ En\]
</dt> <dd>

**System.String que** es el nombre del atributo.

</dd> <dt>

*bstrValue* \[ En\]
</dt> <dd>

**System.String que** es el valor del atributo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, debe tener acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

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

[**IWMPPlaylist.getItemInfo (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





