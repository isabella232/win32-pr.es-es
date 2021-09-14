---
description: Notifica a la aplicación el progreso al abrir un archivo de red.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc06022a9774d851cabff6a18c0f8808f62f14f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161541"
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

## <a name="remarks"></a>Observaciones

El [filtro WM ASF Reader](wm-asf-reader-filter.md) y el filtro heredado Windows origen [multimedia](windows-media-source-filter.md) envían este evento. El primer parámetro de evento tiene uno de los siguientes valores.



| Value                        | Descripción                                    |
|------------------------------|------------------------------------------------|
| AM \_ LOADSTATUS \_ CLOSED       | El filtro de origen ha cerrado el archivo.         |
| CONEXIÓN \_ DE AM LOADSTATUS \_   | El filtro de origen se conecta al servidor. |
| A. \_ M. \_ LOADSTATUS LOADINGDESCR | No se usa.                                      |
| AM \_ LOADSTATUS \_ LOADINGMCAST | No se usa                                       |
| LOCALIZACIÓN \_ DE AM \_ LOADSTATUS     | El filtro de origen está localizando los datos solicitados.  |
| AM \_ LOADSTATUS \_ OPEN         | El filtro de origen ha abierto el archivo.         |
| AM \_ LOADSTATUS \_ OPENING      | El filtro de origen está abriendo el archivo.         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




