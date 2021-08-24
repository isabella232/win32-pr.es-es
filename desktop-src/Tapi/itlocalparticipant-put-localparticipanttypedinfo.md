---
description: El método put \_ LocalParticipantTypedInfo establece la información del participante.
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: Método ITLocalParticipant::p ut_LocalParticipantTypedInfo (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acca83d7ad68ed0974aaa2e7d4fb4755c11939d0711473c406cb09d78451ac41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774905"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a>MÉTODO ITLocalParticipant::p ut \_ LocalParticipantTypedInfo

El **método put \_ LocalParticipantTypedInfo** establece la información del participante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*InfoType* \[ En\]
</dt> <dd>

[**PARTICIPANTE \_ Identificador DE \_ INFORMACIÓN CON TIPO**](participant-typed-info.md) del tipo de información necesaria.

</dd> <dt>

*ppInfo* \[ En\]
</dt> <dd>

**BSTR que** contiene el nuevo valor necesario para la información.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

La aplicación debe usar [SysAllocString para](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) asignar memoria para el parámetro *ppInfo* y usar [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria cuando la variable ya no sea necesaria.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

