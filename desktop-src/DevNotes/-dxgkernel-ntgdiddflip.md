---
description: Hace que se intercambie la memoria de la superficie asociada a las superficies de destino y actuales.
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: Función NtGdiDdFlip (Ntgdi. h)
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
ms.openlocfilehash: 1fd2d6f84f602fd07cc29a0efeae28209cb970a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907214"
---
# <a name="ntgdiddflip-function"></a>NtGdiDdFlip función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Hace que se intercambie la memoria de la superficie asociada a las superficies de destino y actuales.

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

*hSurfaceCurrent* \[ de\]
</dt> <dd>

Identificador de la [estructura \_ \_ local](https://msdn.microsoft.com/library/ms793861.aspx) de la superficie de DD que describe la superficie actual.

</dd> <dt>

*hSurfaceTarget* \[ de\]
</dt> <dd>

Identificador de la [estructura \_ \_ local](https://msdn.microsoft.com/library/ms793861.aspx) de la superficie de DD que describe la superficie de destino; es decir, la superficie en la que se debe voltear el controlador.

</dd> <dt>

*hSurfaceCurrentLeft* \[ de\]
</dt> <dd>

Identificador de la [estructura \_ \_ local del área DD](https://msdn.microsoft.com/library/ms793861.aspx) que describe la superficie izquierda actual.

</dd> <dt>

*hSurfaceTargetLeft* \[ de\]
</dt> <dd>

Identificador de la [estructura \_ \_ local](https://msdn.microsoft.com/library/ms793861.aspx) de la superficie de DD que describe la superficie de destino de la izquierda a la que se va a voltear.

</dd> <dt>

*puFlipData* \[ in, out\]
</dt> <dd>

Puntero a una estructura [DD \_ FLIPDATA](https://msdn.microsoft.com/library/ms794213.aspx) que contiene la información necesaria para realizar el volteo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdFlip** devuelve uno de los siguientes códigos de devolución de llamada.



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

 

 




