---
title: Configuración.volume
description: La propiedad volume especifica o recupera el volumen actual.
ms.assetid: 60143eff-3a34-43eb-a86d-641c2a5cfc01
keywords:
- Configuración.volume Reproductor de Windows Media
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
ms.openlocfilehash: 1c02952426a78323421fd779b253136c1777d509141d51b590b9db40c4d077a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002215"
---
# <a name="settingsvolume"></a>Configuración.volume

La **propiedad** volume especifica o recupera el volumen actual.

## <a name="syntax"></a>Syntax

player.settings.volume

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de lectura y **escritura** **(long)** que va de 0 a 100.

## <a name="remarks"></a>Comentarios

Cero especifica que no hay volumen y 100 especifica el volumen completo. Si no se especifica ningún valor para esta propiedad, el valor predeterminado es la última configuración de volumen establecida para el reproductor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración Objeto**](settings-object.md)
</dt> </dl>

 

 





