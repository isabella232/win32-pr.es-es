---
title: EM_SETRECTNP mensaje (Winuser.h)
description: 'EM_SETRECTNP mensaje: establece el rectángulo de formato de un control de edición multilínea.'
ms.assetid: 1ab497ca-023f-4c26-b92d-b441a0d7b90c
keywords:
- EM_SETRECTNP de mensajes controles de Windows
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
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085993"
---
# <a name="em_setrectnp-message"></a>Mensaje \_ DE EM SETRECTNP

Establece el [rectángulo de formato de](about-edit-controls.md) un control de edición multilínea. El **mensaje \_ EM SETRECTNP** es idéntico al mensaje [**EM \_ SETRECT,**](em-setrect.md) salvo que **EM \_ SETRECTNP** no *vuelve* a dibujar la ventana de control de edición.

El rectángulo de formato es el rectángulo de limitación en el que el control dibuja el texto. El rectángulo de limitación es independiente del tamaño de la ventana de control de edición.

Este mensaje solo se procesa mediante controles de edición multilínea. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.

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

## <a name="remarks"></a>Comentarios

**Edición enriquecte:** Compatible con Microsoft Rich Edit 3.0 y versiones posteriores. Para obtener información sobre la compatibilidad de las versiones de edición enriquecciones con las distintas versiones del sistema, vea [Acerca de los controles rich edit](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ SETRECT**](em-setrect.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**Rect**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

