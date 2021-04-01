---
title: Mensaje de EM_SETRECTNP (Winuser. h)
description: Establece el rectángulo de formato de un control de edición multilínea.
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- EM_SETRECTNP controles de mensajes de Windows
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
ms.openlocfilehash: e017bd4737c843c2452382918d71ef63345917cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996925"
---
# <a name="em_setrectnp-message"></a>\_Mensaje SETRECTNP em

Establece el [rectángulo de formato](about-edit-controls.md) de un control de edición multilínea. El **mensaje em \_ SETRECTNP** es idéntico al mensaje [**em \_ SETRECT**](em-setrect.md) , salvo que **em \_ SETRECTNP** no vuelve  a dibujar la ventana de control de edición.

El rectángulo de formato es el rectángulo de limitación en el que el control dibuja el texto. El rectángulo de limitación es independiente del tamaño de la ventana de control de edición.

Este mensaje solo lo procesan los controles de edición multilínea. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Edición enriquecida 3,0 y versiones posteriores:** Indica si el nuevo rectángulo contiene coordenadas absolutas o relativas. Un valor de cero indica coordenadas absolutas. Un valor de 1 indica desplazamientos respecto al rectángulo de formato actual. (Los desplazamientos pueden ser positivos o negativos).

**Controles de edición:** Este parámetro no se utiliza y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que especifica las nuevas dimensiones del rectángulo. Si este parámetro es **null**, el rectángulo de formato se establece en sus valores predeterminados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

**Edición enriquecida:** Compatible con Microsoft Rich Edit 3,0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**\_SETRECT em**](em-setrect.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

