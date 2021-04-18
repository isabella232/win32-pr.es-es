---
description: El \_ subflujo Get obtiene un puntero a una matriz de interfaces ITSubStream que representan las subsecuencias implicadas en el evento.
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: 'Método ITParticipantEvent:: get_SubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8c2944004af31adfb7256376992506eef59b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690490"
---
# <a name="itparticipanteventget_substream-method"></a>ITParticipantEvent:: get ( \_ método de subsecuencia)

\[**obtener \_ La subsecuencia** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El **\_ subflujo Get** obtiene un puntero a una matriz de interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) que representan las subsecuencias implicadas en el evento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppSubStream* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de punteros [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                           | Significado                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>            | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**\_elementos TAPI E \_ noitems**</dt> </dl> | No hay subsecuencias asociadas al evento.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>       | El parámetro *ppSubStream* no es un puntero válido.<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

