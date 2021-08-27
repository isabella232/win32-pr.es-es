---
title: Propiedad ITsSbEnvironment Name
description: Recupera un valor que indica el nombre del entorno que hospeda el equipo de destino.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Nombre de propiedad Servicios de Escritorio remoto
- Propiedad Name Servicios de Escritorio remoto , interfaz ITsSbEnvironment
- Interfaz ITsSbEnvironment Servicios de Escritorio remoto , propiedad Name
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
ms.openlocfilehash: 0d60f64cf8bc350ca80072b2c7a43ecabf2fbe5d4650188b7d5a5e5c05a4fbc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072205"
---
# <a name="itssbenvironmentname-property"></a>Propiedad ITsSbEnvironment::Name

Recupera un valor que indica el nombre del entorno que hospeda el equipo de destino.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a una variable **BSTR** que contiene el nombre del entorno.

## <a name="remarks"></a>Comentarios

Este método devuelve una cadena que no usa directamente Conexión a Escritorio remoto Broker (Agente de conexión a Escritorio remoto). Agente de conexión a Escritorio remoto pasa esta cadena a los complementos de recursos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





