---
title: LVM_ENABLEGROUPVIEW mensaje (Commctrl.h)
description: Habilita o deshabilita si los elementos de un control de vista de lista se muestran como un grupo.
ms.assetid: 783a5e23-d1cb-4523-a6d2-b2cf93fa7f62
keywords:
- LVM_ENABLEGROUPVIEW controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_ENABLEGROUPVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848bf348a35ee171f23e499464b65c847b67f920c53175fcf920d56e7e30fb90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698785"
---
# <a name="lvm_enablegroupview-message"></a>Mensaje \_ ENABLEGROUPVIEW de LVM

Habilita o deshabilita si los elementos de un control de vista de lista se muestran como un grupo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Un **valor BOOL** que indica si se debe habilitar un control de vista de lista para agrupar los elementos mostrados. Use **TRUE** para habilitar la agrupación, **FALSE** para deshabilitarla. </dd> <dt>

*lParam* 
</dt> <dd>Debe ser **NULL.**</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                       | Descripción                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>  | La capacidad de mostrar elementos de vista de lista como un grupo ya está habilitada o deshabilitada.<br/> |
| <dl> <dt>**1**</dt> </dl>  | El estado del control ha cambiado correctamente.<br/>                                |
| <dl> <dt>**-1**</dt> </dl> | Error en la operación.<br/>                                                             |



 

## <a name="remarks"></a>Comentarios

**LVM \_ ENABLEGROUPVIEW no** se admite en el [**estilo \_ OWNERDATA de LVS.**](list-view-window-styles.md)

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6.0. Para obtener más información sobre los manifiestos, vea [Habilitar estilos visuales.](cookbook-overview.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





