---
description: Notifica a la aplicación de progreso cuando se abre un archivo de red.
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: EC_LOADSTATUS (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc06022a9774d851cabff6a18c0f8808f62f14f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680994"
---
# <a name="ec_loadstatus"></a>LOADSTATUS de EC \_

Notifica a la aplicación de progreso cuando se abre un archivo de red.

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

El filtro de [lector ASF de WM](wm-asf-reader-filter.md) y el filtro de [origen de medios de Windows](windows-media-source-filter.md) heredado envían este evento. El primer parámetro de evento tiene uno de los valores siguientes.



| Value                        | Descripción                                    |
|------------------------------|------------------------------------------------|
| AM \_ LOADSTATUS \_ cerrado       | El filtro de origen ha cerrado el archivo.         |
| \_conexión LOADSTATUS \_ AM   | El filtro de origen se está conectando al servidor. |
| \_LOADINGDESCR LOADSTATUS \_ AM | No se utiliza.                                      |
| \_LOADINGMCAST LOADSTATUS \_ AM | No se usa                                       |
| LOADSTATUS de AM \_ \_     | El filtro de origen está buscando los datos solicitados.  |
| AM \_ LOADSTATUS \_ abierto         | El filtro de origen ha abierto el archivo.         |
| \_abrir LOADSTATUS \_ AM      | El filtro de origen está abriendo el archivo.         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




