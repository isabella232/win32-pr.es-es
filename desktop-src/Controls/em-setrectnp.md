---
title: EM_SETRECTNP mensaje (Winuser.h)
description: 'EM_SETRECTNP mensaje: establece el rectángulo de formato de un control de edición multilínea.'
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- EM_SETRECTNP controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETRECTNP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a8c85d4f7abd58ed3adb33ede66254c190a7bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062071"
---
# <a name="em_setrectnp-message"></a>Mensaje \_ EM SETRECTNP

Establece el [rectángulo de formato de](about-edit-controls.md) un control de edición multilínea. El **mensaje EM \_ SETRECTNP** es idéntico al mensaje [**EM \_ SETRECT,**](em-setrect.md) salvo que **EM \_ SETRECTNP** no *vuelve* a dibujar la ventana de control de edición.

El rectángulo de formato es el rectángulo delimitador en el que el control dibuja el texto. El rectángulo de limitación es independiente del tamaño de la ventana de control de edición.

Este mensaje solo lo procesan los controles de edición multilínea. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Rich Edit 3.0 y versiones posteriores:** Indica si el nuevo rectángulo contiene coordenadas absolutas o relativas. Un valor de cero indica coordenadas absolutas. Un valor de 1 indica desplazamientos relativos al rectángulo de formato actual. (Los desplazamientos pueden ser positivos o negativos).

**Editar controles:** Este parámetro no se usa y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que especifica las nuevas dimensiones del rectángulo. Si este parámetro es **NULL,** el rectángulo de formato se establece en sus valores predeterminados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

**Edición enriquecte:** Compatible con Microsoft Rich Edit 3.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [About Rich Edit Controls](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ SETRECT**](em-setrect.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

