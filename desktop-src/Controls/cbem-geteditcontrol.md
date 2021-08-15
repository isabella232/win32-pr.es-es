---
title: CBEM_GETEDITCONTROL mensaje (Commctrl.h)
description: Obtiene el identificador de la parte del control de edición de un control ComboBoxEx. Un control ComboBoxEx usa un cuadro de edición cuando se establece en el estilo DE LISTA DESPLEGABLE \_ de CBS.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- CBEM_GETEDITCONTROL controles de Windows mensaje
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885a90a1b37fab7cd8e4a492bd00ad349f96202e13ee25a404f7f4aa41f623e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118414075"
---
# <a name="cbem_geteditcontrol-message"></a>Mensaje \_ GETEDITCONTROL de CBEM

Obtiene el identificador de la parte del control de edición de un control ComboBoxEx. Un control ComboBoxEx usa un cuadro de edición cuando se establece en el estilo [**DE LISTA DESPLEGABLE \_ de CBS.**](combo-box-styles.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador al control de edición dentro del control ComboBoxEx si usa el [**estilo \_ DROPDOWN de CBS.**](combo-box-styles.md) De lo contrario, el mensaje devuelve **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





