---
description: Lo usan los tiempos de ejecución de Microsoft DirectDraw y Microsoft Direct3D para obtener información del controlador sobre su estado actual.
ms.assetid: a7697e0c-9485-4a9c-b211-67ce07dc3604
title: Función NtGdiD3DGetDriverState (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DGetDriverState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: c88f2fde4d848aac5ecae3c60aef77d4c6b783cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659351"
---
# <a name="ntgdid3dgetdriverstate-function"></a>NtGdiD3DGetDriverState función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use DirectDraw y Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Lo usan los tiempos de ejecución de Microsoft DirectDraw y Microsoft Direct3D para obtener información del controlador sobre su estado actual.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiD3DGetDriverState(
  _Inout_ PDD_GETDRIVERSTATEDATA pdata
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdata* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**DD \_ GETDRIVERSTATEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getdriverstatedata) que describe el estado del controlador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiD3DGetDriverState** devuelve uno de los siguientes códigos de devolución de llamada.



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

 

 
