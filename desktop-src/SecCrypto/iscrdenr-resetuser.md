---
description: Borra el nombre de usuario del control de tarjeta inteligente.
ms.assetid: fff50db5-0610-4985-94c6-96d7ce990219
title: Método ISCrdEnr::resetUser
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
ms.openlocfilehash: 873872b17684aac3874b82f0570dfac93988356743055088c1916ef3cb41f4a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867905"
---
# <a name="iscrdenrresetuser-method"></a>Método ISCrdEnr::resetUser

El **método resetUser** borra el nombre de usuario del control de tarjeta inteligente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT resetUser();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="remarks"></a>Comentarios

Este método borra de la memoria cualquier nombre de usuario existente y certificado inscrito previamente. Sin embargo, el certificado inscrito anteriormente no se quita de la tarjeta inteligente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr se define como \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::getUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> <dt>

[**ISCrdEnr::setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 




