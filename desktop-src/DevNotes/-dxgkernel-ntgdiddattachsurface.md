---
description: Asocia dos representaciones de superficie en modo kernel.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: Función NtGdiDdAttachSurface (Ntgdi.h)
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
ms.openlocfilehash: 8ec07f539cfa2a99338d8366f10f7c3d79dbdd5ef26a6de0ee0296941e2c84ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088035"
---
# <a name="ntgdiddattachsurface-function"></a>Función NtGdiDdAttachSurface

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios en el sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Asocia dos representaciones de superficie en modo kernel.

## <a name="syntax"></a>Sintaxis


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hSurfaceFrom* \[ En\]
</dt> <dd>

Identificador del objeto de superficie en modo kernel que será el punto inicial de los nuevos datos adjuntos.

</dd> <dt>

*hSurfaceTo* \[ En\]
</dt> <dd>

Controle el objeto de superficie en modo kernel que será el punto final de los nuevos datos adjuntos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiDdAttachSurface** devuelve una de las siguientes opciones:



| Código devuelto                                                                          | Descripción                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**Verdad**</dt> </dl>  | La llamada de función se ha realiza correctamente.<br/> |
| <dl> <dt>**Falso**</dt> </dl> | Error en la llamada de función.<br/>    |



 

## <a name="remarks"></a>Comentarios

Consulte el kit de desarrollo de software (SDK) de DirectDraw y el Kit de desarrollo de controladores (DDK) para obtener una descripción completa de los datos adjuntos de la superficie.

> [!Note]  
> Al igual que con otros datos adjuntos de superficie, los datos adjuntos resultantes son un únicos. Después de llamar a esta función, *hSurfaceTo* no se adjuntará a *hSurfaceFrom*.

 

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

 

 




