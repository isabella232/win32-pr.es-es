---
description: Indica que ha comenzado un comando DVD Navigator.
ms.assetid: 230116b4-23f1-4c37-a781-da2c5aa20a1f
title: EC_DVD_CMD_START (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 418163b55699f8ba7c38026764f3326985d7e1788369729f42067cff62a56949
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998085"
---
# <a name="ec_dvd_cmd_start"></a>EC \_ DVD \_ CMD \_ START

Indica que ha comenzado [un comando DVD Navigator.](dvd-navigator-filter.md)

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

## <a name="remarks"></a>Comentarios

Este evento solo se desencadena si la aplicación establece la marca **\_ \_ \_ SendEvents CMD FLAG** de DVD en un método [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) que toma una marca [**CMD \_ \_ FLAGS de DVD.**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags)

Este evento se genera en el dominio de título.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdevcode.h (incluir Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificación de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Sincronizar comandos de DVD](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




