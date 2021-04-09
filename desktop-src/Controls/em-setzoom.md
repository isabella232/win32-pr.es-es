---
title: Mensaje EM_SETZOOM (RichEdit. h)
description: Establece la relación de zoom. La relación debe ser un valor entre 1/64 y 64. Puede enviar este mensaje a un control de edición o a un control Rich Edit.
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- EM_SETZOOM controles de mensajes de Windows
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
ms.openlocfilehash: 7d38630f27afcfc0ed29e3ccc3129e2dea22d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905359"
---
# <a name="em_setzoom-message"></a>\_Mensaje SETZOOM em

Establece la relación de zoom para un control de edición de varias líneas o un control Rich Edit. La relación debe ser un valor entre 1/64 y 64. El control de edición debe tener el conjunto de estilo extendido **es \_ ex \_** para el que este mensaje tiene un efecto, vea [Edit control Extended Styles](edit-control-window-extended-styles.md).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Numerador de la relación de zoom.

</dd> <dt>

*lParam* 
</dt> <dd>

Denominador de la relación de zoom. Estos parámetros pueden tener los valores siguientes.



| Value                                                                                                                                                                                                                                                              | Significado                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <dt>**Ambos 0**</dt> </dl>                                                                                                   | Desactiva el zoom mediante el mensaje **em \_ SETZOOM** (el zoom puede seguir produciendo el uso de [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)).<br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <dt>**1/64 < (wParam/lParam) < 64**</dt> </dl> | Zooms mostrados por el numerador y el denominador de la relación de zoom<br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se acepta la nueva configuración de zoom, el valor devuelto es **true**.

Si no se acepta la nueva configuración de zoom, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

**Editar:** Compatible con Windows 10 1809 y versiones posteriores. El control de edición debe tener el conjunto de estilo extendido **es \_ ex \_** para el que este mensaje tiene un efecto, vea [Edit control Extended Styles](edit-control-window-extended-styles.md). Para obtener información sobre el control de edición, vea [controles de edición](about-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Redistribuible<br/>          | Edición enriquecida 3,0<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>RichEdit. h/commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_GETZOOM em**](em-getzoom.md)
</dt> </dl>

 

 





