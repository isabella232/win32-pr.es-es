---
description: El \_ método get ParticipantFromSubStream permite a una aplicación detectar qué participantes están asociados a un subflujo determinado.
ms.assetid: 0e42b4f0-d5b6-4b33-b7e5-dc525524ece7
title: 'Método ITParticipantSubStreamControl:: get_ParticipantFromSubStream (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a507665e7f81339ce10961d69e08e76f60bb2be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680627"
---
# <a name="itparticipantsubstreamcontrolget_participantfromsubstream-method"></a>ITParticipantSubStreamControl:: get \_ ParticipantFromSubStream (método)

\[**obtener \_ ParticipantFromSubStream** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ ParticipantFromSubStream** permite a una aplicación detectar qué participantes están asociados a un subflujo determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ParticipantFromSubStream(
  [in]  ITSubStream   *pITSubStream,
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pITSubStream* \[ de\]
</dt> <dd>

Puntero a la interfaz [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .

</dd> <dt>

*ppParticipant* \[ enuncia\]
</dt> <dd>

Puntero a la matriz de punteros de la interfaz [**ITParticipant**](itparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                     | Descripción                                                                        |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>            | El método se realizó correctamente.<br/>                                                       |
| <dl> <dt>**\_puntero E**</dt> </dl>       | El parámetro *pITSubStream* o *ppParticipant* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>    | El parámetro *pITSubStream* no apunta a una interfaz válida.<br/>         |
| <dl> <dt>**\_elementos TAPI E \_ noitems**</dt> </dl> | No hay participantes asociados a la subsecuencia.<br/>                |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | No hay memoria suficiente para realizar la operación.<br/>                    |



 

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

 

