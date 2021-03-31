---
description: Crea un contexto de dispositivo (DC) para la superficie especificada.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: Función NtGdiDdGetDC (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4f930334f0712107d5651a22b35d6917c7977011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153080"
---
# <a name="ntgdiddgetdc-function"></a>NtGdiDdGetDC función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Crea un contexto de dispositivo (DC) para la superficie especificada.

## <a name="syntax"></a>Sintaxis


```C++
HDC APIENTRY NtGdiDdGetDC(
  _In_ HANDLE       hSurface,
  _In_ PALETTEENTRY *puColorTable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSurface* \[ de\]
</dt> <dd>

Identificador de una superficie de DirectDraw en modo kernel previamente devuelta por [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) o [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).

</dd> <dt>

*puColorTable* \[ de\]
</dt> <dd>

Puntero a una tabla de colores de invalidación para el controlador de dominio devuelto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, esta función devuelve una **HDC**; válida. en caso contrario, devuelve **null**.

## <a name="remarks"></a>Observaciones

Solo se permite un DC por superficie en un momento dado. Las llamadas posteriores a **NtGdiDdGetDC** producirán un error hasta que se libere el controlador de dominio anterior.

Se recomienda que las aplicaciones llamen a [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) en su lugar, lo que proporciona la misma funcionalidad de una manera independiente del sistema operativo.

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

[**DdGetDC**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
