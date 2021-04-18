---
title: Método INapSystemHealthAgentCallback CompareSoHRequests (NapSystemHealthAgent. h)
description: SHA usa para comparar solicitudes de SoH.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- Método CompareSoHRequests NAP
- Método CompareSoHRequests NAP, interfaz INapSystemHealthAgentCallback
- Interfaz INapSystemHealthAgentCallback NAP, método CompareSoHRequests
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676789"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a>INapSystemHealthAgentCallback:: CompareSoHRequests (método)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

SHA usa el método **INapSystemHealthAgentCallback:: CompareSoHRequests** para comparar solicitudes de SOH.

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

*LHS* \[ de\]
</dt> <dd>

Puntero al [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a la izquierda de la operación de comparación.

</dd> <dt>

*RHS* \[ de\]
</dt> <dd>

Puntero al [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) a la derecha de la operación de comparación.

</dd> <dt>

*isEqual* \[ enuncia\]
</dt> <dd>

Un puntero a un **valor** **booleano** que es true si *LHS* y *RHS* son semánticamente iguales y **false** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                               | Descripción                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | Indica que se completó correctamente.<br/>                         |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | SHA no implementó el método.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método de devolución de llamada lo declara el sistema NAP y se va a implementar con SHA Writer.

SHA debe comparar SOH y devolver **true** si SOH son semánticamente iguales. NapAgent usa esta información para determinar si se debe iniciar un intercambio de SoH debido al cambio de estado del equipo cliente.

Si los Sha han colocado identificadores incrementales o marcas de tiempo en su SoH, SOH puede ser semánticamente igual (es decir, pueden transmitir la misma información de estado), pero pueden ser unidireccionales por bytes. Los Sha deben implementar esta función para comprobar la igualdad semántica de SOH.

Si los Sha no han colocado marcas de tiempo o identificadores en su SOH, pueden optar por no implementar esta función y devolver **e \_ NOTIMPL**. En este caso, NapAgent realiza una comparación de bytes en [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> <dt>

[**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





