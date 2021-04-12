---
description: Crea una representación del kernel del objeto Microsoft DirectDraw.
ms.assetid: e380f948-35a0-4cf0-9b69-ab2bd4f9a161
title: Función NtGdiDdCreateDirectDrawObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 16dd140c7b205c92b34cb9bd397a4b8d2d3e1a60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152810"
---
# <a name="ntgdiddcreatedirectdrawobject-function"></a>NtGdiDdCreateDirectDrawObject función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Crea una representación del kernel del objeto Microsoft DirectDraw.

## <a name="syntax"></a>Sintaxis


```C++
HANDLE APIENTRY NtGdiDdCreateDirectDrawObject(
  _In_ HDC hdc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HDC* \[ de\]
</dt> <dd>

Cualquier dispositivo de pantalla DC para el que se debe crear el objeto DirectDraw.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, esta función devuelve un identificador a la representación del objeto en modo kernel; en caso contrario, devuelve **null**.

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

[**DdCreateDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject)
</dt> </dl>

 

 
