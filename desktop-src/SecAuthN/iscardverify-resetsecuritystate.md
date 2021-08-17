---
description: Restablece el contexto de seguridad actual de la tarjeta inteligente.
ms.assetid: fcd55b65-a741-4244-8597-ec61cea3f4b7
title: Método ISCardVerify::ResetSecurityState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ResetSecurityState
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6cf1d27298e5bc37288b209547e82f29cfba1393dc3c654563977fbd3f0bf0ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141068"
---
# <a name="iscardverifyresetsecuritystate-method"></a>Método ISCardVerify::ResetSecurityState

\[El **método ResetSecurityState** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método ResetSecurityState** restablece el contexto [*de seguridad actual*](../secgloss/s-gly.md) de la tarjeta [*inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResetSecurityState();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles:



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Comentarios

Para volver a habilitar el contexto [*de seguridad sin*](../secgloss/s-gly.md) restablecerlo, llame a [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).

Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardVerify**](iscardverify.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardVerify**](iscardverify.md)
</dt> <dt>

[**Desbloquear**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))
</dt> </dl>

 

 
