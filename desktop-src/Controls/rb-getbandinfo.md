---
title: Mensaje de RB_GETBANDINFO (commctrl. h)
description: Recupera información sobre una banda especificada en un control rebar.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- RB_GETBANDINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87715cf61b4eb2726eab83d500330721f41719f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150656"
---
# <a name="rb_getbandinfo-message"></a>Mensaje de GETBANDINFO de RB \_

Recupera información sobre una banda especificada en un control rebar.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base cero de la banda para la que se recuperará la información.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que recibirá la información de la banda solicitada. Antes de enviar este mensaje, debe establecer el miembro **cbSize** de esta estructura en el tamaño de la estructura **REBARBANDINFO** y establecer el miembro **fMask** en los elementos que desea recuperar. Además, debe establecer el miembro **CCH** de la estructura **REBARBANDINFO** en el tamaño del búfer **lpText** cuando \_ se especifica RBBIM Text.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si es correcto o cero de lo contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **RB \_ GETBANDINFOW** (Unicode) y **RB \_ GETBANDINFOA** (ANSI)<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SETBANDINFO RB**](rb-setbandinfo.md)
</dt> </dl>

 

 





