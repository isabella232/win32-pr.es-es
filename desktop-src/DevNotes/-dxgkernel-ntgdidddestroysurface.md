---
description: Destruye un objeto de superficie de Microsoft DirectDraw en modo kernel asignado previamente.
ms.assetid: 65419fce-9e82-4621-9906-832144888a3b
title: Función NtGdiDdDestroySurface (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroySurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1ec5538e7aea7abd938cb57dc3dfba9c51e7c6c60f81630bf6665c1ee467ed24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956514"
---
# <a name="ntgdidddestroysurface-function"></a>Función NtGdiDdDestroySurface

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Destruye un objeto de superficie de Microsoft DirectDraw en modo kernel asignado previamente.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiDdDestroySurface(
  _In_ HANDLE hSurface,
  _In_ BOOL   bRealDestroy
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSurface* \[ En\]
</dt> <dd>

Identificador del objeto de superficie en modo kernel asignado previamente.

</dd> <dt>

*bRealDestroy* \[ En\]
</dt> <dd>

Especifica cómo destruir la superficie. Puede ser uno de los siguientes valores.

<dt>



 (TRUE)


</dt> <dd>

Destruir la superficie y liberar memoria de vídeo.

</dd> <dt>



 (FALSE)


</dt> <dd>

Libera la memoria de vídeo, pero deja la superficie en un estado sin inicializar.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdDestroySurface devuelve** uno de los siguientes códigos de devolución de llamada.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CONTROLADOR DDHAL \_ \_ MANIPULADO**</dt> </dl>    | El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación. Si este código es correcto para \_ DD, DirectDraw o Direct3D continúa con la función . De lo contrario, DirectDraw o Direct3D devuelven el código de error proporcionado por el controlador y anulan la función.<br/>                                                                                 |
| <dl> <dt>**CONTROLADOR DDHAL \_ \_ NO CONTROLADA**</dt> </dl> | El controlador no tiene ningún comentario sobre la operación solicitada. Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D notifica una condición de error. De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido mediante la ejecución de la implementación independiente del dispositivo DirectDraw o Direct3D.<br/> |



 

## <a name="remarks"></a>Comentarios

Se recomienda que las aplicaciones usen las API de DirectDraw y Direct3D para crear y destruir superficies en lugar de esta función.

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

 

 




