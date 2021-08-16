---
title: CCM_DPISCALE mensaje (Commctrl.h)
description: Habilita el escalado automático de puntos altos por pulgada (ppp) en controles Tree-View, controles List-View, controles ComboBoxEx, controles Header, Botones, Controles de barra de herramientas, Controles de animación y Listas de imágenes.
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- CCM_DPISCALE controles de Windows mensaje
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
ms.openlocfilehash: e7e72cb8ac3acf413e4381580a4ecf38a4f5bd4b2f5b03d6cff7d7abb85c1f0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320255"
---
# <a name="ccm_dpiscale-message"></a>Mensaje \_ DE CCM PPPSCALE

Habilita el escalado automático de puntos altos por pulgada (ppp) en los controles [Tree-View,](tree-view-controls.md) [List-View,](list-view-control-reference.md) [ComboBoxEx,](comboboxex-controls.md) [Header controls](header-controls.md), [Buttons](buttons.md), [Toolbar controls](toolbar-controls-overview.md), [Animation controls](animation-control-overview.md)y [Image Lists](image-lists.md).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Establezca en **TRUE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="remarks"></a>Comentarios

inicio rápido y [la barra de](/windows/desktop/shell/taskbar) tareas no deben especificar un escalado de ppp, porque las imágenes ya se han escalado.

Cualquier control que use una lista de imágenes creada con la métrica SmallIcon no debe escalar sus iconos.

> [!Note]  
> Para usar esta API, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

