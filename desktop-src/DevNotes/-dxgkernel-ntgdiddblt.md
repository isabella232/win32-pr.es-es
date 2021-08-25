---
description: Realiza una transferencia de bloque de bits.
ms.assetid: 90cc02af-96af-4913-ae7d-62f39cd6ddd7
title: Función NtGdiDdBlt (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdBlt
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f0f4ae51663e9d1c398c34708520047f43288c1f571458a879e262ec9fca025d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911964"
---
# <a name="ntgdiddblt-function"></a>Función NtGdiDdBlt

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Realiza una transferencia de bloque de bits.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdBlt(
  _In_    HANDLE      hSurfaceDest,
  _In_    HANDLE      hSurfaceSrc,
  _Inout_ PDD_BLTDATA puBltData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSurfaceDest* \[ En\]
</dt> <dd>

Controlar una estructura [**\_ \_ LOCAL de DD SURFACE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que describe la superficie en la que se va a blit.

</dd> <dt>

*hSurfaceSrc* \[ En\]
</dt> <dd>

Identificador de una [**estructura \_ \_ LOCAL de DD SURFACE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que describe la superficie de origen.

</dd> <dt>

*puBltData* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura \_ BLTDATA de DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_bltdata) que contiene la información necesaria para que el controlador realice la blit.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdBlt devuelve** uno de los siguientes códigos de devolución de llamada.



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

 

 
