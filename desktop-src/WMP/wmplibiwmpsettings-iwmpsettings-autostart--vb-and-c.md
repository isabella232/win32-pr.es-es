---
title: Propiedad IWMPSettings de autoStart
description: La propiedad autoStart obtiene o establece un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- propiedades de inicio automático de Windows Media Player
- propiedad autoStart Media Player Windows, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad autoStart
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
ms.openlocfilehash: aaf6c1fb43107df11462737286e26fa7801360d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718880"
---
# <a name="iwmpsettingsautostart-property"></a>IWMPSettings:: autoStart (propiedad)

La propiedad **autoStart** obtiene o establece un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a>Valor de propiedad

Valor **System. Boolean** que indica si el elemento multimedia actual comienza a reproducirse automáticamente. El valor predeterminado es **true**.

## <a name="remarks"></a>Observaciones

Si **autoStart** se establece en **true**, el elemento multimedia comenzará a reproducirse cuando se establezca **AxWindowsMediaPlayer. URL**, **AxWindowsMediaPlayer. currentPlaylist** o **AxWindowsMediaPlayer. currentMedia** . De lo contrario, el elemento multimedia no comenzará a reproducirse hasta que se llame al método **IWMPControls. Play** .

A menos que establezca **autoStart** en **true** inmediatamente antes de especificar un elemento multimedia, no debe confiar en este valor como sustituto para usar el método **IWMPControls. Play** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AxWindowsMediaPlayer. currentMedia (VB y C#)**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. currentPlaylist (VB y C#)**](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. URL (VB y C#)**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPControls. Play (VB y C#)**](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





