---
title: Settings. baseURL
description: La propiedad baseURL especifica o recupera la dirección URL base que se usa para la resolución de la ruta de acceso relativa con comandos de script de dirección URL que están incrustados en elementos multimedia.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- Settings. baseURL Windows Media Player
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
ms.openlocfilehash: ed77d90c8ffadc4dd8da0951f7e6a477db3f9de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649555"
---
# <a name="settingsbaseurl"></a>Settings. baseURL

La propiedad **baseurl** especifica o recupera la dirección URL base que se usa para la resolución de la ruta de acceso relativa con comandos de script de dirección URL que están incrustados en elementos multimedia.

## <a name="syntax"></a>Sintaxis

Player. Settings. baseURL

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de lectura/escritura.

## <a name="remarks"></a>Observaciones

Esta propiedad especifica la dirección URL HTTP base que el evento **comando** pasa como parámetro de comando. La dirección URL base se concatena con la dirección URL relativa como se indica a continuación:

1.  Se agrega una barra diagonal final (/) al valor de la propiedad **baseurl** .
2.  Un punto inicial, una barra diagonal inversa o una barra diagonal (., \\ y/) se eliminan de la dirección URL relativa.
3.  La dirección URL relativa se agrega al final de la dirección URL base.
4.  Todas las barras diagonales de la dirección URL completa resultante se señalan en la misma dirección (convertida en barras diagonales o hacia delante) en función de la dirección del primer carácter de barra diagonal que se encuentre en la nueva dirección URL.

**Note**

El control Player no admite el uso de dos puntos (..) en la dirección URL relativa para indicar el elemento primario de la ubicación actual.

**Windows Media Player 10 Mobile**: esta propiedad es de solo lectura y siempre devuelve una cadena vacía.

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

 

 





