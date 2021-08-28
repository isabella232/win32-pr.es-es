---
description: Reposiciones o modifica los atributos visuales de una superficie superpuesta.
ms.assetid: 6d39166c-0efc-450d-adf4-9f4dfdf7c57f
title: Función NtGdiDdUpdateOverlay (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUpdateOverlay
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c65e906529e8afa11f2a16a1171c1d4a7c31ae29bac70d8200997b7a7b88a131
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108945"
---
# <a name="ntgdiddupdateoverlay-function"></a>Función NtGdiDdUpdateOverlay

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Reposiciones o modifica los atributos visuales de una superficie superpuesta.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdUpdateOverlay(
  _In_    HANDLE                hSurfaceDestination,
  _In_    HANDLE                hSurfaceSource,
  _Inout_ PDD_UPDATEOVERLAYDATA puUpdateOverlayData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSurfaceDestination* \[ En\]
</dt> <dd>

Identificador del objeto DirectDraw en modo kernel creado anteriormente.

</dd> <dt>

*hSurfaceSource* \[ En\]
</dt> <dd>

Controlar una estructura [**LOCAL de \_ DD SURFACE \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que describe la superficie superpuesta.

</dd> <dt>

*puUpdateOverlayData* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura \_ UPDATEOVERLAYDATA de DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata) que contiene la información necesaria para actualizar la superposición.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdUpdateOverlay** devuelve uno de los siguientes códigos de devolución de llamada.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CONTROLADOR DDHAL \_ \_ MANIPULADO**</dt> </dl>    | El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación. Si este código es correcto para \_ DD, DirectDraw o Direct3D continúa con la función . De lo contrario, DirectDraw o Direct3D devuelven el código de error proporcionado por el controlador y anulan la función.<br/>                                                                                 |
| <dl> <dt>**CONTROLADOR DDHAL \_ \_ NO CONTROLADA**</dt> </dl> | El controlador no tiene ningún comentario sobre la operación solicitada. Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D notifica una condición de error. De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido mediante la ejecución de la implementación independiente del dispositivo DirectDraw o Direct3D.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con clientes de bajo nivel de gráficos](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
