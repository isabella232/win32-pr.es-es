---
title: TB_GETOBJECT mensaje (Commctrl.h)
description: Recupera IDropTarget para un control de barra de herramientas.
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- TB_GETOBJECT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166782"
---
# <a name="tb_getobject-message"></a>Mensaje \_ GETOBJECT de TB

Recupera [**IDropTarget para un**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) control de barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la interfaz que se solicita. Este valor debe apuntar a **IID \_ IDropTarget.**

</dd> <dt>

*lParam* 
</dt> <dd>

Dirección que recibe el puntero de interfaz. Si se produce un error, se coloca un puntero **NULL** en esta dirección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT** que indica que la operación se ha hecho correctamente o no.

## <a name="remarks"></a>Observaciones

La barra de herramientas [**usa IDropTarget de**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) la barra de herramientas cuando los objetos se arrastran o se le arrastran.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

