---
description: Devuelve el identificador de la API de Microsoft DirectX en modo kernel que se usará en llamadas posteriores a los puntos de entrada en modo kernel que controlan el mecanismo de LA API de DirectX.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: Función NtGdiDdGetDxHandle (Ntgdi.h)
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
ms.openlocfilehash: 13234c7ebe350f096164f0a5de0bde7a60e819e80899aa87258a76727855b869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331925"
---
# <a name="ntgdiddgetdxhandle-function"></a>Función NtGdiDdGetDxHandle

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios en el sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Devuelve el identificador de la API de Microsoft DirectX en modo kernel que se usará en llamadas posteriores a los puntos de entrada en modo kernel que controlan el mecanismo de LA API de DirectX.

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

*hDirectDraw* \[ En\]
</dt> <dd>

Identificador del objeto DirectDraw que posee la superficie. Este parámetro es opcional y se puede establecer en **NULL.**

</dd> <dt>

*hSurface* \[ En\]
</dt> <dd>

Identificador en superficie para el que se va a devolver un identificador de LA API de DirectX en modo kernel. Este parámetro es opcional y se puede establecer en **NULL.**

</dd> <dt>

*bRelease* \[ En\]
</dt> <dd>

Establezca en **TRUE si** se debe liberar la interfaz de modo kernel de la API de DirectX. De lo contrario, **FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Un identificador de API de DirectX que se usa en puntos de entrada de kernel orientados a la API de DirectX posteriores.

## <a name="remarks"></a>Comentarios

Si se *especifican hDirectDraw* y *hSurface,* se omite *hSurface.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad con clientes de bajo nivel de gráficos](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




