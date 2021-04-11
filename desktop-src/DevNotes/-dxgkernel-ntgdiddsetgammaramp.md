---
description: Establece la rampa gamma del dispositivo.
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: Función NtGdiDdSetGammaRamp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetGammaRamp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 0c5efba67eedbd6e70f1e0682f42c1855948cecd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152806"
---
# <a name="ntgdiddsetgammaramp-function"></a>NtGdiDdSetGammaRamp función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Establece la rampa gamma del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
BOOL APIENTRY NtGdiDdSetGammaRamp(
  _In_ HANDLE hDirectDraw,
  _In_ HDC    hdc,
  _In_ LPVOID lpGammaRamp
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDirectDraw* \[ de\]
</dt> <dd>

Identificador del objeto de controlador de modo kernel para el que se va a establecer la rampa.

</dd> <dt>

*HDC* \[ de\]
</dt> <dd>

Reservado.

</dd> <dt>

*lpGammaRamp* \[ de\]
</dt> <dd>

Puntero a una matriz de estructuras **DDGAMMARAMP** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **true** si la función se realiza correctamente. De lo contrario, es **null**.

## <a name="remarks"></a>Observaciones

Se recomienda que las aplicaciones usen los métodos **IDirectDrawGammaControl:: SetGammaRamp** o [**IDirect3DDevice9:: SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) en su lugar porque estos métodos ofrecen la misma funcionalidad independiente del sistema operativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con clientes de nivel inferior de gráficos](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
