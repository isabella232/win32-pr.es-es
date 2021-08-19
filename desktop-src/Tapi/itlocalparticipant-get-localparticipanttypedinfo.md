---
description: El método get LocalParticipantTypedInfo obtiene información del participante, como el nombre del correo electrónico \_ o la ubicación geográfica.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: Método ITLocalParticipant::get_LocalParticipantTypedInfo (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41afb4c55ba769e341b81e5ec1ca721745509ba8bf2bdfd88ae22ebc48bb535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003373"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a>ItLocalParticipant::get \_ LocalParticipantTypedInfo (método)

El **método get \_ LocalParticipantTypedInfo** obtiene información del participante, como el nombre del correo electrónico o la ubicación geográfica.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*InfoType* \[ En\]
</dt> <dd>

[**PARTICIPANTE \_ Identificador DE \_ INFORMACIÓN CON TIPO**](participant-typed-info.md) del tipo de información necesaria.

</dd> <dt>

*ppInfo* \[ out\]
</dt> <dd>

Puntero a un **BSTR** que contendrá la información necesaria después de una devolución correcta del método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

La aplicación debe usar [SysFreeString para](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) liberar la memoria asignada para el *parámetro ppInfo.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITLocalParticipant**](itlocalparticipant.md)
</dt> <dt>

[**INFORMACIÓN \_ CON TIPO DE \_ PARTICIPANTE**](participant-typed-info.md)
</dt> </dl>

 

