---
description: El método siguiente obtiene el siguiente número de elementos especificado en la secuencia de enumeración. Este método está oculto en Visual Basic y en los lenguajes de scripting.
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: 'IEnumParticipant:: Next (método) (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89586370d01aaac54f05242e0eb3c53eb938c47b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691010"
---
# <a name="ienumparticipantnext-method"></a>IEnumParticipant:: Next (método)

\[**Next** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **siguiente** obtiene el siguiente número de elementos especificado en la secuencia de enumeración. Este método está oculto en Visual Basic y en los lenguajes de scripting.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Next(
  [in]  ULONG         celt,
  [out] ITParticipant **ppElements,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Celt* \[ de\]
</dt> <dd>

Número de elementos solicitados.

</dd> <dt>

*ppElements* \[ enuncia\]
</dt> <dd>

Puntero a las interfaces de [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) .

</dd> <dt>

*pceltFetched* \[ enuncia\]
</dt> <dd>

Puntero al número de elementos proporcionados realmente. Puede ser **null** si *Celt* es uno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método devolvió un número de elementos de *Celt* .<br/>           |
| <dl> <dt>**S \_ false**</dt> </dl>       | El número de elementos restantes era menor que *Celt*.<br/>   |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *ppElements* no es un puntero válido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

TAPI llama al método [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) en la interfaz [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) devuelta por **IEnumParticipant:: Next**. La aplicación debe llamar a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en la interfaz **ITAgentHandler** para liberar recursos asociados a ella.

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

 

