---
description: Bloquea una tarjeta inteligente conectada para su uso exclusivo.
ms.assetid: c39a7cfe-04b6-4298-927a-4280664cf769
title: 'ISCardManage:: SCardLock (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardLock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2198f512fde90d1c79173f5151fc4f759944500a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276273"
---
# <a name="iscardmanagescardlock-method"></a>ISCardManage:: SCardLock (método)

\[El método **SCardLock** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **SCardLock** bloquea una [*tarjeta inteligente*](../secgloss/s-gly.md) conectada para su uso exclusivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SCardLock();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles:



| Código devuelto                                                                            | Descripción                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>   | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | No se pudo completar la operación.<br/>     |



 

## <a name="remarks"></a>Observaciones

Para liberar el uso exclusivo de la tarjeta inteligente conectada, llame a [**SCardUnlock**](iscardmanage-scardunlock.md).

Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardManage**](iscardmanage.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**SCardUnlock**](iscardmanage-scardunlock.md)
</dt> </dl>

 

 
