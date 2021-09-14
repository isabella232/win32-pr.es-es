---
description: 'Constructor CDispParams.CDispParams: método constructor.'
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Constructor CDispParams.CDispParams (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 42f55a57a0f9e06d3001c2638d457fe0b82a914d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361381"
---
# <a name="cdispparamscdispparams-constructor"></a>Constructor CDispParams.CDispParams

Método constructor.

## <a name="syntax"></a>Sintaxis


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nArgs* 
</dt> <dd>

Número de argumentos pasados al método o propiedad.

</dd> <dt>

*pArgs* 
</dt> <dd>

Puntero a la lista de argumentos. En la lista, cada argumento se almacena con su tipo variant.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CDispParams (clase)**](cdispparams.md)
</dt> </dl>

 

 




