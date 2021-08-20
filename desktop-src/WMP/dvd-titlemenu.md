---
title: Dvd.titleMenu (método)
description: El método titleMenu detiene la reproducción del título y muestra el menú título.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- método titleMenu Reproductor de Windows Media
- método titleMenu Reproductor de Windows Media , clase DVD
- Clase DE DVD Reproductor de Windows Media , método titleMenu
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
ms.openlocfilehash: 1954ea52d5a67dc502278c7f1e821a06c4e2b849dc4040e690275b6d1b0ef0bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996885"
---
# <a name="dvdtitlemenu-method"></a>Dvd.titleMenu (método)

El **método titleMenu** detiene la reproducción del título y muestra el menú título.

## <a name="syntax"></a>Sintaxis


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cada DVD se ha escrito de forma diferente. El DVD debe contener un menú para que este método funcione. Algunos DVD se han escrito para que los métodos **topMenu** y **titleMenu** abran el mismo menú. El **método titleMenu** normalmente invoca el menú de título, pero en su lugar puede invocar el menú superior, si no hay ningún menú de título disponible.

**Reproductor de Windows Media 10 Mobile:** Este método siempre se realiza correctamente, pero no realiza la operación prevista.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Versión<br/>                  | Reproductor de Windows Media para Windows XP o posterior.<br/>                           |
| Archivo DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dvd (objeto)**](dvd-object.md)
</dt> <dt>

[**DVD.topMenu**](dvd-topmenu.md)
</dt> </dl>

 

 





