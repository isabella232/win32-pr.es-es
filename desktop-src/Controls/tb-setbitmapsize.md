---
title: TB_SETBITMAPSIZE mensaje (Commctrl.h)
description: Establece el tamaño de las imágenes de mapa de bits que se van a agregar a una barra de herramientas.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- TB_SETBITMAPSIZE controles de Windows mensaje
topic_type:
- apiref
api_name:
- TB_SETBITMAPSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c8a717151041fb83b7a0206acf570a6ad7f76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127166657"
---
# <a name="tb_setbitmapsize-message"></a>Mensaje \_ SETBITMAPSIZE de TB

Establece el tamaño de las imágenes de mapa de bits que se van a agregar a una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

LOWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) el ancho, en píxeles, de las imágenes con mapa de bits. HIWORD [**especifica**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) el alto, en píxeles, de las imágenes con mapa de bits.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

El tamaño solo se puede establecer antes de agregar los mapas de bits a la barra de herramientas. Si una aplicación no establece explícitamente el tamaño del mapa de bits, el tamaño predeterminado es 16 por 15 píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

