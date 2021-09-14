---
description: El método Skip omite un número especificado de pines en la secuencia de enumeración. Este método implementa el método IEnumPins::Skip.
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: Método CEnumPins.Skip (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1865453a89130303f28f338d8b7567e856c64173
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255531"
---
# <a name="cenumpinsskip-method"></a>CEnumPins.Skip (método)

El método omite un número especificado de pines en `Skip` la secuencia de enumeración. Este método implementa el [**método IEnumPins::Skip.**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cPins* 
</dt> <dd>

Número de pines que se omitirán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                | Descripción                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Se omite más allá del final de la secuencia.<br/>                                       |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Correcto.<br/>                                                                    |
| <dl> <dt>**VFW \_ E \_ ENUM \_ OUT \_ OF \_ SYNC**</dt> </dl> | El estado del filtro ha cambiado y ahora es incoherente con el enumerador.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CEnumPins (clase)**](cenumpins.md)
</dt> </dl>

 

 




