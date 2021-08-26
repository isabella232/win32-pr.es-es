---
title: Configuración.invokeURLs
description: La propiedad invokeURLs especifica o recupera un valor que indica si los eventos de dirección URL deben iniciar un explorador web.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Configuración.invokeURLs Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Settings.invokeURLs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75de25c5b4a18b6d53423657dc7180fe58cb095f3244800c2c42593d1d450e7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002407"
---
# <a name="settingsinvokeurls"></a>Configuración.invokeURLs

La **propiedad invokeURLs** especifica o recupera un valor que indica si los eventos de dirección URL deben iniciar un explorador web.

## <a name="syntax"></a>Syntax

player.settings.invokeURLs

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un booleano de lectura **y escritura.**



| Value | Descripción                                  |
|-------|----------------------------------------------|
| true  | Predeterminada. Los eventos de dirección URL deben iniciar un explorador. |
| false | Los eventos de dirección URL no deben iniciar un explorador.      |



 

## <a name="remarks"></a>Comentarios

Los archivos multimedia pueden contener direcciones URL. Cuando se envía una dirección URL al control Reproductor de Windows Media, se pasa primero al controlador de eventos **ScriptCommand** independientemente del valor de **invokeURLs**. Una vez que se cierre **ScriptCommand,** Reproductor de Windows Media **invokeURLs** para determinar si se debe iniciar el explorador de Internet predeterminado con la dirección URL. Puede mostrar direcciones URL de forma selectiva si las comprueba en **ScriptCommand** y establece **invokeURLs** como desee.

**Reproductor de Windows Media 10 Mobile:** esta propiedad solo acepta o devuelve false.

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

 

 





