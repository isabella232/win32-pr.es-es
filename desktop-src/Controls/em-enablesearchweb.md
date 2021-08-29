---
title: EM_ENABLESEARCHWEB mensaje (CommCtrl.h)
description: Habilita o deshabilita la característica "Buscar en la web" y la entrada del menú contextual.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- EM_ENABLESEARCHWEB controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_ENABLESEARCHWEB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33cc76e81db5ea7c5b596e0876cad4cfabecc41b5bae62d4a666be3727b38725
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915865"
---
# <a name="em_enablesearchweb-message"></a>Mensaje \_ EM ENABLESEARCHWEB

Habilita o deshabilita la característica "Buscar en la web" y la entrada del menú contextual.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Un valor **TRUE indica** que la característica "Buscar en la web" está habilitada y un valor **false** indica que está deshabilitada.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Comentarios

Si deshabilita "Buscar en la web" con este mensaje, el mensaje [**EM \_ SEARCHWEB**](em-searchweb.md) no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio 1809 \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**EM \_ SEARCHWEB**](em-searchweb.md)
</dt> </dl>

 

 





