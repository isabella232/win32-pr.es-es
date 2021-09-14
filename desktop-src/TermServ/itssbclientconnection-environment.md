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
ms.openlocfilehash: 18018c8f8fc5e7d017809cf5fe109db7c52712c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168634"
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

Si el método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un **valor HRESULT** que indica el error. Los valores posibles incluyen, entre otros, los de la lista siguiente.

<dl> <dt>

PUNTERO \_ E
</dt> <dd>

No se encontró el entorno.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un complemento de orquestación puede llamar a este método para recuperar información del entorno sobre una máquina virtual de destino.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





