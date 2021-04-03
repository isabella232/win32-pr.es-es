---
description: Quita los datos adjuntos creados con NtGdiDdAttachSurface entre dos objetos de superficie de modo kernel.
ms.assetid: 28037b42-a00c-4063-93ee-5d71761a95d8
title: Función NtGdiDdUnattachSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnattachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4513020a40c9b704e0b84e1a8b1c582be95db78f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998110"
---
# <a name="ntgdiddunattachsurface-function"></a>NtGdiDdUnattachSurface función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Quita los datos adjuntos creados con [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)entre dos objetos de superficie de modo kernel.

## <a name="syntax"></a>Sintaxis


```C++
VOID APIENTRY NtGdiDdUnattachSurface(
  _In_ HANDLE hSurface,
  _In_ HANDLE hSurfaceAttached
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSurface* \[ de\]
</dt> <dd>

Objeto de superficie de modo kernel que se pasó como parámetro hSurfaceFrom a [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md).

</dd> <dt>

*hSurfaceAttached* \[ de\]
</dt> <dd>

Objeto de superficie de modo kernel que se pasó como parámetro hSurfaceTo a [ **NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdUnattachSurface** devuelve uno de los siguientes códigos de devolución de llamada.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_controlador DDHAL \_ controlado**</dt> </dl>    | El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación. Si este código es DD \_ Aceptar, DirectDraw o Direct3D continúa con la función. De lo contrario, DirectDraw o Direct3D devuelve el código de error proporcionado por el controlador y anula la función.<br/>                                                                                 |
| <dl> <dt>**\_NOTHANDLED del controlador DDHAL \_**</dt> </dl> | El controlador no tiene ningún comentario en la operación solicitada. Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D informa de una condición de error. De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido ejecutando la implementación independiente de dispositivos DirectDraw o Direct3D.<br/> |



 

## <a name="remarks"></a>Observaciones

Se recomienda que las aplicaciones usen la API de DirectDraw, que controla los datos adjuntos de la superficie de una manera de nivel superior.

No es necesario llamar a esta función, ya que el kernel destruirá automáticamente todos los datos adjuntos cuando se llame a [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) .

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

 

 




