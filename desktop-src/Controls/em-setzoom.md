---
title: EM_SETZOOM mensaje (Richedit.h)
description: Establece la relación de zoom. La relación debe ser un valor entre 1/64 y 64. Puede enviar este mensaje a un control de edición o a un control de edición enriquecido.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- EM_SETZOOM controles de Windows mensaje
topic_type:
- apiref
api_name:
- EM_SETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf6541bc018df253a3ed45f8bced42e2f19938449d7fc35bf7f309909d53a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437185"
---
# <a name="em_setzoom-message"></a>Mensaje \_ DE EM SETZOOM

Establece la relación de zoom para un control de edición multilínea o un control de edición enriquecido. La relación debe ser un valor entre 1/64 y 64. El control de edición debe tener el estilo extendido **ES \_ EX \_ ZOOMABLE** establecido; para que este mensaje suba efecto, vea [Editar estilos extendidos de control](edit-control-window-extended-styles.md).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Numerador de la proporción de zoom.

</dd> <dt>

*lParam* 
</dt> <dd>

Denominador de la relación de zoom. Estos parámetros pueden tener los siguientes valores.



| Value                                                                                                                                                                                                                                                              | Significado                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <dt>**Ambos 0**</dt> </dl>                                                                                                   | Desactiva el zoom mediante el mensaje **\_ EM SETZOOM** (el zoom todavía puede producirse [**con TxGetExtent).**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)<br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <dt>**1/64 < (wParam/lParam) < 64**</dt> </dl> | Zooms display by the zoom ratio numerator/denominator<br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se acepta la nueva configuración de zoom, el valor devuelto es **TRUE.**

Si no se acepta la nueva configuración de zoom, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Comentarios

**Editar:** Compatible con Windows 10 1809 y versiones posteriores. El control de edición debe tener el estilo extendido **ES \_ EX \_ ZOOMABLE** establecido; para que este mensaje suba efecto, vea [Editar estilos extendidos de control](edit-control-window-extended-styles.md). Para obtener información sobre el control de edición, vea [Editar controles](about-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Rich Edit 3.0<br/>                                                              |
| Header<br/>                   | <dl> <dt>Richedit.h/Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EM \_ GETZOOM**](em-getzoom.md)
</dt> </dl>

 

 





