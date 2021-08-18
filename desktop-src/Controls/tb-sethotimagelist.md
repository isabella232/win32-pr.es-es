---
title: TB_SETHOTIMAGELIST mensaje (Commctrl.h)
description: Establece la lista de imágenes que usará el control de barra de herramientas para mostrar los botones de acceso rápido.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- TB_SETHOTIMAGELIST controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12d07c66add48fa8022f7b8505bee377be184af3ed8195251b3a92b46d0ff58c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318855"
---
# <a name="tb_sethotimagelist-message"></a>Mensaje \_ SETHOTIMAGELIST de TB

Establece la lista de imágenes que usará el control de barra de herramientas para mostrar los botones de acceso rápido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador de la lista de imágenes que se establecerá.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el identificador a la lista de imágenes usada anteriormente para mostrar botones de acceso rápido, o **NULL** si no se estableció previamente ninguna lista de imágenes.

## <a name="remarks"></a>Comentarios

Un botón está en caliente cuando el cursor está sobre él. Los controles de barra de herramientas deben tener el estilo [**TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) o [**TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) para tener elementos de acceso rápido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





