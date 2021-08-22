---
description: Notifica a la aplicación el progreso al abrir un archivo de red.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499f05a26f3fa1387347929f5c14a64b1f440a53ed9b5fd17830d582fb640c3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015943"
---
# <a name="ec_loadstatus"></a>EC \_ LOADSTATUS

Notifica a la aplicación el progreso al abrir un archivo de red.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Código de estado. Vea la sección Comentarios.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Comentarios

El [filtro WM ASF Reader y](wm-asf-reader-filter.md) el filtro heredado Windows origen [multimedia](windows-media-source-filter.md) envían este evento. El primer parámetro de evento tiene uno de los siguientes valores.



| Value                        | Descripción                                    |
|------------------------------|------------------------------------------------|
| AM \_ LOADSTATUS \_ CLOSED       | El filtro de origen ha cerrado el archivo.         |
| AM \_ LOADSTATUS \_ CONNECTING   | El filtro de origen se conecta al servidor. |
| CARGA \_ DE AM \_ LOADSTATUSDESCR | No se usa.                                      |
| AM \_ LOADSTATUS \_ LOADINGMCAST | No se usa                                       |
| LOCALIZACIÓN \_ DE AM LOADSTATUS \_     | El filtro de origen está localizando los datos solicitados.  |
| AM \_ LOADSTATUS \_ OPEN         | El filtro de origen ha abierto el archivo.         |
| AM \_ LOADSTATUS \_ OPENING      | El filtro de origen está abriendo el archivo.         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




