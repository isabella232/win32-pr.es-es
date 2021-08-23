---
title: LVM_GETISEARCHSTRING mensaje (Commctrl.h)
description: Recupera la cadena de búsqueda incremental de un control list-view. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView GetISearchString.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- LVM_GETISEARCHSTRING controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETISEARCHSTRING
- LVM_GETISEARCHSTRINGA
- LVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d612a6c1ba303bc08b6d5067ccb4dd3802354456159e3aea4120bd122348e74f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540825"
---
# <a name="lvm_getisearchstring-message"></a>Mensaje \_ GETISEARCHSTRING de LVM

Recupera la cadena de búsqueda incremental de un control list-view. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView GetISearchString.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer que recibe la cadena de búsqueda incremental. Para recuperar simplemente la longitud de la cadena, establezca *lParam* en **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de caracteres de la cadena de búsqueda incremental, sin incluir el carácter NULL final, o cero si el control de vista de lista no está en modo de búsqueda incremental.

## <a name="remarks"></a>Comentarios

**Advertencia de seguridad:** El uso incorrecto de este mensaje podría poner en peligro la seguridad del programa. Este mensaje no proporciona una manera de conocer el tamaño del búfer. Si usa este mensaje, llame primero al mensaje que pasa **NULL** en *lParam*, lo que devuelve el número de caracteres, excepto **NULL** que son necesarios. A continuación, llame al mensaje una segunda vez para recuperar la cadena. Debe revisar las [Consideraciones de seguridad: Controles de Windows Microsoft](sec-comctls.md) antes de continuar.

La *cadena de búsqueda incremental* es la secuencia de caracteres que el usuario tipos mientras la vista de lista tiene el foco de entrada. Cada vez que el usuario tipos un carácter, el sistema anexa el carácter a la cadena de búsqueda y, a continuación, busca un elemento correspondiente. Si el sistema encuentra una coincidencia, selecciona el elemento y, si es necesario, lo desplaza a la vista.

Se asocia un período de tiempo de espera a cada carácter que el usuario tipos. Si el período de tiempo de espera transcurre antes de que el usuario tipos otro carácter, se restablece la cadena de búsqueda incremental.

Asegúrese de que el búfer es lo suficientemente grande como para contener la cadena y el carácter NULL final. Si es demasiado pequeño, se produciría un error de página no válido inmediato.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ GETISEARCHSTRINGW** (Unicode) y **LVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 





