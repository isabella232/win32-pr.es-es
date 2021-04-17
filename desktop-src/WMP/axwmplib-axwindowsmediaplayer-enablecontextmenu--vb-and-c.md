---
title: Propiedad AxWindowsMediaPlayer. enableContextMenu
description: La propiedad enableContextMenu obtiene o establece un valor que indica si se debe habilitar el menú contextual, que aparece al hacer clic con el botón secundario del mouse.
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- propiedades de enableContextMenu Media Player de Windows
- propiedad enableContextMenu Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad enableContextMenu
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
ms.openlocfilehash: 09c705fd45b9b994863ab4f93df1c3ae10858930
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698554"
---
# <a name="axwindowsmediaplayerenablecontextmenu-property"></a>Propiedad AxWindowsMediaPlayer. enableContextMenu

La propiedad enableContextMenu obtiene o establece un valor que indica si se debe habilitar el menú contextual, que aparece al hacer clic con el botón secundario del mouse.

## <a name="syntax"></a>Sintaxis


```CSharp
public System.Boolean enableContextMenu {get; set;}
```


```VB

Public Property enableContextMenu As System.Boolean
```





## <a name="property-value"></a>Valor de propiedad

Valor System. Boolean que indica si se debe habilitar el menú contextual. El valor predeterminado es true.

## <a name="remarks"></a>Observaciones

Durante la reproducción a pantalla completa, Windows Media Player oculta el cursor del mouse cuando **enableContextMenu** es igual a false y **uiMode** es igual a "none".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                          |
| Espacio de nombres<br/> | **AxWMPLib**<br/>                                                                                                    |
| Ensamblado<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB y C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





