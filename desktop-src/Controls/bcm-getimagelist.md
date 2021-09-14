---
title: BCM_GETIMAGELIST mensaje (Commctrl.h)
description: Obtiene la estructura BUTTON \_ IMAGELIST que describe la lista de imágenes asignada a un control de botón. Puede enviar este mensaje explícitamente o usar la \_ macro Button GetImageList.
ms.assetid: 79383758-53d4-4955-b472-befd338cbec6
keywords:
- BCM_GETIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- BCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0c28e997e23d6df63150fe2283d04be1a8c0d4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170134"
---
# <a name="bcm_getimagelist-message"></a>Mensaje \_ GETIMAGELIST de BCM

Obtiene la [**estructura BUTTON \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que describe la lista de imágenes asignada a un control de botón. Puede enviar este mensaje explícitamente o usar la macro [**\_ Button GetImageList.**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**BUTTON \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que contiene información de lista de imágenes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, devuelve **TRUE.** De lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





