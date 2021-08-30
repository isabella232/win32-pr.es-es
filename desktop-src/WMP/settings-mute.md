---
title: Configuración.mute
description: La propiedad mute especifica y recupera un valor que indica si el audio está silenciado.
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- Configuración.mute Reproductor de Windows Media
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
ms.openlocfilehash: 26c3a6d510f2b5906ea604a783f59b6246ac8b302a2a77d8941237361ee888eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002395"
---
# <a name="settingsmute"></a>Configuración.mute

La **propiedad mute** especifica y recupera un valor que indica si el audio está silenciado.

## <a name="syntax"></a>Syntax

player.settings.mute

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un booleano de lectura **y escritura.**



| Value | Descripción                  |
|-------|------------------------------|
| true  | El audio está silenciado.              |
| false | Predeterminada. El audio no está silenciado. |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento HTML CHECKBOX que permite al usuario silenciar y desactivar el audio. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración Objeto**](settings-object.md)
</dt> </dl>

 

 





