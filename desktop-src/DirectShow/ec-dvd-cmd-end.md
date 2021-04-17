---
description: Indica que se ha completado un comando determinado del explorador de DVD.
ms.assetid: f460db8e-b966-41fa-bfa1-4ad3fa65c3e3
title: EC_DVD_CMD_END (Dvdevcode. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690047"
---
# <a name="ec_dvd_cmd_end"></a>\_fin de \_ cmd de DVD de EC \_

Indica que se ha completado un comando determinado del [Explorador de DVD](dvd-navigator-filter.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Identificador del comando. Pase este parámetro al método [**IDvdInfo2:: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) para recuperar un puntero de interfaz [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor **HRESULT** que indica el estado del comando.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este evento solo se desencadena si la aplicación establece la marca \_ \_ \_ SendEvents de la marca de cmd de DVD en un método [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) que toma una marca de [**marcas de \_ cmd \_ de DVD**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) .

Este evento se desencadena en el dominio de título.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdevcode. h (incluir DShow. h)</dt> </dl> |



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

 

 




