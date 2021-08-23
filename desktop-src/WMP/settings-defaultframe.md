---
title: Configuración.defaultFrame
description: La propiedad defaultFrame especifica o recupera el nombre del marco utilizado para mostrar una dirección URL que se recibe en un evento ScriptCommand.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Configuración.defaultFrame Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0240864cd19c1a4d84c30abfc6e6b8ecb08457d26c3c660d19fc18d228b19615
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571815"
---
# <a name="settingsdefaultframe"></a>Configuración.defaultFrame

La **propiedad defaultFrame** especifica o recupera el nombre del marco utilizado para mostrar una dirección URL que se recibe en un **evento ScriptCommand.**

## <a name="syntax"></a>Syntax

player.settings.defaultFrame

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de lectura y **escritura** que corresponde al valor del atributo **name** del elemento FRAME de destino.

## <a name="remarks"></a>Comentarios

Si se especifica un marco de destino en el propio **evento ScriptCommand,** se omite esta propiedad.

Esta propiedad se omite cuando se usa el applet De Java de Netscape Navigator. En Navegador, cada comando de script de dirección URL recibido muestra la dirección URL en una nueva ventana del explorador, independientemente del valor de *Configuración*. **defaultFrame**.

**Reproductor de Windows Media 10 Mobile:** esta propiedad es de solo lectura y siempre devuelve una cadena vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Evento Player.ScriptCommand**](player-player-scriptcommand.md)
</dt> <dt>

[**Configuración Objeto**](settings-object.md)
</dt> <dt>

[**Uso del Reproductor de Windows Media con Netscape 7.1**](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





