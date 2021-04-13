---
description: Libera el uso exclusivo de la tarjeta inteligente conectada.
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: 'ISCardManage:: SCardUnlock (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardUnlock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90c6b10d407992ae8147998d2d420989cc91e970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276271"
---
# <a name="iscardmanagescardunlock-method"></a>ISCardManage:: SCardUnlock (método)

\[El método **SCardUnlock** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **SCardUnlock** libera el uso exclusivo de la [*tarjeta inteligente*](../secgloss/s-gly.md)conectada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Disposición* \[ de\]
</dt> <dd>

El estado al que se dejará la tarjeta inteligente cuando se lance el bloqueo.

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

**OMITI**
</dt><span id="RESET"></span><span id="reset"></span><dt>

**RESET**
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

**No energía**
</dt><span id="EJECT"></span><span id="eject"></span><dt>

**EXPULSAR**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                  | Descripción                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Operación completada correctamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El parámetro de *disposición* no es válido.<br/> |



 

## <a name="remarks"></a>Observaciones

Para bloquear la tarjeta inteligente conectada, llame a [**SCardLock**](iscardmanage-scardlock.md).

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

[**SCardLock**](iscardmanage-scardlock.md)
</dt> </dl>

 

 
