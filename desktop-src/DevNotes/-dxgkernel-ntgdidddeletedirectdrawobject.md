---
description: Destruye un objeto de dispositivo de Microsoft DirectDraw de modo kernel creado previamente.
ms.assetid: 0b2e1bae-8291-4fe4-9528-980680906e0a
title: Función NtGdiDdDeleteDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 9ac10798f83fe7e1a07a0803dd29cfa9cd8b1c98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152808"
---
# <a name="ntgdidddeletedirectdrawobject-function"></a>NtGdiDdDeleteDirectDrawObject función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Destruye un objeto de dispositivo de Microsoft DirectDraw de modo kernel creado previamente.

## <a name="syntax"></a>Sintaxis


```C++
BOOL APIENTRY NtGdiDdDeleteDirectDrawObject(
   HANDLE hDirectDrawLocal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDirectDrawLocal* 
</dt> <dd>

Identificador del objeto de dispositivo DirectDraw en modo kernel.

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

[**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> <dt>

[**DdDeleteDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletedirectdrawobject)
</dt> </dl>

 

 
