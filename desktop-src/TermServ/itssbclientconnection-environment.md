---
title: Propiedad ITsSbClientConnection Environment
description: Recupera un objeto que contiene información sobre el entorno que hospeda el equipo de destino.
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- Propiedades de entorno Servicios de Escritorio remoto
- Propiedad environment Servicios de Escritorio remoto , interfaz ITsSbClientConnection
- Interfaz ITsSbClientConnection Servicios de Escritorio remoto , propiedad Environment
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33cc1c3c8a13a21135ee834950e8c0a60d2794cd4b1edb618e5e67c0744fe3e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072215"
---
# <a name="itssbclientconnectionenvironment-property"></a>Propiedad ITsSbClientConnection::Environment

Recupera un objeto que contiene información sobre el entorno que hospeda el equipo de destino. Por ejemplo, en un escenario de escritorio virtual, este objeto contendrá información sobre el equipo que hospeda la máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a un puntero a un objeto de entorno [**ITsSbEnvironment.**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)

## <a name="error-codes"></a>Códigos de error

Si el método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve **un valor HRESULT** que indica el error. Los valores posibles incluyen, entre otros, los de la lista siguiente.

<dl> <dt>

PUNTERO \_ E
</dt> <dd>

No se encontró el entorno.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Un complemento de orquestación puede llamar a este método para recuperar información del entorno sobre una máquina virtual de destino.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





