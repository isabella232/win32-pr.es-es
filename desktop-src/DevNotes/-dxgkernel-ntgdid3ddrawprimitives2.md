---
description: Representa primitivas y devuelve el estado de representación actualizado.
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: Función NtGdiD3DDrawPrimitives2 (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DDrawPrimitives2
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 8d3964a9946da37d211aab0e5949cff5e09a40dcc18607aabb3a0c13c37acfe9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833665"
---
# <a name="ntgdid3ddrawprimitives2-function"></a>Función NtGdiD3DDrawPrimitives2

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Representa primitivas y devuelve el estado de representación actualizado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiD3DDrawPrimitives2(
  _In_    HANDLE                         hCmdBuf,
  _In_    HANDLE                         hVBuf,
  _Inout_ LPD3DNTHAL_DRAWPRIMITIVES2DATA pded,
  _Inout_ FLATPTR                        *pfpVidMemCmd,
  _Inout_ DWORD                          *pdwSizeCmd,
  _Inout_ FLATPTR                        *pfpVidMemVtx,
  _Inout_ DWORD                          *pdwSizeVtx
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hCmdBuf* \[ En\]
</dt> <dd>

Identificador de la [**estructura \_ \_ LOCAL de DD SURFACE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que identifica la superficie de DirectDraw que contiene los datos del comando.

</dd> <dt>

*hVBuf* \[ En\]
</dt> <dd>

Controle la estructura [**\_ \_ LOCAL de DD SURFACE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que identifica la superficie de DirectDraw que contiene los datos del vértice.

</dd> <dt>

*pded* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura D3DNRENDER \_ DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/) que contiene la información necesaria para que el controlador represente una o varias primitivas.

</dd> <dt>

*pfpVidMemCmd* \[ in, out\]
</dt> <dd>

Nuevo puntero a la memoria de vídeo si el controlador intercambie el búfer de comandos.

</dd> <dt>

*pdwSizeCmd* \[ in, out\]
</dt> <dd>

Especifica el número mínimo de bytes por el que el controlador debe aumentar el búfer del comando de intercambio.

</dd> <dt>

*pfpVidMemVtx* \[ in, out\]
</dt> <dd>

Nuevo puntero a la memoria de vídeo si el controlador intercambie el búfer de vértices.

</dd> <dt>

*pdwSizeVtx* \[ in, out\]
</dt> <dd>

Especifica el número mínimo de bytes que el controlador debe asignar para el búfer de vértices de intercambio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiD3DDrawPrimitives2** devuelve uno de los siguientes códigos de devolución de llamada.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CONTROLADOR DDHAL \_ \_ MANIPULADO**</dt> </dl>    | El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación. Si este código es correcto para \_ DD, DirectDraw o Direct3D continúa con la función . De lo contrario, DirectDraw o Direct3D devuelven el código de error proporcionado por el controlador y anulan la función.<br/>                                                                                 |
| <dl> <dt>**CONTROLADOR DDHAL \_ \_ NO CONTROLADA**</dt> </dl> | El controlador no tiene ningún comentario sobre la operación solicitada. Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D notifica una condición de error. De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido mediante la ejecución de la implementación independiente del dispositivo DirectDraw o Direct3D.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con clientes de bajo nivel de gráficos](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
