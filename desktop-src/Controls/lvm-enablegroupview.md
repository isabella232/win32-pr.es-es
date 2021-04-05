---
title: Mensaje de LVM_ENABLEGROUPVIEW (commctrl. h)
description: Habilita o deshabilita si los elementos de un control de vista de lista se muestran como un grupo.
ms.assetid: 783a5e23-d1cb-4523-a6d2-b2cf93fa7f62
keywords:
- LVM_ENABLEGROUPVIEW controles de mensajes de Windows
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
ms.openlocfilehash: a1d546e1236fa4f0800c0353810beb5b427ba4fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078876"
---
# <a name="lvm_enablegroupview-message"></a>\_Mensaje ENABLEGROUPVIEW LVM

Habilita o deshabilita si los elementos de un control de vista de lista se muestran como un grupo.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Un **booleano** que indica si se va a habilitar un control de vista de lista para agrupar los elementos mostrados. Use **true** para habilitar la agrupación y **false** para deshabilitarla. </dd> <dt>

*lParam* 
</dt> <dd>Debe ser **null**.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                       | Descripción                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**0,1**</dt> </dl>  | La capacidad de mostrar los elementos de vista de lista como un grupo ya está habilitada o deshabilitada.<br/> |
| <dl> <dt>**1**</dt> </dl>  | El estado del control se ha cambiado correctamente.<br/>                                |
| <dl> <dt>**-1**</dt> </dl> | Error en la operación.<br/>                                                             |



 

## <a name="remarks"></a>Observaciones

**LVM \_ ENABLEGROUPVIEW** no se admite en el estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





