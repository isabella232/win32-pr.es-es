---
title: Método INapSystemHealthAgentCallback CompareSoHRequests (NapSystemHealthAgent.h)
description: Sha lo usa para comparar las solicitudes de SoH.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- Nap del método CompareSoHRequests
- Método NAP de CompareSoHRequests, interfaz INapSystemHealthAgentCallback
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
ms.openlocfilehash: 3af26786c8ef021794876d8876ae5d8faee65b8cbbfc39b434b000ff502c64c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939440"
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

Puntero a [**SoHRequest a**](/windows/win32/api/naptypes/ns-naptypes-soh) la derecha de la operación de comparación.

</dd> <dt>

*isEqual* \[ out\]
</dt> <dd>

Puntero a un **BOOL que** es **TRUE si** *lhs* y *rhs* son semánticamente iguales y **FALSE en** caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                               | Descripción                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Indica que se completó correctamente.<br/>                         |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Sha no implementó el método.<br/> |



 

## <a name="remarks"></a>Comentarios

El sistema NAP declara este método de devolución de llamada y lo va a implementar el escritor SHA.

Sha debe comparar los SoH y devolver **TRUE** si los SoH son semánticamente iguales. NapAgent usa esta información para determinar si se debe iniciar un intercambio de SoH debido al cambio de estado de la máquina cliente.

Si los SHA han puesto los ID incrementales o las marcas de tiempo en su SoH, los SoH pueden ser semánticamente iguales (es decir, pueden transmitir la misma información de estado), pero pueden ser diferentes en cuanto a bytes. Las SHA deben implementar esta función para comprobar la igualdad semántica de los SoH.

Si los SHA no han puesto marcas de tiempo o identificadores en sus SoH, pueden optar por no implementar esta función y devolver **E \_ NOTIMPL**. En este caso, NapAgent realiza una comparación por bytes en [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                |
| Header<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> <dt>

[**Soh**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





