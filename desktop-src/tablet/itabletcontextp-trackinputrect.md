---
description: Actualiza el digitalizador de tabletas a coordenadas de asignación de ubicación de ventana.
ms.assetid: 2984b87b-620e-4e5d-a3cc-4c3f4c89bae3
title: ITabletContextP::TrackInputRect (método)
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
ms.openlocfilehash: 400055247583ec0bd2095d5d6f68d8481c69fd6bb4e7f7730344120203655ce2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350575"
---
# <a name="itabletcontextptrackinputrect-method"></a>ITabletContextP::TrackInputRect (método)

Actualiza el digitalizador de tabletas a coordenadas de asignación de ubicación de ventana.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TrackInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*prcInput* \[ out\]
</dt> <dd>

Nuevo rectángulo de ventana de entrada después de actualizar la asignación entre las coordenadas de ventana y digitalizador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                            | Descripción                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Comentarios

Llame a este método cada vez que cambie la ubicación de la ventana en la pantalla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITabletContextP (interfaz)**](itabletcontextp.md)
</dt> </dl>

 

 




