---
title: EM_SETPAGEROTATE mensaje (Richedit.h)
description: Establece el diseño de texto para un control de edición enriquecido.
ms.assetid: 3c2a37fe-ee9f-4b34-87bf-7ac27d010afc
keywords:
- EM_SETPAGEROTATE controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eb595456bca444c92b536b0e428ee56a5903ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062079"
---
# <a name="em_setpagerotate-message"></a>Mensaje \_ EM SETPAGEROTATE

\[**EM \_ SETPAGEROTATE** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Establece el diseño de texto para un control de edición enriquecido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de diseño de texto. Puede ser uno de los siguientes valores.



| Value                                                                                                                                       | Significado                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="EPR_0"></span><span id="epr_0"></span><dl> <dt>**EPR \_ 0**</dt> </dl>       | El texto fluye de izquierda a derecha y de arriba abajo.<br/>                              |
| <span id="EPR_90"></span><span id="epr_90"></span><dl> <dt>**EPR \_ 90**</dt> </dl>    | El texto fluye de abajo a arriba y de izquierda a derecha.<br/>                              |
| <span id="EPR_180"></span><span id="epr_180"></span><dl> <dt>**EPR \_ 180**</dt> </dl> | El texto fluye de derecha a izquierda y de abajo a arriba.<br/>                              |
| <span id="EPR_270"></span><span id="epr_270"></span><dl> <dt>**EPR \_ 270**</dt> </dl> | El texto fluye de arriba abajo y de derecha a izquierda.<br/>                              |
| <span id="EPR_SE"></span><span id="epr_se"></span><dl> <dt>**Epr \_ SE**</dt> </dl>    | **Windows 8:** El texto fluye de arriba a abajo y de izquierda a derecha (diseño de texto de Tonón).<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

No se usa; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es el nuevo valor de diseño de texto.

## <a name="remarks"></a>Observaciones

Este mensaje establece el diseño de texto para todo el documento. Sin embargo, el contenido incrustado no se gira y la aplicación debe rotarlo por separado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp1\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**EM \_ GETPAGEROTATE**](em-getpagerotate.md)
</dt> </dl>

 

 





