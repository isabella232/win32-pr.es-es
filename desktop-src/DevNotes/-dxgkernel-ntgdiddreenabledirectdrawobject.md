---
description: Vuelve a habilitar un objeto de dispositivo en modo kernel de Microsoft DirectDraw después de un conmutador de modo.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: Función NtGdiDdReenableDirectDrawObject (Ntgdi.h)
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
ms.openlocfilehash: 808e2e74492b9a3e828e09389e04f0e1e4b09fef9a63fdd7a22d81521b3df30d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045575"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a>Función NtGdiDdReenableDirectDrawObject

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios en el sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Vuelve a habilitar un objeto de dispositivo en modo kernel de Microsoft DirectDraw después de un conmutador de modo.

## <a name="syntax"></a>Sintaxis


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDirectDrawLocal* \[ En\]
</dt> <dd>

Objeto DirectDraw que debe volver a habilitarse.

</dd> <dt>

*pubNewMode* \[ in, out\]
</dt> <dd>

Puntero a una bool que se rellenará con un valor que representa si el modo de presentación ha cambiado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente (se puede volver a habilitar el dispositivo), esta función devuelve **TRUE.** De lo contrario (por ejemplo, se cambió el controlador de pantalla), devuelve **FALSE**.

## <a name="remarks"></a>Comentarios

Una vez que se ha vuelto a habilitar el objeto, las funcionalidades del dispositivo se pueden volver a consultar a través de una llamada a [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).

Se recomienda a las aplicaciones usar las API DirectDraw o [Direct3D](../direct3d10/d3d10-graphics-reference.md) versión 8, que automatizan y abstraen este proceso de una manera independiente del sistema operativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con clientes de bajo nivel de gráficos](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdReenableDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
