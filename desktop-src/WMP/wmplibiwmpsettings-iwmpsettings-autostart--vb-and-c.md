---
title: Propiedad autoStart de IWMPSettings
description: La propiedad autoStart obtiene o establece un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- propiedad autoStart Reproductor de Windows Media
- Propiedad autoStart Reproductor de Windows Media , interfaz IWMPSettings
- Interfaz IWMPSettings Reproductor de Windows Media , propiedad autoStart
topic_type:
- apiref
api_name:
- IWMPSettings.autoStart
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7be64a030bbfe8abbd81830a7638094cd3da93939f3184ad3a4cfca0063c9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568472"
---
# <a name="iwmpsettingsautostart-property"></a>Propiedad IWMPSettings::autoStart

La **propiedad autoStart** obtiene o establece un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a>Valor de propiedad

Valor **System.Boolean** que indica si el elemento multimedia actual comienza a reproducirse automáticamente. El valor predeterminado es **true**.

## <a name="remarks"></a>Comentarios

Si **autoStart** se establece en **true,** el elemento multimedia comenzará a reproducirse cuando se establezca **AxWindowsMediaPlayer.URL,** **AxWindowsMediaPlayer.currentPlaylist** o **AxWindowsMediaPlayer.currentMedia.** De lo contrario, el elemento multimedia no se iniciará hasta que se llame al método **IWMPControls.play.**

A menos que **establezca autoStart** en **true** inmediatamente antes de especificar un elemento multimedia, no debe confiar en esta configuración como sustituto del uso del **método IWMPControls.play.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**AxWindowsMediaPlayer.currentMedia (VB y C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.currentPlaylist (VB y C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer.URL (VB y C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPControls.play (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





