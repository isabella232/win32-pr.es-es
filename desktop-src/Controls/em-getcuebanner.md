---
title: EM_GETCUEBANNER mensaje (Commctrl.h)
description: Obtiene el texto que se muestra como la indicación textual, o sugerencia, en un control de edición.
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- EM_GETCUEBANNER controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d28d4aeea5a206c74f2e6b41cee27b5073448ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062195"
---
# <a name="em_getcuebanner-message"></a>Mensaje \_ GETCUEBANNER de EM

Obtiene el texto que se muestra como la indicación textual, o sugerencia, en un control de edición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Puntero a un búfer Unicode que recibe el conjunto de texto como la indicación textual. El autor de la llamada es responsable de asignar el búfer.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Tamaño del búfer al que apunta *wParam* en **WCHARs,** incluido el **valor NULL final.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o FALSE **de** lo contrario.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Editar \_ GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





