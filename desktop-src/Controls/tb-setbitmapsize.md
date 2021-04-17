---
title: Mensaje de TB_SETBITMAPSIZE (commctrl. h)
description: Establece el tamaño de las imágenes de mapa de imágenes que se van a agregar a una barra de herramientas.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- TB_SETBITMAPSIZE controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489029"
---
# <a name="tb_setbitmapsize-message"></a>\_Mensaje SETBITMAPSIZE TB

Establece el tamaño de las imágenes de mapa de imágenes que se van a agregar a una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el ancho, en píxeles, de las imágenes de mapa de bytes. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el alto, en píxeles, de las imágenes de mapa Dete.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Solo se puede establecer el tamaño antes de agregar mapas de bits a la barra de herramientas. Si una aplicación no establece explícitamente el tamaño del mapa de bits, el tamaño predeterminado es de 16 por 15 píxeles.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

