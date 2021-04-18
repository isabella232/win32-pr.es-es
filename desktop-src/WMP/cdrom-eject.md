---
title: CDROM. EJECT (método)
description: El método EJECT expulsa el CD o DVD de la unidad. | CDROM. EJECT (método)
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- método EJECT Media Player de Windows
- método EJECT Media Player de Windows, clase CDROM
- Clase CDROM Windows Media Player, método EJECT
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
ms.openlocfilehash: 78326ca57dcf097344fc073681fae772222ea9ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698078"
---
# <a name="cdromeject-method"></a>CDROM. EJECT (método)

El método **EJECT** expulsa el CD o DVD de la unidad.

## <a name="syntax"></a>Sintaxis


```JScript
Cdrom.eject()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la puerta de la unidad está abierta, este método cierra la puerta.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se crea un elemento de botón HTML que usa *CDROM*. **expulsar** para abrir la puerta de la unidad que tiene el especificador de unidad index cero. El objeto **Player** se creó con ID = "Player".


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Versión<br/>                  | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDROM (objeto)**](cdrom-object.md)
</dt> <dt>

[**Player. playState**](player-playstate.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





