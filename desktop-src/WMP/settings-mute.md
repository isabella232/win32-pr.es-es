---
title: Settings. MUTE
description: La propiedad MUTE especifica y recupera un valor que indica si el audio está silenciado.
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- Configuración. silenciar Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mute
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061439e9e091b2ad1cf6be49873d7e3895132b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708800"
---
# <a name="settingsmute"></a>Settings. MUTE

La propiedad **MUTE** especifica y recupera un valor que indica si el audio está silenciado.

## <a name="syntax"></a>Sintaxis

Player. Settings. MUTE

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **valor booleano** de lectura/escritura.



| Value | Descripción                  |
|-------|------------------------------|
| true  | El audio está silenciado.              |
| false | Predeterminada. Audio no silenciado. |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento CHECKBOX HTML que permite al usuario silenciar y deshacer el audio. El objeto **Player** se creó con ID = "Player".


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX"  ID = MUTE  
             onClick = "
                        /* Use the CHECKBOX state to set 
                           the mute property. */
                        Player.settings.mute = MUTE.checked;
">
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de configuración**](settings-object.md)
</dt> </dl>

 

 





