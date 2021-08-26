---
title: LVM_INSERTMARKHITTEST mensaje (Commctrl.h)
description: Recupera el punto de inserción más cercano a un punto especificado.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- LVM_INSERTMARKHITTEST controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250585fea10846e10238132c5150f5ace9f8e00c474e763023c36c8566fbc752
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919985"
---
# <a name="lvm_insertmarkhittest-message"></a>Mensaje \_ INSERTMARKHITTEST de LVM

Recupera el punto de inserción más cercano a un punto especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Puntero a una **estructura POINT** que contiene las coordenadas de la prueba de acceso.</dd> <dt>

*lParam* 
</dt> <dd>Puntero a una <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">estructura LVINSERTMARK</a> que especifica el punto de inserción más cercano a las coordenadas definidas por el *parámetro wParam.*</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario. **Se** devuelve FALSE si el tamaño del miembro **cbSize** de la estructura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) no es igual al tamaño real de la estructura o cuando no se aplica un punto de inserción en la vista actual.

## <a name="remarks"></a>Comentarios

Un punto de inserción solo puede aparecer si el control list-view está en la vista de iconos, la vista de icono pequeña o la vista de mosaico y no está en modo de vista de grupo.

Si los puntos de inserción no se aplican a la vista, la estructura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) contiene un -1 en el **miembro iItem.**

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





