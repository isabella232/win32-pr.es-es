---
description: Indica que se ha completado un comando determinado de DVD Navigator.
ms.assetid: f460db8e-b966-41fa-bfa1-4ad3fa65c3e3
title: EC_DVD_CMD_END (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_END
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 550a3969ba431127b05234a0c9fe38eb5938ebf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063274"
---
# <a name="ec_dvd_cmd_end"></a>EC \_ DVD \_ CMD \_ END

Indica que se ha completado [un comando determinado](dvd-navigator-filter.md) de DVD Navigator.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Identificador del comando. Pase este parámetro al [**método IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) para recuperar un puntero de [**interfaz IDvdCmd.**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd)

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**Valor HRESULT** que indica el estado del comando.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este evento solo se desencadena si la aplicación establece la marca SendEvents CMD FLAG de DVD en un método \_ \_ \_ [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) que toma una marca [**\_ CMD \_ FLAGS de DVD.**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags)

Este evento se genera en el dominio de título.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdevcode.h (incluir Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificación de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Sincronizar comandos de DVD](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




