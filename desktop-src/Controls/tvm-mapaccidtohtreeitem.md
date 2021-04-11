---
title: Mensaje de TVM_MAPACCIDTOHTREEITEM (commctrl. h)
description: Asigna un identificador de accesibilidad a un HTREEITEM.
ms.assetid: f4feb7cb-2138-4930-b8ee-b9e2d4b19001
keywords:
- TVM_MAPACCIDTOHTREEITEM controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_MAPACCIDTOHTREEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b827b18387723fe4792321f7932e1abb3673466e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079110"
---
# <a name="tvm_mapaccidtohtreeitem-message"></a>\_Mensaje de MAPACCIDTOHTREEITEM TVM

Asigna un identificador de accesibilidad a un **HTREEITEM**.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>**Uint** que contiene el identificador de accesibilidad que se va a asignar a un **HTREEITEM**. </dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el **HTREEITEM** al que está asignado el identificador de accesibilidad especificado.

## <a name="remarks"></a>Observaciones

Al agregar un elemento a un control de vista de árbol, un **HTREEITEM** devuelve, que identifica de forma única el elemento.

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

[**MapAccIDToHTREEITEM de TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_mapaccidtohtreeitem)
</dt> </dl>

 

 





