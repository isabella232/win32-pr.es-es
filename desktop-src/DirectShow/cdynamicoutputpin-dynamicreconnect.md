---
description: El método DynamicReconnect realiza una reconexión dinámica con un nuevo tipo de medio. La reconexión puede producirse mientras se ejecuta el gráfico de filtros.
ms.assetid: 1fe9f1cc-1f5d-407e-8c80-fea6cd1cb16f
title: Método CDynamicOutputPin.DynamicReconnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DynamicReconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd595748380a35f74e591283ed3d03273c683e97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061735"
---
# <a name="cdynamicoutputpindynamicreconnect-method"></a>Método CDynamicOutputPin.DynamicReconnect

El `DynamicReconnect` método realiza una reconexión dinámica con un nuevo tipo de medio. La reconexión puede producirse mientras se ejecuta el gráfico de filtros.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DynamicReconnect(
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntero a una [**estructura \_ AM MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                            | Descripción                                                                                                                                         |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Correcto.<br/>                                                                                                                                 |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Error. Posiblemente, el filtro propietario no llamó [**al método CDynamicOutputPin::SetConfigInfo.**](cdynamicoutputpin-setconfiginfo.md)<br/> |



 

## <a name="remarks"></a>Observaciones

Se debe llamar a este método desde el mismo subproceso que entrega datos al pin. Una vez que se llama a este método, no se pueden entregar ejemplos con el tipo de medio anterior. El autor de la llamada debe asegurarse de que no hay ninguna muestra antigua pendiente.

Llame [**a CDynamicOutputPin::StartUsingOutputPin antes**](cdynamicoutputpin-startusingoutputpin.md) de llamar a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDynamicOutputPin (clase)**](cdynamicoutputpin.md)
</dt> </dl>

 

 




