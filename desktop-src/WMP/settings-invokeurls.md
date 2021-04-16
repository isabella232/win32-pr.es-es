---
title: Settings. invokeURLs
description: La propiedad invokeURLs especifica o recupera un valor que indica si los eventos de dirección URL deben iniciar un explorador Web.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Settings. invokeURLs Windows Media Player
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
ms.openlocfilehash: eb55bb61243e6905a51a943a26adc120511335c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649754"
---
# <a name="settingsinvokeurls"></a>Settings. invokeURLs

La propiedad **invokeURLs** especifica o recupera un valor que indica si los eventos de dirección URL deben iniciar un explorador Web.

## <a name="syntax"></a>Sintaxis

Player. Settings. invokeURLs

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **valor booleano** de lectura/escritura.



| Value | Descripción                                  |
|-------|----------------------------------------------|
| true  | Predeterminada. Los eventos de URL deben iniciar un explorador. |
| false | Los eventos de URL no deben iniciar un explorador.      |



 

## <a name="remarks"></a>Observaciones

Los archivos multimedia pueden contener direcciones URL. Cuando se envía una dirección URL al control de Media Player de Windows, se pasa primero al controlador de eventos **comando** independientemente del valor de **invokeURLs**. Después de que **comando** se cierre, Windows Media Player comprueba **invokeURLs** para determinar si se debe iniciar el explorador de Internet predeterminado con la dirección URL. Puede mostrar las direcciones URL de forma selectiva al comprobarlas en **comando** y establecer **invokeURLs** como desee.

**Windows Media Player 10 Mobile**: esta propiedad solo acepta o devuelve false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Evento Player. comando**](player-player-scriptcommand.md)
</dt> <dt>

[**Objeto de configuración**](settings-object.md)
</dt> </dl>

 

 





