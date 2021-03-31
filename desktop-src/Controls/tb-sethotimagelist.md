---
title: Mensaje de TB_SETHOTIMAGELIST (commctrl. h)
description: Establece la lista de imágenes que utilizará el control de barra de herramientas para mostrar los botones de acceso rápido.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- TB_SETHOTIMAGELIST controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a84c3420eaf64710ac1f8764db20d2cfc88b7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996800"
---
# <a name="tb_sethotimagelist-message"></a>\_Mensaje SETHOTIMAGELIST TB

Establece la lista de imágenes que utilizará el control de barra de herramientas para mostrar los botones de acceso rápido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la lista de imágenes que se va a establecer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador de la lista de imágenes utilizada previamente para mostrar los botones de acceso rápido, o **null** si no se ha establecido previamente ninguna lista de imágenes.

## <a name="remarks"></a>Observaciones

Un botón está activo cuando el cursor se sitúa sobre él. Los controles de barra de herramientas deben tener el estilo de [**\_ lista**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ plano**](toolbar-control-and-button-styles.md) o TBSTYLE para tener elementos activos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





