---
title: CB_GETCUEBANNER mensaje (Winuser.h)
description: Obtiene el texto del banner de la indicación que se muestra en el control de edición de un cuadro combinado. Envíe este mensaje explícitamente o mediante la macro \_ ComboBox GetCueBannerText.
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- CB_GETCUEBANNER controles de Windows mensaje
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81ddcd8123f28317726f412255f440d47f53310aa035ab34d25190658550163
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089275"
---
# <a name="cb_getcuebanner-message"></a>Mensaje \_ GETCUEBANNER de CB

Obtiene el texto del banner de la indicación que se muestra en el control de edición de un cuadro combinado. Envíe este mensaje explícitamente o mediante la [**macro \_ ComboBox GetCueBannerText.**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Puntero a un búfer de cadena Unicode que recibe el texto del banner de la indicación. La aplicación que realiza la llamada es responsable de asignar la memoria para el búfer. El tamaño del búfer debe ser igual a la longitud de la cadena de banner de indicación en **WCHARs,** más 1 para el WCHAR **NULL** **final.**

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Tamaño del búfer al que apunta *lpcwText* en **WCHARs.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 1 si se realiza correctamente o un valor de error en caso contrario.

Si no hay texto de banner de indicación para obtener, el valor devuelto es 0. Si la aplicación que realiza la llamada no puede asignar un búfer o establece *lParam* antes de enviar este mensaje, puede producirse un comportamiento no definido y es posible que el valor devuelto no sea confiable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Características del cuadro combinado](combo-box-features.md)
</dt> </dl>

 

 





