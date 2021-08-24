---
title: Método removeItem de IWMPPlaylist
description: El método removeItem quita el elemento multimedia especificado de la lista de reproducción.
ms.assetid: 8b5a4c34-863d-4963-97c8-cc5aa2223ab5
keywords:
- Método removeItem Reproductor de Windows Media
- Método removeItem Reproductor de Windows Media , interfaz IWMPPlaylist
- Interfaz IWMPPlaylist Reproductor de Windows Media , método removeItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.removeItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ea9250cc7e368699a916b4c87f419fc5b0b66001a4d7ca12afd5587a0adda7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246443"
---
# <a name="iwmpplaylistremoveitem-method"></a>IWMPPlaylist::removeItem (método)

El **método removeItem** quita el elemento multimedia especificado de la lista de reproducción.

## <a name="syntax"></a>Sintaxis


```CSharp
public void removeItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub removeItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.removeItem
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*pIWMPMedia* \[ En\]
</dt> <dd>

Interfaz **WMPLib.IWMPMedia** que representa el elemento multimedia que se quitará de la lista de reproducción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el elemento quitado es la pista que se está reproduciendo actualmente, la reproducción se detiene y el siguiente elemento de la lista de reproducción se convierte en el actual.

Si no hay ningún elemento siguiente, se usa el elemento anterior. Si no hay ningún otro elemento, la propiedad **AxWindowsMediaPlayer.currentMedia** devolverá **NULL.**

Antes de llamar a este método, debe tener acceso completo a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AxWindowsMediaPlayer.currentMedia (VB y C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPMedia (VB y C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPPlaylist (VB y C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.insertItem (VB y C#)**](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylist.Item (VB y C#)**](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





