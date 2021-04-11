---
title: Mensaje de CCM_DPISCALE (commctrl. h)
description: Habilita el escalado automático de puntos por pulgada (PPP) en controles Tree-View, controles de List-View, controles ComboBoxEx, controles de encabezado, botones, controles de barra de herramientas, controles de animación y listas de imágenes.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- CCM_DPISCALE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CCM_DPISCALE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef978f486f370adf9872d28e1accbacc37a6de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150565"
---
# <a name="ccm_dpiscale-message"></a>\_Mensaje DPISCALE de CCM

Habilita el ajuste de escala automático de puntos por pulgada (PPP) en [controles de vista de árbol](tree-view-controls.md), [controles de vista de lista](list-view-control-reference.md), [controles ComboBoxEx](comboboxex-controls.md), [controles de encabezado](header-controls.md), [botones](buttons.md), controles de [barra de herramientas](toolbar-controls-overview.md), controles de [animación](animation-control-overview.md)y [listas de imágenes](image-lists.md).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Establézcalo en **true**.

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto.

## <a name="remarks"></a>Observaciones

El inicio rápido y la [barra de tareas](/windows/desktop/shell/taskbar) no deben especificar un ajuste de escala de PPP, ya que las imágenes ya se han escalado.

Cualquier control que utiliza una lista de imágenes creada con la métrica SmallIcon no debe escalar sus iconos.

> [!Note]  
> Para usar esta API, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

