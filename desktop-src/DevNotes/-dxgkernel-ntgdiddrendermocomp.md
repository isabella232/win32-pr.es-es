---
description: Indica al controlador qué macrobloques representar especificando las superficies que contienen macrobloques, los desplazamientos en cada superficie donde existe el macrobloques y el tamaño de los datos de adaptativo macrobloque que se van a representar.
ms.assetid: c49d9dfa-a3db-4572-a474-72c7d4e80940
title: Función NtGdiDdRenderMoComp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdRenderMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 6e1dd0942a6996264e02531f7e21b2a99f059143
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906973"
---
# <a name="ntgdiddrendermocomp-function"></a>NtGdiDdRenderMoComp función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Indica al controlador qué macrobloques representar especificando las superficies que contienen macrobloques, los desplazamientos en cada superficie donde existe el macrobloques y el tamaño de los datos de adaptativo macrobloque que se van a representar.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdRenderMoComp(
  _In_    HANDLE               hMoComp,
  _Inout_ PDD_RENDERMOCOMPDATA puRenderMoCompData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMoComp* \[ de\]
</dt> <dd>

Identificador de una [**estructura \_ \_ local DD MOTIONCOMP**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) que contiene una descripción de la compensación de movimiento que se solicita.

</dd> <dt>

*puRenderMoCompData* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**DD \_ RENDERMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_rendermocompdata) que contiene la información necesaria para representar un marco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdRenderMoComp** devuelve uno de los siguientes códigos de devolución de llamada.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_controlador DDHAL \_ controlado**</dt> </dl>    | El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación. Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función. De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.<br/>                                                                                 |
| <dl> <dt>**\_NOTHANDLED del controlador DDHAL \_**</dt> </dl> | El controlador no tiene ningún comentario en la operación solicitada. Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error. De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.<br/> |



 

## <a name="remarks"></a>Observaciones

Para obtener más información, vea el kit de desarrollo de controladores (DDK) de Microsoft DirectX video Acceleration.

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

 

 
