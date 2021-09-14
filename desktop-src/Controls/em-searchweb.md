---
title: EM_SEARCHWEB mensaje (Commctrl.h)
description: Abre el explorador y realiza una búsqueda web con el texto seleccionado como término de búsqueda.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- EM_SEARCHWEB controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SEARCHWEB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e83c18db47d18648797ee3d58fe12567af941b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062137"
---
# <a name="em_searchweb-message"></a>EM \_ SEARCHWeb message

Abre el explorador y realiza una búsqueda web con el texto seleccionado como término de búsqueda.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Si la característica "Buscar en la web" está deshabilitada mediante el mensaje [**EM \_ ENABLESEARCHWEB,**](em-enablesearchweb.md) este mensaje no tiene ningún efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio 1809 \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2019 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ ENABLESEARCHWEB**](em-enablesearchweb.md)
</dt> </dl>

 

 





