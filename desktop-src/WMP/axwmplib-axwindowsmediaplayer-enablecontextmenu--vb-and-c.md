---
title: Propiedad AxWindowsMediaPlayer.enableContextMenu
description: La propiedad enableContextMenu obtiene o establece un valor que indica si se debe habilitar el menú contextual, que aparece cuando se hace clic en el botón derecho del mouse.
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- Propiedad enableContextMenu Reproductor de Windows Media
- Propiedad enableContextMenu Reproductor de Windows Media , clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Reproductor de Windows Media , propiedad enableContextMenu
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.enableContextMenu
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5603762ec9823f7e9896c5c22c1dee33f2399bb02301921057f8502046bcc002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582344"
---
# <a name="axwindowsmediaplayerenablecontextmenu-property"></a>Propiedad AxWindowsMediaPlayer.enableContextMenu

La propiedad enableContextMenu obtiene o establece un valor que indica si se debe habilitar el menú contextual, que aparece cuando se hace clic en el botón derecho del mouse.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean enableContextMenu {get; set;}
```


```VB

Public Property enableContextMenu As System.Boolean
```





## <a name="property-value"></a>Valor de propiedad

Valor System.Boolean que indica si se debe habilitar el menú contextual. El valor predeterminado es true.

## <a name="remarks"></a>Comentarios

Durante la reproducción a pantalla completa, Reproductor de Windows Media el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a "none".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Reproductor de Windows Media serie 9 o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





