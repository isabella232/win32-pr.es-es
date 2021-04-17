---
description: El método SKIP omite el siguiente número de elementos especificado en la secuencia de enumeración. Este método está oculto en Visual Basic y en los lenguajes de scripting.
ms.assetid: 7f641354-c3f5-4eb3-ad1c-98abf7694106
title: 'IEnumParticipant:: Skip (método) (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc406a69c126c25b1c554679595868a595b839b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690705"
---
# <a name="ienumparticipantskip-method"></a>IEnumParticipant:: Skip (método)

\[**SKIP** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **SKIP** omite el siguiente número de elementos especificado en la secuencia de enumeración. Este método está oculto en Visual Basic y en los lenguajes de scripting.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Celt* \[ de\]
</dt> <dd>

Número de elementos que se van a omitir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El número de elementos omitidos era *Celt*.<br/>               |
| <dl> <dt>**S \_ false**</dt> </dl>       | El número de elementos omitidos no era *Celt*.<br/>           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




