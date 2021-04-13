---
title: DVD. titleMenu (método)
description: El método titleMenu detiene la reproducción del título y muestra el menú de título.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- método titleMenu de Windows Media Player
- método titleMenu de Windows Media Player, clase de DVD
- Clase de DVD Windows Media Player, método titleMenu
topic_type:
- apiref
api_name:
- DVD.titleMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9351603d5307415f57610422a83d3586067bdcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359716"
---
# <a name="dvdtitlemenu-method"></a>DVD. titleMenu (método)

El método **titleMenu** detiene la reproducción del título y muestra el menú de título.

## <a name="syntax"></a>Sintaxis


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cada DVD se crea de forma diferente. El DVD debe contener un menú para que este método funcione. Algunos DVDs se crean para que los métodos de **menú** y **titleMenu** abran el mismo menú. El método **titleMenu** normalmente invoca el menú de título, pero puede invocar el menú superior en su lugar, si no hay ningún menú de título disponible.

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

[**DVD. Menu**](dvd-topmenu.md)
</dt> </dl>

 

 





