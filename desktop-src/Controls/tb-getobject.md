---
title: Mensaje de TB_GETOBJECT (commctrl. h)
description: Recupera IDropTarget para un control de barra de herramientas.
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- TB_GETOBJECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce923feaec893e6f4304eb0b993de33dc1fe2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150744"
---
# <a name="tb_getobject-message"></a>\_Mensaje GETOBJECT de TB

Recupera [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) para un control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la interfaz que se solicita. Este valor debe apuntar al **IID \_ IDropTarget**.

</dd> <dt>

*lParam* 
</dt> <dd>

Dirección que recibe el puntero de interfaz. Si se produce un error, se coloca un puntero **nulo** en esta dirección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** que indica si la operación se ha realizado correctamente o no.

## <a name="remarks"></a>Observaciones

La barra de herramientas usa el [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de la barra de herramientas cuando los objetos se arrastran o se colocan en él.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

