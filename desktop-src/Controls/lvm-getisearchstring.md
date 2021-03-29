---
title: Mensaje de LVM_GETISEARCHSTRING (commctrl. h)
description: Recupera la cadena de búsqueda incremental de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro GetISearchString de ListView.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- LVM_GETISEARCHSTRING controles de mensajes de Windows
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
ms.openlocfilehash: 9040cf96c5c483b29764b1ccfb67e0e4fff3f897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492418"
---
# <a name="lvm_getisearchstring-message"></a>\_Mensaje GETISEARCHSTRING LVM

Recupera la cadena de búsqueda incremental de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetISearchString de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un búfer que recibe la cadena de búsqueda incremental. Para recuperar solo la longitud de la cadena, establezca *lParam* en **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de caracteres de la cadena de búsqueda incremental, sin incluir el carácter nulo de terminación, o bien cero si el control de vista de lista no está en modo de búsqueda incremental.

## <a name="remarks"></a>Observaciones

**Advertencia de seguridad:** El uso incorrecto de este mensaje podría poner en peligro la seguridad del programa. Este mensaje no proporciona una manera de conocer el tamaño del búfer. Si usa este mensaje, llame primero al mensaje que pasa **null** en *lParam*; esto devuelve el número de caracteres, excluidos los **valores NULL** necesarios. A continuación, llame al mensaje una segunda vez para recuperar la cadena. Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.

La *cadena de búsqueda incremental* es la secuencia de caracteres que el usuario escribe mientras la vista de lista tiene el foco de entrada. Cada vez que el usuario escribe un carácter, el sistema anexa el carácter a la cadena de búsqueda y, a continuación, busca un elemento coincidente. Si el sistema encuentra una coincidencia, selecciona el elemento y, si es necesario, lo desplaza a la vista.

Un período de tiempo de espera está asociado a cada uno de los caracteres que el usuario escribe. Si el período de tiempo de espera transcurre antes de que el usuario escribe otro carácter, se restablece la cadena de búsqueda incremental.

Asegúrese de que el búfer sea lo suficientemente grande para contener la cadena y el carácter nulo de terminación. Si es demasiado pequeño, se producirá un error de página no válido inmediato.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ GETISEARCHSTRINGW** (Unicode) y **\_ GETISEARCHSTRINGA de LVM** (ANSI)<br/> |



 

 





