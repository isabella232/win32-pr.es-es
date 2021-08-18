---
description: Destruye un objeto de dispositivo Microsoft DirectDraw en modo kernel creado previamente.
ms.assetid: 0b2e1bae-8291-4fe4-9528-980680906e0a
title: Función NtGdiDdDeleteDirectDrawObject (Ntgdi.h)
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
ms.openlocfilehash: 866624e35c5c05afa14692a2e83d1c15293af9435aa68deddf9c602b80820708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956554"
---
# <a name="ntgdidddeletedirectdrawobject-function"></a>Función NtGdiDdDeleteDirectDrawObject

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Destruye un objeto de dispositivo Microsoft DirectDraw en modo kernel creado previamente.

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

Controle el objeto de dispositivo DirectDraw en modo kernel.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, esta función devuelve **TRUE**; de lo contrario, **devuelve FALSE.**

## <a name="remarks"></a>Comentarios

Se recomienda que las aplicaciones usen las API de DirectDraw y [Direct3D](../direct3d10/d3d10-graphics-reference.md) para crear y administrar objetos de dispositivos gráficos. Estas construcciones abstrae el proceso de creación de dispositivos de una manera simplificada e independiente del sistema operativo.

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

[**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> <dt>

[**DdDeleteDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletedirectdrawobject)
</dt> </dl>

 

 
