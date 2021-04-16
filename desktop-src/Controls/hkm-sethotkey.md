---
title: Mensaje de HKM_SETHOTKEY (commctrl. h)
description: Establece la combinación de teclas de acceso rápido de un control de tecla de acceso rápido.
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- HKM_SETHOTKEY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3672136c44c0268e218e7f87cbbeb3373b76b39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534036"
---
# <a name="hkm_sethotkey-message"></a>HKM \_ SETHOTKEY

Establece la combinación de teclas de acceso rápido de un control de tecla de acceso rápido.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) de [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) es el código de tecla virtual de la tecla de acceso rápido. El [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) de **LOWORD** es el modificador de clave que indica las teclas que definen una combinación de teclas de acceso rápido. Para obtener una lista de valores de marcador de modificador, vea la descripción del mensaje [**\_ GETHOTKEY de HKM**](hkm-gethotkey.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

No se utiliza; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

