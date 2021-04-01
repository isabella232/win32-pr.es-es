---
title: Mensaje de TVM_MAPHTREEITEMTOACCID (commctrl. h)
description: Asigna un HTREEITEM a un identificador de accesibilidad.
ms.assetid: 87ef0785-88c1-49f4-8a05-872577e16fe4
keywords:
- TVM_MAPHTREEITEMTOACCID controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_MAPHTREEITEMTOACCID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad6267c2040583917283fc444db74ddacbdabd69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150299"
---
# <a name="tvm_maphtreeitemtoaccid-message"></a>\_Mensaje de MAPHTREEITEMTOACCID TVM

Asigna un **HTREEITEM** a un identificador de accesibilidad.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>**HTREEITEM** que se asigna a un identificador de accesibilidad.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un identificador de accesibilidad.

## <a name="remarks"></a>Observaciones

Al agregar un elemento a un control de vista de árbol, se devuelve un identificador **HTREEITEM** que identifica de forma única el elemento.

> [!Note]  
> Para usar este mensaje, debe proporcionar un manifiesto que especifique Comclt32.dll versión 6,0. Para obtener más información sobre los manifiestos, vea [habilitar estilos visuales](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MapHTREEITEMtoAccID de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_maphtreeitemtoaccid)
</dt> </dl>

 

 





