---
title: CBEM_SETIMAGELIST mensaje (Commctrl.h)
description: Establece una lista de imágenes para un control ComboBoxEx.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- CBEM_SETIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33816abe36e2d1e1593e6365061a500d072c155b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173934"
---
# <a name="cbem_setimagelist-message"></a>Mensaje \_ SETIMAGELIST de CBEM

Establece una lista de imágenes para un control ComboBoxEx.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la lista de imágenes que se va a establecer para el control.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de la lista de imágenes previamente asociada al control o devuelve **NULL** si no se estableció previamente ninguna lista de imágenes.

## <a name="remarks"></a>Observaciones

> [!IMPORTANT]
> El alto de las imágenes de la lista de imágenes puede cambiar los requisitos de tamaño del control ComboBoxEx. Se recomienda cambiar el tamaño del control después de enviar este mensaje para asegurarse de que se muestra correctamente.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





