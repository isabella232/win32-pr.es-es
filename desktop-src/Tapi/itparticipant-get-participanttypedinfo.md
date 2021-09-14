---
description: El método get ParticipantTypedInfo obtiene una representación BSTR del tipo de información necesaria, como \_ PTI \_ EMAILADDRESS.
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: Método ITParticipant::get_ParticipantTypedInfo (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9936f49e6daa05702699487e4313a918c545a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160646"
---
# <a name="itparticipantget_participanttypedinfo-method"></a>ItParticipant::get \_ ParticipantTypedInfo (método)

\[**get \_ ParticipantTypedInfo** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método \_ get ParticipantTypedInfo** obtiene una representación **BSTR** del tipo de información necesaria, como PTI \_ EMAILADDRESS.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*InfoType* \[ En\]
</dt> <dd>

[**PARTICIPANTE \_ Descriptor DE \_ INFORMACIÓN CON TIPO**](participant-typed-info.md) del tipo de información necesaria.

</dd> <dt>

*ppInfo* \[ out\]
</dt> <dd>

Puntero a **la representación BSTR** de la información necesaria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                    | Descripción                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>         | Storage error de información *en ppInfo.*<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>   | El *parámetro InfoType* no es válido.<br/>               |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>      | El *parámetro ppInfo* no es un puntero válido.<br/>       |
| <dl> <dt>**TAPI \_ E \_ NOITEM**</dt> </dl> | TAPI no tiene información sobre el tipo especificado.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | No existe memoria suficiente para realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

La aplicación debe usar [**SysFreeString para**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) liberar la memoria asignada para el *parámetro ppInfo.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                |
| Encabezado<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**INFORMACIÓN \_ CON TIPO DE \_ PARTICIPANTE**](participant-typed-info.md)
</dt> <dt>

[**tipos de medios**](tapimediatype--constants.md)
</dt> </dl>

 

