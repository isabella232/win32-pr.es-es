---
title: Mensaje EM_SETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Establece el estado actual de las opciones tipográficas de un control Rich Edit.
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- EM_SETTYPOGRAPHYOPTIONS controles de mensajes de Windows
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
ms.openlocfilehash: 0528e19aacec394c5af6250536fdc4f693e60ece
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996557"
---
# <a name="em_settypographyoptions-message"></a>\_Mensaje SETTYPOGRAPHYOPTIONS em

Establece el estado actual de las opciones tipográficas de un control Rich Edit.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica uno o ambos de los valores siguientes.



| Value                                                                                                                                                                                    | Significado                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="TO_ADVANCEDTYPOGRAPHY_"></span><span id="to_advancedtypography_"></span><dl> <dt>**A \_ ADVANCEDTYPOGRAPHY**</dt> </dl> | El salto de línea y el formato de línea avanzados están activados. <br/>                    |
| <span id="TO_SIMPLELINEBREAK"></span><span id="to_simplelinebreak"></span><dl> <dt>**a \_ SIMPLELINEBREAK**</dt> </dl>             | Salto de línea más rápido para texto simple (requiere **\_ ADVANCEDTYPOGRAPHY**). <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Máscara formada por una o varias de las marcas de *wParam*. Solo se establecerán o se borrarán las marcas que se establezcan en esta máscara. Esto permite establecer o borrar una sola marca sin leer los Estados actuales de la marca.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si *wParam* es válido; en caso contrario, **false**.

## <a name="remarks"></a>Observaciones

El control Rich Edit activa automáticamente el salto de línea avanzado cuando sea necesario, por ejemplo, para administrar scripts complejos como el árabe y el hebreo, y para las matemáticas. También es necesario para párrafos justificados, guiones y otras características tipográficas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Edición enriquecida 3,0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETTYPOGRAPHYOPTIONS em**](em-gettypographyoptions.md)
</dt> </dl>

 

 





