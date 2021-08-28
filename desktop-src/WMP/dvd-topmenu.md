---
title: Método DVD.topMenu
description: El método topMenu detiene la reproducción del título y muestra el menú superior (o raíz) del título actual.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- Método topMenu Reproductor de Windows Media
- Método topMenu Reproductor de Windows Media , clase DVD
- Dvd class Reproductor de Windows Media , topMenu (método)
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
ms.openlocfilehash: e6042547d26d40c620da503836de1ec15991280b17dd066cf81d32c617e85064
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651165"
---
# <a name="dvdtopmenu-method"></a>Método DVD.topMenu

El **método topMenu** detiene la reproducción del título y muestra el menú superior (o raíz) del título actual.

## <a name="syntax"></a>Sintaxis


```JScript
DVD.topMenu()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cada DVD se ha escrito de forma diferente. El DVD debe contener un menú para que este método funcione. Algunos DVD se han escrito para que los métodos **topMenu** y **titleMenu** abran el mismo menú. El **método topMenu** normalmente invoca el menú superior (o raíz), pero puede invocar el menú de título en su lugar, si no hay ningún menú raíz disponible.

**Reproductor de Windows Media 10 Mobile:** Este método siempre se realiza correctamente, pero no realiza la operación prevista.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Versión<br/>                  | Reproductor de Windows Media para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dvd (objeto)**](dvd-object.md)
</dt> <dt>

[**DVD.titleMenu**](dvd-titlemenu.md)
</dt> </dl>

 

 





