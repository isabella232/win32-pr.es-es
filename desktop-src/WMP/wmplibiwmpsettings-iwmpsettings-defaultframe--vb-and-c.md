---
title: Propiedad defaultFrame de IWMPSettings
description: La propiedad defaultFrame obtiene o establece el nombre del marco utilizado para mostrar una dirección URL que se recibe en un evento AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- propiedad defaultFrame Reproductor de Windows Media
- Propiedad defaultFrame Reproductor de Windows Media , interfaz IWMPSettings
- Interfaz IWMPSettings Reproductor de Windows Media , propiedad defaultFrame
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39352b2c49bfdcd50f3e5c74d88a9fafef6752034dbd220cda3bb34dc0ed5de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053443"
---
# <a name="iwmpsettingsdefaultframe-property"></a>Propiedad IWMPSettings::d efaultFrame

La **propiedad defaultFrame** obtiene o establece el nombre del marco utilizado para mostrar una dirección URL que se recibe en un evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent.**

## <a name="syntax"></a>Syntax


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a>Valor de propiedad

**System.String que** es el valor del atributo name del elemento **FRAME de** destino.

## <a name="remarks"></a>Comentarios

Si se especifica un marco de destino en el propio evento **\_ \_ ScriptCommandEvent de WMPOCXEvents,** esta propiedad se omite.

Esta propiedad se omite cuando se usa el applet java de Netscape Navigator. En Netscape Navigator, cada comando de script de dirección URL recibido mostrará la dirección URL en una nueva ventana del explorador, independientemente del valor **de defaultFrame**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Evento AxWindowsMediaPlayer.ScriptCommand (VB y C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interfaz IWMPSettings (VB y C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





