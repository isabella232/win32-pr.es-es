---
description: Devuelve el número de pases donde el hardware puede realizar las operaciones de combinación especificadas en el estado actual.
ms.assetid: 355dae78-cd65-4fc9-8f08-8e5ae123064b
title: Función NtGdiD3DValidateTextureStageState (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DValidateTextureStageState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 521169773ae46fa3158752e0d80696888c8bffbfe3dd5d3c0068aee944c290ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088045"
---
# <a name="ntgdid3dvalidatetexturestagestate-function"></a>Función NtGdiD3DValidateTextureStageState

\[Esta función está sujeta a cambios con cada revisión del sistema operativo. En su lugar, use Microsoft DirectDraw y Microsoft Direct3DAPIs; estas API aíslan las aplicaciones de estos cambios del sistema operativo y ocultan muchas otras dificultades implicadas en la interacción directa con los controladores de pantalla.\]

Devuelve el número de pases donde el hardware puede realizar las operaciones de combinación especificadas en el estado actual.

## <a name="syntax"></a>Sintaxis


```C++
DWORD APIENTRY NtGdiD3DValidateTextureStageState(
  _Inout_ LPD3DNTHAL_VALIDATETEXTURESTAGESTATEDATA pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pData* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**D3DNVALIDTEXTURESTAGESTATEDATA \_**](/windows-hardware/drivers/ddi/) que contiene la información necesaria para que el controlador determine y devuelva el número de pases necesarios para realizar las operaciones de combinación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**NtGdiD3DValidateTextureStageState** devuelve uno de los siguientes códigos de devolución de llamada.



| Código devuelto                                                                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CONTROLADOR DDHAL \_ \_ MANIPULADO**</dt> </dl>    | El controlador ha realizado la operación y ha devuelto un código de retorno válido para esa operación. Si este código es correcto para \_ DD, DirectDraw o Direct3D continúa con la función . De lo contrario, DirectDraw o Direct3D devuelven el código de error proporcionado por el controlador y anulan la función.<br/>                                                                                 |
| <dl> <dt>**CONTROLADOR DDHAL \_ \_ NO CONTROLADA**</dt> </dl> | El controlador no tiene ningún comentario sobre la operación solicitada. Si el controlador debe haber implementado una devolución de llamada determinada, DirectDraw o Direct3D notifica una condición de error. De lo contrario, DirectDraw o Direct3D controla la operación como si la devolución de llamada del controlador no se hubiera definido mediante la ejecución de la implementación independiente del dispositivo DirectDraw o Direct3D.<br/> |



 

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

 

 
