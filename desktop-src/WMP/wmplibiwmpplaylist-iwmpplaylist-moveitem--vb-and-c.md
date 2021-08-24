---
title: Método moveItem de IWMPPlaylist
description: El método moveItem cambia la ubicación de un elemento multimedia en la lista de reproducción.
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- Método moveItem Reproductor de Windows Media
- Método moveItem Reproductor de Windows Media , interfaz IWMPPlaylist
- Interfaz IWMPPlaylist Reproductor de Windows Media método , moveItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.moveItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f2c4f2aa3d4478a114e405b1b40816fc1697c2c291c272aabc68db3813766d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760665"
---
# <a name="iwmpplaylistmoveitem-method"></a>IWMPPlaylist::moveItem (método)

El **método moveItem** cambia la ubicación de un elemento multimedia en la lista de reproducción.

## <a name="syntax"></a>Sintaxis


```CSharp
public void moveItem(
  System.Int32 lIndexOld,
  System.Int32 lIndexNew
);
```


```VB

Public Sub moveItem( _
  ByVal lIndexOld As System.Int32, _
  ByVal lIndexNew As System.Int32 _
)
Implements IWMPPlaylist.moveItem
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*lIndexOld* \[ En\]
</dt> <dd>

**System.Int32** que es el índice original.

</dd> <dt>

*lIndexNew* \[ En\]
</dt> <dd>

**System.Int32** que es el nuevo índice.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Todos los elementos después del elemento insertado tendrán sus números de índice aumentados en uno.

Antes de llamar a este método, debe tener acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





