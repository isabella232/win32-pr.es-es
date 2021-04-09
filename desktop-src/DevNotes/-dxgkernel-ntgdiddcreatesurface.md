---
description: Conecta una superficie a otra superficie.
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: Función NtGdiDdCreateSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 663d29be32dc544d44a47061e1a6ff7f81e60862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152811"
---
# <a name="ntgdiddcreatesurface-function"></a>NtGdiDdCreateSurface función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Conecta una superficie a otra superficie.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdCreateSurface(
  _In_    HANDLE               hDirectDraw,
  _In_    HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Out_   HANDLE               *puhSurface
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDirectDraw* \[ de\]
</dt> <dd>

Identificador de la [**estructura \_ \_ global DD DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) que representa el controlador.

</dd> <dt>

*hSurface* \[ de\]
</dt> <dd>

Identificador anterior de la misma superficie. Se usa si la superficie se vuelve a crear después de un cambio de modo.

</dd> <dt>

*puSurfaceDescription* \[ in, out\]
</dt> <dd>

Puntero a la estructura [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) que describe la superficie o el búfer que debe crear el controlador.

</dd> <dt>

*puSurfaceGlobalData* \[ in, out\]
</dt> <dd>

Puntero a la [**estructura \_ \_ global de la superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) que contiene los datos de la superficie que se comparten globalmente con varias superficies.

</dd> <dt>

*puSurfaceLocalData* \[ in, out\]
</dt> <dd>

Puntero a una lista de [**estructuras \_ \_ locales de la superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que describen los objetos Surface creados por el controlador.

</dd> <dt>

*puSurfaceMoreData* \[ in, out\]
</dt> <dd>

Puntero a una [**superficie de DD \_ \_ más**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) estructura que contiene datos adicionales de la superficie local.

</dd> <dt>

*puCreateSurfaceData* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**DD \_ CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) que contiene la información necesaria para crear una superficie.

</dd> <dt>

*puhSurface* \[ enuncia\]
</dt> <dd>

La API de DirectDraw usa y no debe rellenar el controlador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdCreateSurface** devuelve uno de los siguientes códigos de devolución de llamada.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_controlador DDHAL \_ controlado**</dt> </dl>    | El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación. Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función. De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.<br/>                                                                                 |
| <dl> <dt>**\_NOTHANDLED del controlador DDHAL \_**</dt> </dl> | El controlador no tiene ningún comentario en la operación solicitada. Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error. De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.<br/> |



 

## <a name="remarks"></a>Observaciones

Se recomienda que la aplicación llame a [IDirectDraw7:: CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) en lugar de usar esta función.

Al crear una cadena de superficies asociadas, como una cadena o cadena de intercambio, se debe llamar primero a [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) para cada superficie. A continuación, llame a [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) para adjuntarlos. Por último, llame a **NtGdiDdCreateSurface** solo para la primera superficie de la cadena. En este caso, *hSurface* sería el identificador devuelto por **NtGdiDdCreateSurfaceObject** para la primera superficie de la cadena.

Solo se debe llamar a **NtGdiDdCreateSurface** para crear superficies en la memoria de vídeo local y no local. Nunca se debe llamar para crear superficies de memoria del sistema. Para crear superficies de memoria del sistema, use [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) en su lugar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con clientes de nivel inferior de gráficos](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
