---
description: Adjunta dos representaciones de superficie en modo kernel.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: Función NtGdiDdAttachSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAttachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a3d099e7b3a3106e0e1e4285b37d2ea205baf3d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659427"
---
# <a name="ntgdiddattachsurface-function"></a>NtGdiDdAttachSurface función)

\[Esta función está sujeta a cambios en cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades para interactuar directamente con los controladores de pantalla.\]

Adjunta dos representaciones de superficie en modo kernel.

## <a name="syntax"></a>Sintaxis


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSurfaceFrom* \[ de\]
</dt> <dd>

Identificador del objeto de superficie de modo kernel que será el punto de inicio de los nuevos datos adjuntos.

</dd> <dt>

*hSurfaceTo* \[ de\]
</dt> <dd>

Identificador del objeto de superficie de modo kernel que será el punto final de los nuevos datos adjuntos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdAttachSurface** devuelve uno de los siguientes:



| Código devuelto                                                                          | Descripción                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**REALES**</dt> </dl>  | La llamada de función se realizó correctamente.<br/> |
| <dl> <dt>**ES**</dt> </dl> | Error en la llamada de función.<br/>    |



 

## <a name="remarks"></a>Observaciones

Vea el kit de desarrollo de software (SDK) de DirectDraw y el kit de desarrollo de controladores (DDK) para obtener una descripción completa de los datos adjuntos de la superficie.

> [!Note]  
> Como con otros datos adjuntos de la superficie, los datos adjuntos resultantes son unidireccionales. Después de llamar a esta función, *hSurfaceTo* no se adjuntará a *hSurfaceFrom*.

 

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

 

 




