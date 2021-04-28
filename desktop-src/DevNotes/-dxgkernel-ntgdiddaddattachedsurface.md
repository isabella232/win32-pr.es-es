---
description: 'Función NtGdiDdAddAttachedSurface: adjunta una superficie a otra superficie.'
ms.assetid: c4ef9e96-c498-4175-a2cd-22e0f88fd86e
title: Función NtGdiDdAddAttachedSurface (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAddAttachedSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: dacaa07a586a88c808d8da07b8233002e8ae5055
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085793"
---
# <a name="ntgdiddaddattachedsurface-function"></a>Función NtGdiDdAddAttachedSurface

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios en el sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Adjunta una superficie a otra superficie.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdAddAttachedSurface(
  _In_    HANDLE                     hSurface,
  _In_    HANDLE                     hSurfaceAttached,
  _Inout_ PDD_ADDATTACHEDSURFACEDATA puAddAttachedSurfaceData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSurface* \[ En\]
</dt> <dd>

Identificador de una [**estructura LOCAL de DD \_ SURFACE \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa la superficie a la que se asocia otra superficie.

</dd> <dt>

*hSurfaceAttached* \[ En\]
</dt> <dd>

Identificador de una [**estructura LOCAL de DD \_ SURFACE \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa la superficie que se va a adjuntar.

</dd> <dt>

*puAddAttachedSurfaceData* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura \_ ADDATTACHEDSURFACEDATA de DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) que contiene la información necesaria para que el controlador realice los datos adjuntos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdAddAttachedSurface** devuelve uno de los siguientes códigos de devolución de llamada.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CONTROLADOR DDHAL \_ \_ MANIPULADO**</dt> </dl>    | El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación. Si este código es DD \_ correcto, DirectDraw o Direct3D continúa con la función . De lo contrario, DirectDraw o Direct3D devuelven el código de error proporcionado por el controlador y anulan la función.<br/>                                                                                 |
| <dl> <dt>**CONTROLADOR DDHAL \_ \_ NO CONTROLADA**</dt> </dl> | El controlador no tiene ningún comentario sobre la operación solicitada. Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D notifica una condición de error. De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido mediante la ejecución de la implementación independiente del dispositivo DirectDraw o Direct3D.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Compatibilidad con clientes de bajo nivel de gráficos](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
