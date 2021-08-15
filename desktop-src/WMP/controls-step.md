---
title: Método Controls.step
description: El método step hace que el elemento multimedia de vídeo actual congele la reproducción en el fotograma siguiente o en el fotograma anterior.
ms.assetid: f717c583-4073-45a9-b05d-7134d02724a4
keywords:
- step method Reproductor de Windows Media
- step method Reproductor de Windows Media , Clase Controls
- Clase Controls Reproductor de Windows Media , método step
topic_type:
- apiref
api_name:
- Controls.step
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4626ff80aee55ad6c22be7580a07ef2319afb6792a8c11b815d72af23b5727fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118839830"
---
# <a name="controlsstep-method"></a>Método Controls.step

El **método step** hace que el elemento multimedia de vídeo actual congele la reproducción en el fotograma siguiente o en el fotograma anterior.

## <a name="syntax"></a>Sintaxis


```JScript
Controls.step(
  frameCount
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*frameCount* \[ En\]
</dt> <dd>

**Number** ( long )**que** indica cuántos fotogramas se debe usar antes de inmovilizar. Actualmente debe establecerse en 1 o -1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Actualmente, este método solo admite los parámetros 1 o -1, por lo que solo puede ir paso a paso un fotograma a la vez.

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Controls (objeto)**](controls-object.md)
</dt> <dt>

[**Dvd (objeto)**](dvd-object.md)
</dt> </dl>

 

 





