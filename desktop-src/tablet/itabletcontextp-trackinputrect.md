---
description: Actualiza el digitalizador de Tablet PC a las coordenadas de asignación de ubicación de la ventana.
ms.assetid: 2984b87b-620e-4e5d-a3cc-4c3f4c89bae3
title: 'ITabletContextP:: TrackInputRect (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.TrackInputRect
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 4529263b81933651db35b88262b11e979d39e6f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716905"
---
# <a name="itabletcontextptrackinputrect-method"></a>ITabletContextP:: TrackInputRect (método)

Actualiza el digitalizador de Tablet PC a las coordenadas de asignación de ubicación de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TrackInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*prcInput* \[ enuncia\]
</dt> <dd>

El nuevo rectángulo de la ventana de entrada después de actualizar la asignación entre las coordenadas de ventana y digitalizador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

Llame a este método siempre que cambie la ubicación de la ventana en la pantalla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 




