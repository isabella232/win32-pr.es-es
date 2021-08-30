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
ms.openlocfilehash: ba9180358f8398060fe7632c0a75b28f61ffb237638b0d121fccefe7cf3c2f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910025"
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

Puntero a la lista de argumentos. En la lista, cada argumento se almacena con su tipo de variante.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDispParams (clase)**](cdispparams.md)
</dt> </dl>

 

 




