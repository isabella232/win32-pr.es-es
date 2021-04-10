---
description: Vuelve a habilitar un objeto de dispositivo en modo kernel de Microsoft DirectDraw después de un cambio de modo.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: Función NtGdiDdReenableDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReenableDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: afd736317ecdf802cb418e81063b622db43f0651
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153329"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a>NtGdiDdReenableDirectDrawObject función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Vuelve a habilitar un objeto de dispositivo en modo kernel de Microsoft DirectDraw después de un cambio de modo.

## <a name="syntax"></a>Sintaxis


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDirectDrawLocal* \[ de\]
</dt> <dd>

Objeto DirectDraw que debe volver a habilitarse.

</dd> <dt>

*pubNewMode* \[ in, out\]
</dt> <dd>

Puntero a un valor BOOLEANO que se rellenará con un valor que represente si el modo de presentación cambió.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente (el dispositivo se puede volver a habilitar), esta función devuelve **true**. En caso contrario (por ejemplo, se ha cambiado el controlador de pantalla), devuelve **false**.

## <a name="remarks"></a>Observaciones

Una vez que se ha vuelto a habilitar el objeto, se pueden volver a consultar las capacidades del dispositivo mediante una llamada a [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).

Se recomienda que las aplicaciones usen las API DirectDraw o [Direct3D](../direct3d10/d3d10-graphics-reference.md) versión 8, que automatizan y abstraen este proceso de forma independiente del sistema operativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con clientes de nivel inferior de gráficos](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdReenableDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
