---
description: El método Skip omite el siguiente número especificado de elementos en la secuencia de enumeración. Este método está oculto a los lenguajes Visual Basic y scripting.
ms.assetid: 7f641354-c3f5-4eb3-ad1c-98abf7694106
title: Método IEnumParticipant::Skip (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a55eb3298578738bb427efd6ab2b830b9a7850668aa3c9fa4712cc1bf48d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660705"
---
# <a name="ienumparticipantskip-method"></a>IEnumParticipant::Skip (método)

\[**Skip** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método Skip** omite el siguiente número especificado de elementos en la secuencia de enumeración. Este método está oculto a los lenguajes Visual Basic y scripting.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*celta* \[ En\]
</dt> <dd>

Número de elementos que se van a omitir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El número de elementos omitido era *celta*.<br/>               |
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | El número de elementos omitido no *era de centígrado.*<br/>           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




