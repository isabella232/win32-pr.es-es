---
title: Settings. Volume
description: La propiedad Volume especifica o recupera el volumen actual.
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- Configuración. volumen Windows Media Player
topic_type:
- apiref
api_name:
- Settings.volume
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f5ec4299bf33ed16143eec8570b65c548599e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653570"
---
# <a name="settingsvolume"></a>Settings. Volume

La propiedad **Volume** especifica o recupera el volumen actual.

## <a name="syntax"></a>Sintaxis

Player. Settings. Volume

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de lectura y escritura (**largo**) que oscila entre 0 y 100.

## <a name="remarks"></a>Observaciones

Cero no especifica ningún volumen y 100 especifica el volumen completo. Si no se especifica ningún valor para esta propiedad, el valor predeterminado es la última configuración de volumen establecida para el reproductor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de configuración**](settings-object.md)
</dt> </dl>

 

 





