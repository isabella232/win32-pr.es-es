---
description: Indica al controlador qué macrobloques se deben representar especificando las superficies que contienen los macrobloques, los desplazamientos en cada superficie donde existen los macrobloques y el tamaño de los datos de macrobloque que se representarán.
ms.assetid: c49d9dfa-a3db-4572-a474-72c7d4e80940
title: Función NtGdiDdRenderMoComp (Ntgdi.h)
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
ms.openlocfilehash: d057ba1c7b533d75ce10754670b911ddc01a689acee29d79614a3ce2f273d278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827976"
---
# <a name="ntgdiddrendermocomp-function"></a>Función NtGdiDdRenderMoComp

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Indica al controlador qué macrobloques se deben representar especificando las superficies que contienen los macrobloques, los desplazamientos en cada superficie donde existen los macrobloques y el tamaño de los datos de macrobloque que se representarán.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdRenderMoComp(
  _In_    HANDLE               hMoComp,
  _Inout_ PDD_RENDERMOCOMPDATA puRenderMoCompData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMoComp* \[ En\]
</dt> <dd>

Controlar a una [**estructura \_ LOCAL MOTIONCOMP \_ de DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) que contiene una descripción de la compensación de movimiento que se solicita.

</dd> <dt>

*puRenderMoCompData* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura \_ RENDERMOCOMPDATA de DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_rendermocompdata) que contiene la información necesaria para representar un marco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdRenderMoComp devuelve** uno de los siguientes códigos de devolución de llamada.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CONTROLADOR DDHAL \_ \_ MANIPULADO**</dt> </dl>    | El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación. Si este código es correcto para \_ DD, DirectDraw o Direct3D continúa con la función . De lo contrario, DirectDraw o Direct3D devuelven el código de error proporcionado por el controlador y anulan la función.<br/>                                                                                 |
| <dl> <dt>**CONTROLADOR DDHAL \_ \_ NO CONTROLADA**</dt> </dl> | El controlador no tiene ningún comentario sobre la operación solicitada. Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D notifica una condición de error. De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido mediante la ejecución de la implementación independiente del dispositivo DirectDraw o Direct3D.<br/> |



 

## <a name="remarks"></a>Comentarios

Para más información, consulte El Kit de desarrollo de controladores de aceleración de vídeo (DDK) de Microsoft DirectX.

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

 

 
