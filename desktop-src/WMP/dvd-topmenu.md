---
title: DVD. webmenu (método)
description: El método de menú de menús detiene la reproducción del título y muestra el menú superior (o raíz) del título actual.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- método de menú de menús Media Player Windows
- método de menú de menús Windows Media Player, clase de DVD
- Clase de DVD Windows Media Player, método de menú de menús
topic_type:
- apiref
api_name:
- DVD.topMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be2b0fdafb10039b24f1d77e65f4b105889da85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491272"
---
# <a name="dvdtopmenu-method"></a>DVD. webmenu (método)

El método de **menú de menús** detiene la reproducción del título y muestra el menú superior (o raíz) del título actual.

## <a name="syntax"></a>Sintaxis


```JScript
DVD.topMenu()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cada DVD se crea de forma diferente. El DVD debe contener un menú para que este método funcione. Algunos DVDs se crean para que los métodos de **menú** y **titleMenu** abran el mismo menú. El método de **menú de menús** normalmente invoca el menú superior (o raíz), pero puede invocar el menú de título en su lugar, si no hay ningún menú raíz disponible.

**Windows Media Player 10 Mobile:** Este método siempre se realiza correctamente, pero no realiza la operación deseada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Versión<br/>                  | Windows Media Player para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de DVD**](dvd-object.md)
</dt> <dt>

[**DVD. titleMenu**](dvd-titlemenu.md)
</dt> </dl>

 

 





