---
title: Mensaje de EM_SETHANDLE (Winuser. h)
description: Establece el identificador de la memoria que va a usar un control de edición multilínea.
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- EM_SETHANDLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8f918d056db1000c6018f55d89095a73a15109
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150917"
---
# <a name="em_sethandle-message"></a>\_Mensaje SETHANDLE em

Establece el identificador de la memoria que va a usar un control de edición multilínea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del búfer de memoria que el control de edición utiliza para almacenar el texto que se muestra actualmente en lugar de asignar su propia memoria. Si es necesario, el control reasigna esta memoria.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Antes de que una aplicación establezca un nuevo identificador de memoria, debe enviar un mensaje de [**\_ GETHANDLE em**](em-gethandle.md) para recuperar el identificador del búfer de memoria actual y liberar esa memoria.

Un control de edición reasigna automáticamente el búfer determinado cada vez que necesita espacio adicional para el texto o quita el texto suficiente para que ya no se necesite espacio adicional.

Al enviar un mensaje **\_ SETHANDLE em** se borra el búfer de deshacer (EM) y la marca de modificación interna ([**em \_ GETMODIFY**](em-getmodify.md) devuelve cero).[**\_**](em-canundo.md) Se vuelve a dibujar la ventana de control de edición.

**Edición enriquecida:** No se admite el mensaje **\_ SETHANDLE em** . Los controles Rich Edit no almacenan texto como una matriz de caracteres simple.

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

[**la \_ CANUNDO em**](em-canundo.md)
</dt> <dt>

[**GETHANDLE (EM) \_**](em-gethandle.md)
</dt> <dt>

[**\_GETMODIFY em**](em-getmodify.md)
</dt> </dl>

 

 





