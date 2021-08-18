---
title: Configuración.getMode (método)
description: El método getMode determina si el modo de bucle o el modo aleatorio está activo.
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- Método getMode Reproductor de Windows Media
- Método getMode Reproductor de Windows Media , Configuración clase
- Configuración clase Reproductor de Windows Media método , getMode
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
ms.openlocfilehash: 779c775319cbe0d6dc443b4eb99febd494db3d30fb35228b7310f8f1ae7d691d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995335"
---
# <a name="settingsgetmode-method"></a>Configuración.getMode (método)

El **método getMode** determina si el modo de bucle o el modo aleatorio está activo.

## <a name="syntax"></a>Sintaxis


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*modeName* \[ En\]
</dt> <dd>

**Cadena** que especifica el nombre del modo en cuestión, que contiene uno de los valores siguientes.



| String     | Descripción                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| autoRewind | Las pistas se reinician al principio después de reproducir hasta el final.                                                          |
| bucle       | La secuencia de pistas se repite a sí misma.                                                                                   |
| showFrame  | El fotograma clave más cercano se muestra en la posición actual cuando no se reproduce. Este modo no es relevante para las pistas de audio. |
| shuffle    | Las pistas se reproducen en orden aleatorio.                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor booleano** que indica si el modo especificado está activo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Para los modos de bucle y orden aleatorio, Reproductor de Windows Media versión 7.0 o posterior. Para los modos autoRewind y showFrame, Reproductor de Windows Media serie 9 o posterior.<br/> |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración Objeto**](settings-object.md)
</dt> <dt>

[**Configuración.setMode**](settings-setmode.md)
</dt> </dl>

 

 





