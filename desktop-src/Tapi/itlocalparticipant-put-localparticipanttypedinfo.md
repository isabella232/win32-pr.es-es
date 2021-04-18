---
description: El \_ método put LocalParticipantTypedInfo establece la información del participante.
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: 'ITLocalParticipant: método de ut_LocalParticipantTypedInfo de:p (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77809a9a3858b6a098fa3ff6a93878cf38518f92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690648"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a>ITLocalParticipant::p \_ método LocalParticipantTypedInfo UT

El método **Put \_ LocalParticipantTypedInfo** establece la información del participante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*InfoType* \[ de\]
</dt> <dd>

[**Participante \_ Identificador de \_ información con tipo**](participant-typed-info.md) del tipo de información necesaria.

</dd> <dt>

*ppInfo* \[ de\]
</dt> <dd>

**BSTR** que contiene el nuevo valor necesario para la información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

La aplicación debe usar [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para asignar memoria para el parámetro *PpInfo* y usar [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar memoria cuando la variable ya no se necesite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITLocalParticipant**](itlocalparticipant.md)
</dt> <dt>

[**\_información con tipo de participante \_**](participant-typed-info.md)
</dt> </dl>

 

