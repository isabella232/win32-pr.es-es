---
description: Crea un objeto de superficie en modo kernel que representa el objeto de superficie en modo de usuario al que hace referencia puSurfaceLocal.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: Función NtGdiDdCreateSurfaceObject (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7dac10cb5f648cc7281d95bcd83be9983a63abd76208f6f745e1bd6c5ec00b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956544"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a>Función NtGdiDdCreateSurfaceObject

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Crea un objeto de superficie en modo kernel que representa el objeto de superficie en modo de usuario al que hace referencia *puSurfaceLocal.*

## <a name="syntax"></a>Sintaxis


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDirectDrawLocal* \[ En\]
</dt> <dd>

Identificador del objeto DirectDraw en modo kernel.

</dd> <dt>

*hSurface* \[ En\]
</dt> <dd>

Identificador anterior a la misma superficie. Se usa si la superficie se vuelve a crear después de un cambio de modo.

</dd> <dt>

*puSurfaceLocal* \[ En\]
</dt> <dd>

Puntero a la [**estructura \_ \_ LOCAL de DD SURFACE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa el objeto de superficie en modo de usuario DirectDraw al que se va a asociar la memoria asignada. Consulte la documentación del DDK para obtener más información.

</dd> <dt>

*puSurfaceMore* \[ En\]
</dt> <dd>

Puntero a la [**estructura DD \_ SURFACE \_ MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) que contiene datos locales adicionales para cada objeto de superficie individual. Consulte la documentación del DDK para obtener más información.

</dd> <dt>

*puSurfaceGlobal* \[ En\]
</dt> <dd>

Puntero a la [**estructura GLOBAL \_ de DD SURFACE \_**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) que contiene datos de superficie compartidos globalmente con varias superficies. Consulte la documentación del DDK para obtener más información.

</dd> <dt>

*bComplete* \[ En\]
</dt> <dd>

Marca de finalización de objetos en modo kernel. Puede ser uno de los siguientes valores.

<dt>



 (TRUE)


</dt> <dd>

Complete todo el procesamiento relativo a la representación en modo kernel.

</dd> <dt>



 (FALSE)


</dt> <dd>

Cree el objeto , pero no configure datos internos, como el puntero de memoria. Los objetos creados con **FALSE** se pueden adjuntar mediante [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) y se completan mediante una llamada a [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, esta función devuelve un identificador a la representación de la superficie en modo kernel; de lo contrario, **devuelve NULL.**

## <a name="remarks"></a>Comentarios

Se recomienda a las aplicaciones usar las API de DirectDraw y [Direct3D](../direct3d10/d3d10-graphics-reference.md) para crear y administrar objetos de dispositivos gráficos. Estas construcciones abstrae el proceso de creación de dispositivos de una manera simplificada e independiente del sistema operativo.

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

[**DdCreateSurfaceObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[**NtGdiDdDeleteSurfaceObject**](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
