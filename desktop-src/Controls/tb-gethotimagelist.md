---
title: TB_GETHOTIMAGELIST mensaje (Commctrl.h)
description: Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar botones de acceso rápido.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- TB_GETHOTIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e19c1f3989b0d749a9c663d00b5fb7b54d67fc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166826"
---
# <a name="tb_gethotimagelist-message"></a>Mensaje \_ DE TB GETHOTIMAGELIST

Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar botones de acceso rápido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la lista de imágenes que el control usa para mostrar botones de acceso rápido, o **NULL** si no se establece ninguna lista de imágenes de acceso rápido.

## <a name="remarks"></a>Observaciones

Un botón está en caliente cuando el cursor está sobre él. Los controles de barra de herramientas deben tener el estilo [**TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) o [**TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) para tener elementos de acceso rápido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





