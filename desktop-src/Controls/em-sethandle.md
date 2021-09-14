---
title: EM_SETHANDLE mensaje (Winuser.h)
description: Establece el identificador de la memoria que usará un control de edición multilínea.
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- EM_SETHANDLE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062111"
---
# <a name="em_sethandle-message"></a>Mensaje \_ EM SETHANDLE

Establece el identificador de la memoria que usará un control de edición multilínea.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del búfer de memoria que el control de edición usa para almacenar el texto mostrado actualmente en lugar de asignar su propia memoria. Si es necesario, el control asigna esta memoria.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Antes de que una aplicación establece un nuevo identificador de memoria, debe enviar un mensaje [**EM \_ GETHANDLE**](em-gethandle.md) para recuperar el identificador del búfer de memoria actual y liberar esa memoria.

Un control de edición asigna automáticamente el búfer especificado siempre que necesite espacio adicional para el texto, o quita suficiente texto para que ya no se necesite espacio adicional.

Al enviar **un mensaje EM \_ SETHANDLE** se borra el búfer de deshacer [**(EM \_ CANUNDO**](em-canundo.md) devuelve cero) y la marca de modificación interna [**(EM \_ GETMODIFY**](em-getmodify.md) devuelve cero). Se vuelve a dibujar la ventana de control de edición.

**Edición enriquecte:** No se admite el mensaje **\_ EM SETHANDLE.** Los controles de edición enriquecciones no almacenan texto como una matriz simple de caracteres.

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

[**EM \_ CANUNDO**](em-canundo.md)
</dt> <dt>

[**EM \_ GETHANDLE**](em-gethandle.md)
</dt> <dt>

[**EM \_ GETMODIFY**](em-getmodify.md)
</dt> </dl>

 

 





