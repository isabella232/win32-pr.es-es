---
title: Método IMsTscAxEvents OnUserNameAcquired
description: Se llama cuando el control ha adquirido el nombre de usuario.
ms.assetid: 0653B28B-2D46-429F-8A36-5656786C0B26
ms.tgt_platform: multiple
keywords:
- Método OnUserNameAcquired Servicios de Escritorio remoto
- Método OnUserNameAcquired Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnUserNameAcquired
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnUserNameAcquired
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5d77f0eb739daa54f8385112b79f67f279eae9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259031"
---
# <a name="imstscaxeventsonusernameacquired-method"></a>Método IMsTscAxEvents::OnUserNameAcquired

Se llama cuando el control ha adquirido el nombre de usuario.

## <a name="syntax"></a>Sintaxis


```C++
void OnUserNameAcquired(
   BSTR bstrUserName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrUserName* 
</dt> <dd>

Nombre de usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





