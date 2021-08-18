---
title: Configuración.setMode (método)
description: El método setMode establece varios modos en activo o inactivo.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- Método setMode Reproductor de Windows Media
- Método setMode Reproductor de Windows Media , Configuración clase
- Configuración clase Reproductor de Windows Media método , setMode
topic_type:
- apiref
api_name:
- Settings.setMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f504fe429dddf1b3db191545e2f34a3605a8fc390346c8f00afe8c3d005f0277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995325"
---
# <a name="settingssetmode-method"></a>Configuración.setMode (método)

El **método setMode** establece varios modos en activo o inactivo.

## <a name="syntax"></a>Sintaxis


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*modeName* \[ En\]
</dt> <dd>

**Cadena** que especifica el nombre del modo que se va a cambiar, que contiene uno de los valores siguientes.



| String     | Descripción                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| autoRewind | Modo que indica si las pistas se reboban al principio después de reproducir hasta el final. El estado predeterminado es true.                                                  |
| bucle       | Modo que indica si la secuencia de pistas se repite a sí misma. El estado predeterminado es false.                                                                            |
| showFrame  | Modo que indica si el fotograma clave de vídeo más cercano se muestra en la posición actual cuando no se reproduce. El estado predeterminado es false. No tiene ningún efecto en las pistas de audio. |
| shuffle    | Modo que indica si las pistas se reproducen en orden aleatorio. El estado predeterminado es false.                                                                            |



 

</dd> <dt>

*state* \[ En\]
</dt> <dd>

**Valor** booleano que especifica si el nuevo modo especificado está activo o no.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cuando el modo showFrame está activo, el reproductor debe acceder al contenido de la pista para recuperar el fotograma de vídeo. Debido a las consideraciones de ancho de banda, use este modo con precaución al reproducir contenido no local.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Para los modos de bucle y orden aleatorio, Reproductor de Windows Media versión 7.0 o posterior. Para los modos autoRewind y showFrame, Reproductor de Windows Media serie 9 o posterior.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración Objeto**](settings-object.md)
</dt> <dt>

[**Configuración.getMode**](settings-getmode.md)
</dt> </dl>

 

 





