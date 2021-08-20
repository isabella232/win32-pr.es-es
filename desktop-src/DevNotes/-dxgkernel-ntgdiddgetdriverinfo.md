---
description: Consulta al controlador la funcionalidad adicional de Microsoft DirectDraw y Microsoft Direct3D que admite el controlador.
ms.assetid: 7169b672-5c61-4fca-860b-5ef426a7f925
title: Función NtGdiDdGetDriverInfo (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDriverInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: ef06c770eac2e0b57f6bbdfcb6767a415d1d5da7a89ae24cb1661b0f18e0f0ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956354"
---
# <a name="ntgdiddgetdriverinfo-function"></a>Función NtGdiDdGetDriverInfo

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use DirectDraw y Direct3DAPI; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Consulta al controlador la funcionalidad adicional de Microsoft DirectDraw y Microsoft Direct3D que admite el controlador.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdGetDriverInfo(
  _In_    HANDLE                hDirectDraw,
  _Inout_ PDD_GETDRIVERINFODATA puGetDriverInfoData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDirectDraw* \[ En\]
</dt> <dd>

Identificador del objeto DirectDraw en modo kernel creado anteriormente.

</dd> <dt>

*puGetDriverInfoData* \[ in, out\]
</dt> <dd>

Puntero a una [estructura \_ GETDRIVERINFODATA](https://msdn.microsoft.com/library/ms793868.aspx) de DD que contiene la información necesaria para realizar la consulta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdGetDriverInfo** devuelve uno de los siguientes códigos de devolución de llamada.



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

 

 




