---
title: Configuración.baseURL
description: La propiedad baseURL especifica o recupera la dirección URL base usada para la resolución de rutas de acceso relativas con comandos de script de dirección URL que se incrustan en elementos multimedia.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- Configuración.baseURL Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Settings.baseURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e06275a3028df6b90d25665e11aab3c2a0961dfa6c525cde0636434f06986b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995385"
---
# <a name="settingsbaseurl"></a>Configuración.baseURL

La **propiedad baseURL** especifica o recupera la dirección URL base usada para la resolución de rutas de acceso relativas con comandos de script de dirección URL que se incrustan en elementos multimedia.

## <a name="syntax"></a>Syntax

player.settings.baseURL

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de lectura y **escritura.**

## <a name="remarks"></a>Comentarios

Esta propiedad especifica la dirección URL HTTP base que el evento **ScriptCommand** pasa como parámetro de comando. La dirección URL base se concatena con la dirección URL relativa como se muestra a continuación:

1.  Se agrega una barra diagonal final (/) al valor de la **propiedad baseURL.**
2.  Se eliminan de la dirección URL relativa un punto inicial, una barra diagonal o una barra diagonal (., \\ y /).
3.  La dirección URL relativa se agrega al final de la dirección URL base.
4.  Todas las barras diagonales de la dirección URL completa resultante apuntan en la misma dirección (convertida a barras diagonales o hacia atrás) en función de la dirección del primer carácter de barra diagonal encontrado en la nueva dirección URL.

**Nota**

El control player no admite el uso de dos puntos (..) en la dirección URL relativa para indicar el elemento primario de la ubicación actual.

**Reproductor de Windows Media 10 Mobile:** esta propiedad es de solo lectura y siempre devuelve una cadena vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Evento Player.ScriptCommand**](player-player-scriptcommand.md)
</dt> <dt>

[**Configuración Objeto**](settings-object.md)
</dt> </dl>

 

 





