---
description: Hace que la memoria de superficie asociada al destino y las superficies actuales se intercambian.
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: Función NtGdiDdFlip (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlip
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 18113c841c22b31c9768d42491a63ead8cafee3c3b598bc46f442068592e67b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956494"
---
# <a name="ntgdiddflip-function"></a>Función NtGdiDdFlip

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Hace que la memoria de superficie asociada al destino y las superficies actuales se intercambian.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdFlip(
  _In_    HANDLE       hSurfaceCurrent,
  _In_    HANDLE       hSurfaceTarget,
  _In_    HANDLE       hSurfaceCurrentLeft,
  _In_    HANDLE       hSurfaceTargetLeft,
  _Inout_ PDD_FLIPDATA puFlipData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSurfaceCurrent* \[ En\]
</dt> <dd>

Identificador de la [estructura \_ \_ LOCAL de DD SURFACE](https://msdn.microsoft.com/library/ms793861.aspx) que describe la superficie actual.

</dd> <dt>

*hSurfaceTarget* \[ En\]
</dt> <dd>

Controle la [estructura \_ \_ LOCAL de DD SURFACE](https://msdn.microsoft.com/library/ms793861.aspx) que describe la superficie de destino; es decir, la superficie a la que se debe voltear el controlador.

</dd> <dt>

*hSurfaceCurrentLeft* \[ En\]
</dt> <dd>

Identificador de la [estructura \_ \_ LOCAL de DD SURFACE](https://msdn.microsoft.com/library/ms793861.aspx) que describe la superficie izquierda actual.

</dd> <dt>

*hSurfaceTargetLeft* \[ En\]
</dt> <dd>

Identificador de la [estructura \_ \_ LOCAL de DD SURFACE](https://msdn.microsoft.com/library/ms793861.aspx) que describe la superficie de destino izquierda a la que se debe voltear.

</dd> <dt>

*puFlipData* \[ in, out\]
</dt> <dd>

Puntero a una [estructura \_ FLIPDATA de DD](https://msdn.microsoft.com/library/ms794213.aspx) que contiene la información necesaria para realizar el volteo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdFlip devuelve** uno de los siguientes códigos de devolución de llamada.



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

 

 




