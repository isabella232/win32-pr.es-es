---
description: Libera el contexto de dispositivo (DC) creado anteriormente para el objeto de superficie de Microsoft DirectDraw en modo kernel indicado.
ms.assetid: 98def2a1-878d-4776-a519-32cb70107338
title: Función NtGdiDdReleaseDC (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReleaseDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: daa4cad2f6f3937ebe29b3996ebbaa72b894ee743f97222cb1f6e2ff61f7dbb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824915"
---
# <a name="ntgdiddreleasedc-function"></a>Función NtGdiDdReleaseDC

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios en el sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Libera el contexto de dispositivo (DC) creado anteriormente para el objeto de superficie de Microsoft DirectDraw en modo kernel indicado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL APIENTRY NtGdiDdReleaseDC(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSurface* \[ En\]
</dt> <dd>

Identificador del objeto de superficie DirectDraw en modo kernel creado anteriormente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, esta función **devuelve TRUE**; de lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Comentarios

Las aplicaciones que necesitan obtener un controlador de dominio para una superficie de DirectDraw pueden usar [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc), que expone esta funcionalidad de una manera independiente del sistema operativo.

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

[**DdReleaseDC**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreleasedc)
</dt> </dl>

 

 
