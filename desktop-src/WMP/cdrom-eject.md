---
title: Método Cdrom.eject
description: El método de expulsión expulsa el CD o DVD de la unidad. | Método Cdrom.eject
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- método de Reproductor de Windows Media
- método de Reproductor de Windows Media , clase Cdrom
- Método de expulsión Reproductor de Windows Media cdrom
topic_type:
- apiref
api_name:
- Cdrom.eject
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bd1c5a7a79c2a9b76b3a7a1997c43713fe0f3c1ae28e635a235feb82d214ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997685"
---
# <a name="cdromeject-method"></a>Método Cdrom.eject

El **método de** expulsión expulsa el CD o DVD de la unidad.

## <a name="syntax"></a>Sintaxis


```JScript
Cdrom.eject()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si la puerta de la unidad está abierta, este método cierra la puerta.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento de botón HTML que usa *Cdrom*. **para** abrir la puerta de la unidad que tiene el índice cero del especificador de unidad. El **objeto Player** se creó con id. = "Player".


```JScript
<INPUT TYPE = "BUTTON"
       NAME = "EJECTBUTTON"
       VALUE = "EJECT"
       OnClick =  "Player.cdromCollection.item(0).eject()"
>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Versión<br/>                  | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Cdrom (objeto)**](cdrom-object.md)
</dt> <dt>

[**Player.playState**](player-playstate.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





