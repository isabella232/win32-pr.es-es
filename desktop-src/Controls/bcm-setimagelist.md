---
title: Mensaje de BCM_SETIMAGELIST (commctrl. h)
description: Asigna una lista de imágenes a un control de botón. Puede enviar este mensaje explícitamente o utilizar la \_ macro Button SetImageList.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- BCM_SETIMAGELIST controles de mensajes de Windows
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
ms.openlocfilehash: c9bdf29735958f3c40af544bca4b946458df8431
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079274"
---
# <a name="bcm_setimagelist-message"></a>\_Mensaje SETIMAGELIST de BCM

Asigna una lista de imágenes a un control de botón. Puede enviar este mensaje explícitamente o utilizar la macro [**Button \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**de \_ ImageList de botón**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que contiene información de la lista de imágenes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje se realiza correctamente, devuelve **true**. En caso contrario, devuelve **false**.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

La lista de imágenes a la que se hace referencia en el miembro **himl** de la estructura [**\_ ImageList del botón**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) debe contener una sola imagen que se usará para todos los Estados o imágenes individuales para cada Estado. Los siguientes Estados se definen en vssym32. h.

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

Tenga en cuenta que PBS \_ STYLUSHOT se usa solo en Tablet PC.

Cada valor es un índice de la imagen correspondiente en la lista de imágenes. Si solo hay una imagen, se utiliza para todos los Estados. Si la lista de imágenes contiene más de una imagen, cada índice corresponde a un estado del botón. Si no se proporciona una imagen para cada Estado, no se dibuja nada para esos Estados sin imágenes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





