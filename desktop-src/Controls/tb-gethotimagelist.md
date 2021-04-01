---
title: Mensaje de TB_GETHOTIMAGELIST (commctrl. h)
description: Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar los botones de acceso rápido.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- TB_GETHOTIMAGELIST controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150402"
---
# <a name="tb_gethotimagelist-message"></a>\_Mensaje GETHOTIMAGELIST TB

Recupera la lista de imágenes que usa un control de barra de herramientas para mostrar los botones de acceso rápido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de la lista de imágenes que utiliza el control para mostrar los botones de acceso rápido, o **null** si no se ha establecido ninguna lista de imágenes activas.

## <a name="remarks"></a>Observaciones

Un botón está activo cuando el cursor se sitúa sobre él. Los controles de barra de herramientas deben tener el estilo de [**\_ lista**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ plano**](toolbar-control-and-button-styles.md) o TBSTYLE para tener elementos activos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





