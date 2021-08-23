---
description: Se usa para crear un comando de nivel de controlador o un búfer de vértices de la descripción especificada.
ms.assetid: c65403a1-5686-4c7d-80a4-6e49417c11eb
title: Función NtGdiDdCreateD3DBuffer (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 55e28e50f10ced5380685cbdb5016363a77adc7e61d2df201565d18f4794fcf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956704"
---
# <a name="ntgdiddcreated3dbuffer-function"></a>Función NtGdiDdCreateD3DBuffer

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Se usa para crear un comando de nivel de controlador o un búfer de vértices de la descripción especificada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdCreateD3DBuffer(
  _In_    HANDLE               hDirectDraw,
  _Inout_ HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Inout_ HANDLE               *puhSurface
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDirectDraw* \[ En\]
</dt> <dd>

Identificador de la [**estructura \_ DD DIRECTDRAW \_ GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa el controlador.

</dd> <dt>

*hSurface* \[ in, out\]
</dt> <dd>

Puntero a una matriz de identificadores de superficie. El autor de la llamada puede establecer estos identificadores en los valores de identificador anteriores si las superficies se van a volver a crear después de un cambio de modo. Este proceso se denomina "restauración" en la documentación de DirectDraw.

</dd> <dt>

*puSurfaceDescription* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) que describe la superficie o el búfer que debe crear el controlador.

</dd> <dt>

*puSurfaceGlobalData* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura GLOBAL \_ de DD SURFACE \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) que contiene datos de superficie que se comparten globalmente con varias superficies.

</dd> <dt>

*puSurfaceLocalData* \[ in, out\]
</dt> <dd>

Puntero a una lista de estructuras [**\_ \_ LOCALES de DD SURFACE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que describen los objetos de superficie creados por el controlador. Normalmente solo hay una entrada en esta matriz.

</dd> <dt>

*puSurfaceMoreData* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura DD \_ SURFACE \_ MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) que contiene datos de superficie locales adicionales.

</dd> <dt>

*puCreateSurfaceData* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura \_ CREATESURFACEDATA de DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) que contiene la información necesaria para crear el búfer.

</dd> <dt>

*puhSurface* \[ in, out\]
</dt> <dd>

La API de DirectDraw la usa y el controlador no debe rellenarlo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdCreateD3DBuffer** devuelve uno de los siguientes códigos de devolución de llamada.



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

 

 
