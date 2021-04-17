---
description: El \_ método get SubStreamFromParticipant permite a una aplicación detectar qué subsecuencias están asociadas a un participante determinado.
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: 'Método ITParticipantSubStreamControl:: get_SubStreamFromParticipant (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0eae68cd62c38348e1a576f114a9e93ac52f9cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681243"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a>ITParticipantSubStreamControl:: get \_ SubStreamFromParticipant (método)

\[**obtener \_ SubStreamFromParticipant** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ SubStreamFromParticipant** permite a una aplicación detectar qué subsecuencias están asociadas a un participante determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pParticipant* \[ de\]
</dt> <dd>

Puntero a la interfaz [**ITParticipant**](itparticipant.md) .

</dd> <dt>

*ppITSubStream* \[ enuncia\]
</dt> <dd>

Puntero a la matriz de punteros de la interfaz [**ITParticipant**](itparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                                 |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *ppITSubStream* no es un puntero válido.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *pParticipant* no apunta a una interfaz válida.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>  | No se pudo obtener acceso a la información del participante de la secuencia.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipantSubStreamControl**](itparticipantsubstreamcontrol.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

