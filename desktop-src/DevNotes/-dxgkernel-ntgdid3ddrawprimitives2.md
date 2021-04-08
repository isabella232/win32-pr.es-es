---
description: Representa primitivas y devuelve el estado de representación actualizado.
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: Función NtGdiD3DDrawPrimitives2 (Ntgdi. h)
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
ms.openlocfilehash: ebde2fd5adf3b0892606d0ebbc1c7d5f6b55d9cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080135"
---
# <a name="ntgdid3ddrawprimitives2-function"></a>NtGdiD3DDrawPrimitives2 función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

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

*hCmdBuf* \[ de\]
</dt> <dd>

Identificador de la [**estructura \_ \_ local del área DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que identifica la superficie de DirectDraw que contiene los datos del comando.

</dd> <dt>

*hVBuf* \[ de\]
</dt> <dd>

Identificador de la [**estructura \_ \_ local**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) de la superficie de DD que identifica la superficie de DirectDraw que contiene los datos de vértices.

</dd> <dt>

*pded* \[ in, out\]
</dt> <dd>

Puntero a una estructura de [**\_ DRAWPRIMITIVES2DATA de D3DNTHAL**](/windows-hardware/drivers/ddi/) que contiene la información necesaria para que el controlador represente una o más primitivas.

</dd> <dt>

*pfpVidMemCmd* \[ in, out\]
</dt> <dd>

Nuevo puntero a la memoria de vídeo si el controlador intercambió el búfer de comandos.

</dd> <dt>

*pdwSizeCmd* \[ in, out\]
</dt> <dd>

Especifica el número mínimo de bytes que el controlador debe aumentar el búfer del comando swap.

</dd> <dt>

*pfpVidMemVtx* \[ in, out\]
</dt> <dd>

Nuevo puntero a la memoria de vídeo si el controlador cambió el búfer de vértices.

</dd> <dt>

*pdwSizeVtx* \[ in, out\]
</dt> <dd>

Especifica el número mínimo de bytes que debe asignar el controlador para el búfer de vértices de intercambio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiD3DDrawPrimitives2** devuelve uno de los siguientes códigos de devolución de llamada.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_controlador DDHAL \_ controlado**</dt> </dl>    | El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación. Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función. De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.<br/>                                                                                 |
| <dl> <dt>**\_NOTHANDLED del controlador DDHAL \_**</dt> </dl> | El controlador no tiene ningún comentario en la operación solicitada. Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error. De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.<br/> |



 

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

 

 
