---
description: Crea un objeto de superficie de modo kernel que representa el objeto de superficie de modo de usuario al que hace referencia puSurfaceLocal.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: Función NtGdiDdCreateSurfaceObject (Ntgdi. h)
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
ms.openlocfilehash: 5aef9a70897f5a8a46f9c966242d8842c54f9946
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080115"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a>NtGdiDdCreateSurfaceObject función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Crea un objeto de superficie de modo kernel que representa el objeto de superficie de modo de usuario al que hace referencia *puSurfaceLocal*.

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

*hDirectDrawLocal* \[ de\]
</dt> <dd>

Identificador del objeto DirectDraw en modo kernel.

</dd> <dt>

*hSurface* \[ de\]
</dt> <dd>

Identificador anterior de la misma superficie. Se usa si la superficie se vuelve a crear después de un cambio de modo.

</dd> <dt>

*puSurfaceLocal* \[ de\]
</dt> <dd>

Puntero a la [**estructura \_ \_ local del área DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa el objeto de superficie del modo de usuario de DirectDraw con el que se va a asociar la memoria asignada. Consulte la documentación de DDK para obtener más información.

</dd> <dt>

*puSurfaceMore* \[ de\]
</dt> <dd>

Puntero a la [**superficie de la DD \_ \_ más**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) estructura que contiene datos locales adicionales para cada objeto de superficie individual. Consulte la documentación de DDK para obtener más información.

</dd> <dt>

*puSurfaceGlobal* \[ de\]
</dt> <dd>

Puntero a la [**estructura \_ \_ global**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) de la superficie de DD que contiene los datos de la superficie compartidos globalmente con varias superficies. Consulte la documentación de DDK para obtener más información.

</dd> <dt>

*bComplete* \[ de\]
</dt> <dd>

Marca de finalización de objeto en modo kernel. Puede ser uno de los valores siguientes.

<dt>



 REALES


</dt> <dd>

Complete todo el procesamiento relacionado con la representación en modo kernel.

</dd> <dt>



 ES


</dt> <dd>

Cree el objeto, pero no configure datos internos, como el puntero de memoria. Los objetos creados con **false** se pueden adjuntar mediante [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) y se completan mediante una llamada a [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, esta función devuelve un identificador a la representación de la superficie del modo kernel; en caso contrario, devuelve **null**.

## <a name="remarks"></a>Observaciones

Se recomienda que las aplicaciones usen las API de DirectDraw y [Direct3D](../direct3d10/d3d10-graphics-reference.md) para crear y administrar objetos de dispositivo de gráficos. Estas construcciones abstraen el proceso de creación de dispositivos de una manera simplificada y independiente del sistema operativo.

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

[**DdCreateSurfaceObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[**NtGdiDdDeleteSurfaceObject**](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
