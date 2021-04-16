---
description: Borra el nombre de usuario del control de tarjeta inteligente.
ms.assetid: fff50db5-0610-4985-94c6-96d7ce990219
title: 'ISCrdEnr:: resetuser (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.resetUser
- SCrdEnr.resetUser
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3b00721229890f82b00e7e7a41ccb8796a81b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669656"
---
# <a name="iscrdenrresetuser-method"></a>ISCrdEnr:: resetuser (método)

El método **resetuser** borra el nombre de usuario del control de tarjeta inteligente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT resetUser();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="remarks"></a>Observaciones

Este método borra cualquier nombre de usuario existente y el certificado inscrito previamente de la memoria. No obstante, el certificado inscrito previamente no se quita de la tarjeta inteligente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr:: getUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> <dt>

[**ISCrdEnr::setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 




