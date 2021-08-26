---
title: BCM_SETIMAGELIST mensaje (Commctrl.h)
description: Asigna una lista de imágenes a un control de botón. Puede enviar este mensaje explícitamente o usar la macro Button \_ SetImageList.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- BCM_SETIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- BCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f5c88020bb139c358b17386b003bfb9de9cfcd4e769b9262ed90e23f3f95e75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921565"
---
# <a name="bcm_setimagelist-message"></a>Mensaje \_ SETIMAGELIST de BCM

Asigna una lista de imágenes a un control de botón. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button SetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**\_ BUTTON IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que contiene información de lista de imágenes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, devuelve **TRUE.** De lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Comentarios

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

La lista de imágenes a la que se hace referencia en el miembro **himl** de la estructura [**BUTTON \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) debe contener una sola imagen que se usará para todos los estados o imágenes individuales para cada estado. Los estados siguientes se definen en vssym32.h.

``` syntax
enum PUSHBUTTONSTATES {
    PBS_NORMAL = 1,
    PBS_HOT = 2,
    PBS_PRESSED = 3,
    PBS_DISABLED = 4,
    PBS_DEFAULTED = 5,
    PBS_STYLUSHOT = 6,
};
```

Tenga en cuenta que PBS \_ STYLUSHOT solo se usa en equipos tableta.

Cada valor es un índice de la imagen adecuada en la lista de imágenes. Si solo hay una imagen, se usa para todos los estados. Si la lista de imágenes contiene más de una imagen, cada índice corresponde a un estado del botón. Si no se proporciona una imagen para cada estado, no se dibuja nada para esos estados sin imágenes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





