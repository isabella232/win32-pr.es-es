---
description: El \_ método get LocalParticipantTypedInfo obtiene información de los participantes, como el nombre de correo electrónico o la ubicación geográfica.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: 'Método ITLocalParticipant:: get_LocalParticipantTypedInfo (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabaf503963c09898c06659884fd3ac3858e704
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690650"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a>ITLocalParticipant:: get \_ LocalParticipantTypedInfo (método)

El método **Get \_ LocalParticipantTypedInfo** obtiene información de los participantes, como el nombre de correo electrónico o la ubicación geográfica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*InfoType* \[ de\]
</dt> <dd>

[**Participante \_ Identificador de \_ información con tipo**](participant-typed-info.md) de tipo de información requerida.

</dd> <dt>

*ppInfo* \[ enuncia\]
</dt> <dd>

Puntero a un **BSTR** que contendrá la información necesaria después de una devolución correcta del método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

La aplicación debe usar [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria asignada para el parámetro *ppInfo* .

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

 

