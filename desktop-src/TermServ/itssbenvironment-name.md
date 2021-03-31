---
title: Propiedad nombre de ITsSbEnvironment
description: Recupera un valor que indica el nombre del entorno que hospeda el equipo de destino.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Propiedad Nombre Servicios de Escritorio remoto
- Propiedad Nombre Servicios de Escritorio remoto, interfaz ITsSbEnvironment
- Servicios de Escritorio remoto de la interfaz ITsSbEnvironment, propiedad Name
topic_type:
- apiref
api_name:
- ITsSbEnvironment.Name
- ITsSbEnvironment.get_Name
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b5ac2fd725ec07102c08e93b2bfb39dabe701ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996134"
---
# <a name="itssbenvironmentname-property"></a>ITsSbEnvironment:: Name (propiedad)

Recupera un valor que indica el nombre del entorno que hospeda el equipo de destino.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Un puntero a una variable **BSTR** que contiene el nombre del entorno.

## <a name="remarks"></a>Observaciones

Este método devuelve una cadena que no usa directamente Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto). El agente de conexión a escritorio remoto pasa esta cadena a complementos de recursos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





