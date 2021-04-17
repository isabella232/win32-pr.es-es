---
description: Devuelve el identificador de la API de Microsoft DirectX de modo kernel que se va a usar en las llamadas posteriores a los puntos de entrada de modo kernel que controlan el mecanismo de la API de DirectX.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: Función NtGdiDdGetDxHandle (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDxHandle
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1b304216c518765be73d9f3a3e63d39ec4b37fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659537"
---
# <a name="ntgdiddgetdxhandle-function"></a>NtGdiDdGetDxHandle función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Devuelve el identificador de la API de Microsoft DirectX de modo kernel que se va a usar en las llamadas posteriores a los puntos de entrada de modo kernel que controlan el mecanismo de la API de DirectX.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdGetDxHandle(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ BOOL   bRelease
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDirectDraw* \[ de\]
</dt> <dd>

Identificador del objeto DirectDraw propietario de la superficie. Este parámetro es opcional y se puede establecer en **null**.

</dd> <dt>

*hSurface* \[ de\]
</dt> <dd>

Identificador de la superficie para la que se va a devolver un identificador de API de DirectX en modo kernel. Este parámetro es opcional y se puede establecer en **null**.

</dd> <dt>

*bRelease* \[ de\]
</dt> <dd>

Establézcalo en **true** si se debe liberar la interfaz del modo kernel de la API de DirectX. En caso contrario, **false**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un identificador de API de DirectX que se usa en los siguientes puntos de entrada de kernel orientados a API de DirectX.

## <a name="remarks"></a>Observaciones

Si se especifican *hDirectDraw* y *hSurface* , se omite *hSurface* .

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

 

 




