---
description: Crea un contexto de dispositivo (DC) para la superficie especificada.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: Función NtGdiDdGetDC (Ntgdi.h)
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
ms.openlocfilehash: 200635ca71ab16a84a137f85be13cc4fdbb6db200e4c0da795d07f945f06e9f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053345"
---
# <a name="ntgdiddgetdc-function"></a>Función NtGdiDdGetDC

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios en el sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

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

*hSurface* \[ En\]
</dt> <dd>

Identificador de una superficie de DirectDraw en modo kernel devuelta anteriormente por [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) o [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).

</dd> <dt>

*puColorTable* \[ En\]
</dt> <dd>

Puntero a una tabla de colores de invalidación para el controlador de dominio devuelto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, esta función devuelve un **HDC válido;** de lo contrario, **devuelve NULL.**

## <a name="remarks"></a>Comentarios

Solo se permite un controlador de dominio por superficie en un momento dado. Las llamadas posteriores **a NtGdiDdGetDC producirán** un error hasta que se libera el controlador de dominio anterior.

En su lugar, se recomienda a las aplicaciones llamar a [IDirectDrawSurface7::GetDC,](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) que proporciona la misma funcionalidad de una manera independiente del sistema operativo.

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

[**DdGetDC**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
