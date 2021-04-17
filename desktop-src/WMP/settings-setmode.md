---
title: Settings. setMode (método)
description: El método setMode establece varios modos en activo o inactivo.
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- método setMode de Windows Media Player
- método setMode de Windows Media Player, clase de configuración
- Clase de configuración Windows Media Player, método setMode
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
ms.openlocfilehash: cf5740bf5638ce34e161414ac96eaa0fc80fcdb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653571"
---
# <a name="settingssetmode-method"></a>Settings. setMode (método)

El método **setMode** establece varios modos en activo o inactivo.

## <a name="syntax"></a>Sintaxis


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*modeName* \[ de\]
</dt> <dd>

**Cadena** que especifica el nombre del modo que se va a cambiar, que contiene uno de los valores siguientes.



| String     | Descripción                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| autoRewind | Modo que indica si las pistas se rebobinan al principio después de reproducirse hasta el final. El estado predeterminado es true.                                                  |
| bucle       | Modo que indica si la secuencia de pistas se repite. El estado predeterminado es false.                                                                            |
| showFrame  | Modo que indica si se muestra el fotograma clave de vídeo más próximo en la posición actual cuando no se reproduce. El estado predeterminado es false. No tiene ningún efecto en las pistas de audio. |
| shuffle    | Modo que indica si las pistas se reproducen en orden aleatorio. El estado predeterminado es false.                                                                            |



 

</dd> <dt>

*Estado* \[ de de\]
</dt> <dd>

**Valor booleano** que especifica si el nuevo modo especificado está activo o no.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando el modo showFrame está activo, el reproductor debe tener acceso al contenido de Track para recuperar el fotograma de vídeo. Debido a las consideraciones de ancho de banda, use este modo con precaución al reproducir contenido no local.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | En los modos de bucle y orden aleatorio, Windows Media Player versión 7,0 o posterior. En los modos autoRewind y showFrame, Windows Media Player 9 series o posterior.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de configuración**](settings-object.md)
</dt> <dt>

[**Settings. getMode**](settings-getmode.md)
</dt> </dl>

 

 





