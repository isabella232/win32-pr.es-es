---
description: El método Unadvise quita una solicitud de aviso.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: Método CAMSchedule.Unadvise (Dsschedule.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bc9b1c964d698e1c1323846c7a25a29f60c0cd71009fbb60f1a09a6757b50b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057605"
---
# <a name="camscheduleunadvise-method"></a>Método CAMSchedule.Unadvise

El `Unadvise` método quita una solicitud de asesoramiento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwAdviseCookie* 
</dt> <dd>

Identificador de la solicitud de asesoramiento, devuelto por el [**método CAMSchedule::AddAdvisePacket.**](camschedule-addadvisepacket.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                             | Descripción          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | No encontrado<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Correcto<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Dsschedule.h (incluir Secuencias.h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CLASE CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




