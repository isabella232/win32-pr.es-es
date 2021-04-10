---
description: Notifica al controlador cuando Microsoft DirectDraw está invierte hacia o desde una superficie de Windows Interfaz de dispositivo gráfico (GDI).
ms.assetid: e79be33a-24bc-477b-bc67-395fff74309c
title: Función NtGdiDdFlipToGDISurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlipToGDISurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7e233bddf72c79507eab1fcefbf3de66460d228e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153081"
---
# <a name="ntgdiddfliptogdisurface-function"></a>NtGdiDdFlipToGDISurface función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Notifica al controlador cuando Microsoft DirectDraw está invierte hacia o desde una superficie de Windows Interfaz de dispositivo gráfico (GDI).

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdFlipToGDISurface(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_FLIPTOGDISURFACEDATA puFlipToGDISurfaceData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDirectDraw* \[ de\]
</dt> <dd>

Identificador del objeto DirectDraw en modo kernel creado previamente.

</dd> <dt>

*puFlipToGDISurfaceData* \[ in, out\]
</dt> <dd>

Puntero a una estructura [DD \_ FLIPTOGDISURFACEDATA](https://msdn.microsoft.com/library/ms793922.aspx) que contiene la información de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdFlipToGDISurface** devuelve uno de los siguientes códigos de devolución de llamada.



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

 

 




