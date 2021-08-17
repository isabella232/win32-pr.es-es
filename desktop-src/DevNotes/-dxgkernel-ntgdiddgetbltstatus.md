---
description: Consulta el estado blit de la superficie especificada.
ms.assetid: 0221bdc6-2146-4f4d-afb5-d1f701446d5e
title: Función NtGdiDdGetBltStatus (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetBltStatus
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 488d0b28da747346b795ef7a1c5a3846d4661c0afb31c65a9e624584b8fe60e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956364"
---
# <a name="ntgdiddgetbltstatus-function"></a>Función NtGdiDdGetBltStatus

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Consulta el estado blit de la superficie especificada.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdGetBltStatus(
  _In_    HANDLE               hSurface,
  _Inout_ PDD_GETBLTSTATUSDATA puGetBltStatusData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSurface* \[ En\]
</dt> <dd>

Controlar una estructura [LOCAL de \_ DD SURFACE \_ que](https://msdn.microsoft.com/library/ms793861.aspx) representa la superficie cuyo estado de la blit se está consultando.

</dd> <dt>

*puGetBltStatusData* \[ in, out\]
</dt> <dd>

Puntero a una [estructura \_ GETBLTSTATUSDATA](https://msdn.microsoft.com/library/ms794243.aspx) de DD que contiene la información necesaria para realizar la consulta de estado blit.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdGetBltStatus devuelve** uno de los siguientes códigos de devolución de llamada.



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

 

 




