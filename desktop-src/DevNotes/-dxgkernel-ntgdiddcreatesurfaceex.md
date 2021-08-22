---
description: Crea una superficie de Microsoft Direct3D a partir de una superficie de Microsoft DirectDraw y le asocia un valor de identificador solicitado.
ms.assetid: 7b1ce714-a56e-4508-8160-af8c1748c5f7
title: Función NtGdiDdCreateSurfaceEx (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceEx
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: ff5db8859cc339dc97f86e1b0421f662d69b85ba0f46449a1e721c1dc355d79c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956564"
---
# <a name="ntgdiddcreatesurfaceex-function"></a>Función NtGdiDdCreateSurfaceEx

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use DirectDraw y Direct3DAPI; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Crea una superficie de Microsoft Direct3D a partir de una superficie de Microsoft DirectDraw y le asocia un valor de identificador solicitado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdCreateSurfaceEx(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ DWORD  dwSurfaceHandle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDirectDraw* \[ En\]
</dt> <dd>

Identificador del objeto DirectDraw creado por la aplicación.

</dd> <dt>

*hSurface* \[ En\]
</dt> <dd>

Identificador de la superficie de DirectDraw que se va a crear para Direct3D. Estos identificadores son únicos dentro de cada estructura [**\_ \_ LOCAL DD DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) diferente.

</dd> <dt>

*dwSurfaceHandle* \[ En\]
</dt> <dd>

Controlar una [**estructura \_ CREATESURFACEEXDATA de DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) que contiene la información necesaria para que el controlador cree la superficie.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdCreateSurfaceEx devuelve** uno de los siguientes códigos de devolución de llamada.



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

 

 
