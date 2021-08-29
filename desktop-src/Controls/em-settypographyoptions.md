---
title: EM_SETTYPOGRAPHYOPTIONS mensaje (Richedit.h)
description: Establece el estado actual de las opciones de tipografía de un control de edición enriquecido.
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- EM_SETTYPOGRAPHYOPTIONS controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aec3938e4322a13303ec2fc336b47d7e61a51eea58d49214001720a371f0326a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437455"
---
# <a name="em_settypographyoptions-message"></a>Mensaje \_ EM SETTYPOGRAPHYOPTIONS

Establece el estado actual de las opciones de tipografía de un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica uno o ambos de los valores siguientes.



| Value                                                                                                                                                                                    | Significado                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="TO_ADVANCEDTYPOGRAPHY_"></span><span id="to_advancedtypography_"></span><dl> <dt>**TO \_ ADVANCEDTYPOGRAPHY**</dt> </dl> | La separación de línea avanzada y el formato de línea están activados. <br/>                    |
| <span id="TO_SIMPLELINEBREAK"></span><span id="to_simplelinebreak"></span><dl> <dt>**PARA \_ SIMPLELINEBREAK**</dt> </dl>             | Separación de línea más rápida para texto simple **(requiere TO \_ ADVANCEDTYPOGRAPHY**). <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Máscara que consta de una o varias de las marcas de *wParam*. Solo se establecerán o borrarán las marcas que se establecen en esta máscara. Esto permite establecer o borrar una sola marca sin leer los estados de marca actuales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** *wParam es* válido; de lo **contrario, FALSE.**

## <a name="remarks"></a>Comentarios

La separación de línea avanzada se activa automáticamente mediante el control de edición enriquecido cuando es necesario, como para controlar scripts complejos como árabe y hebreo, y para matemáticas. También es necesario para párrafos, guiones y otras características tipográficas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ GETTYPOGRAPHYOPTIONS**](em-gettypographyoptions.md)
</dt> </dl>

 

 





