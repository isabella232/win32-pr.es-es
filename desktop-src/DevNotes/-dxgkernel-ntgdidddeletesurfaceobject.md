---
description: NtGdiDdDeleteSurfaceObject elimina un objeto de superficie del modo kernel creado previamente.
ms.assetid: 95ce6c73-7e41-4ac3-b849-9b8f53aa3ac3
title: Función NtGdiDdDeleteSurfaceObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 03988b842aacc29915287490508eb9e9d057e907
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659348"
---
# <a name="ntgdidddeletesurfaceobject-function"></a>NtGdiDdDeleteSurfaceObject función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

**NtGdiDdDeleteSurfaceObject** elimina un objeto de superficie del modo kernel creado previamente.

## <a name="syntax"></a>Sintaxis


```C++
BOOL APIENTRY NtGdiDdDeleteSurfaceObject(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSurface* \[ de\]
</dt> <dd>

Identificador del objeto de superficie de modo kernel creado previamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, esta función devuelve **true**; en caso contrario, devuelve **false**.

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

[**DdDeleteSurfaceObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletesurfaceobject)
</dt> <dt>

[**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md)
</dt> </dl>

 

 
