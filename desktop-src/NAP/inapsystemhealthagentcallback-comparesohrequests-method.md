---
title: Método INapSystemHealthAgentCallback CompareSoHRequests (NapSystemHealthAgent.h)
description: SHA lo usa para comparar las solicitudes SoH.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- Nap del método CompareSoHRequests
- CompareSoHRequests method NAP , INapSystemHealthAgentCallback interface
- INapSystemHealthAgentCallback interface NAP , CompareSoHRequests method
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.CompareSoHRequests
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6713f3de47cfbde6df67662f89ab3c094d0674
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071645"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a>Método INapSystemHealthAgentCallback::CompareSoHRequests

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Sha usa el método **INapSystemHealthAgentCallback::CompareSoHRequests** para comparar las solicitudes de SoH.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CompareSoHRequests(
  [in]  const SoHRequest *lhs,
  [in]  const SoHRequest *rhs,
  [out]       BOOL       *isEqual
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lhs* \[ En\]
</dt> <dd>

Puntero a [**SoHRequest a**](/windows/win32/api/naptypes/ns-naptypes-soh) la izquierda de la operación de comparación.

</dd> <dt>

*rhs* \[ En\]
</dt> <dd>

Puntero a [**SoHRequest a la**](/windows/win32/api/naptypes/ns-naptypes-soh) derecha de la operación de comparación.

</dd> <dt>

*isEqual* \[ out\]
</dt> <dd>

Puntero a un **BOOL que** es **TRUE si** *lhs* y *rhs* son semánticamente iguales y **FALSE** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                               | Descripción                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Indica que se completó correctamente.<br/>                         |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Sha no implementó el método.<br/> |



 

## <a name="remarks"></a>Observaciones

El sistema NAP declara este método de devolución de llamada y lo va a implementar el escritor SHA.

Sha debe comparar los SoH y devolver **TRUE** si los SoHs son semánticamente iguales. NapAgent usa esta información para determinar si se debe iniciar un intercambio de SoH debido al cambio de estado de la máquina cliente.

Si las SHA han puesto los ID incrementales o las marcas de tiempo en su SoH, los SoH pueden ser iguales semánticamente (es decir, pueden transmitir la misma información de estado), pero pueden ser desiguales en cuanto a bytes. Las SHA deben implementar esta función para comprobar la igualdad semántica de los SoH.

Si las SHA no han puesto marcas de tiempo o identificadores en sus soHs, pueden optar por no implementar esta función y devolver **E \_ NOTIMPL**. En este caso, NapAgent realiza una comparación por bytes en [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> <dt>

[**Soh**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





