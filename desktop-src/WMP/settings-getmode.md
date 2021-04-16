---
title: Settings. getMode (método)
description: El método getMode determina si el modo de bucle o el modo de orden aleatorio está activo.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- método getMode de Windows Media Player
- método getMode de Windows Media Player, clase de configuración
- Clase de configuración Windows Media Player, método getMode
topic_type:
- apiref
api_name:
- Settings.getMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fc3e82091200d05bb173c71f2c0e5a7d213b80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649755"
---
# <a name="settingsgetmode-method"></a>Settings. getMode (método)

El método **getMode** determina si el modo de bucle o el modo de orden aleatorio está activo.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*modeName* \[ de\]
</dt> <dd>

**Cadena** que especifica el nombre del modo en cuestión, que contiene uno de los valores siguientes.



| String     | Descripción                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| autoRewind | Las pistas se reinician al principio después de reproducirse hasta el final.                                                          |
| bucle       | La secuencia de pistas se repite.                                                                                   |
| showFrame  | El fotograma clave más cercano se muestra en la posición actual cuando no se reproduce. Este modo no es relevante para las pistas de audio. |
| shuffle    | Las pistas se reproducen en orden aleatorio.                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un valor **booleano** que indica si el modo especificado está activo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | En los modos de bucle y orden aleatorio, Windows Media Player versión 7,0 o posterior. En los modos autoRewind y showFrame, Windows Media Player 9 series o posterior.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de configuración**](settings-object.md)
</dt> <dt>

[**Settings. setMode**](settings-setmode.md)
</dt> </dl>

 

 





