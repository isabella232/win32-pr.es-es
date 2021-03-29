---
title: Mensaje de EM_GETRECT (Winuser. h)
description: Obtiene el rectángulo de formato de un control de edición.
ms.assetid: eef0150d-9b7a-4247-acbf-6fea2efd1dc3
keywords:
- EM_GETRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_GETRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8192fd4c3aa7fbe953a36217f6b1408f055d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905311"
---
# <a name="em_getrect-message"></a>\_Mensaje GETRECT em

Obtiene el [rectángulo de formato](about-edit-controls.md) de un control de edición. El rectángulo de formato es el rectángulo de limitación en el que el control dibuja el texto. El rectángulo de limitación es independiente del tamaño de la ventana de control de edición. Puede enviar este mensaje a un control de edición o a un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recibe el rectángulo de formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto no es significativo.

## <a name="remarks"></a>Observaciones

Puede modificar el rectángulo de formato de un control de edición multilínea mediante los mensajes [**em \_ SETRECT**](em-setrect.md) y [**em \_ SETRECTNP**](em-setrectnp.md) .

En determinadas condiciones, es posible que **em \_ GETRECT** no devuelva los valores exactos que [**em \_ SETRECT**](em-setrect.md) o [**em \_ SETRECTNP**](em-setrectnp.md) set será aproximadamente correcto, pero puede estar desactivado en unos pocos píxeles.

**Edición enriquecida:** Compatible con Microsoft Rich Edit 1,0 y versiones posteriores. El rectángulo de formato no incluye la barra de selección, que es un área no marcada a la izquierda de cada párrafo. Al hacer clic en ella, la barra de selección selecciona la línea. Para obtener información sobre la compatibilidad de las versiones de edición enriquecidas con las distintas versiones del sistema, vea acerca de los [controles Rich Edit](about-rich-edit-controls.md).

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

[**\_SETRECTNP em**](em-setrectnp.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

