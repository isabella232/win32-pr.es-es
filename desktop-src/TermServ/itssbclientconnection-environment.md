---
title: Propiedad de entorno ITsSbClientConnection
description: Recupera un objeto que contiene información sobre el entorno que hospeda el equipo de destino.
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de propiedades de entorno
- Propiedad de entorno Servicios de Escritorio remoto, interfaz ITsSbClientConnection
- Servicios de Escritorio remoto de la interfaz ITsSbClientConnection, propiedad de entorno
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491615"
---
# <a name="itssbclientconnectionenvironment-property"></a>ITsSbClientConnection:: Environment (propiedad)

Recupera un objeto que contiene información sobre el entorno que hospeda el equipo de destino. Por ejemplo, en un escenario de escritorio virtual, este objeto contiene información sobre el equipo que hospeda la máquina virtual.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a>Valor de propiedad

Un puntero a un puntero a un objeto de entorno [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) .

## <a name="error-codes"></a>Códigos de error

Si el método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un valor **HRESULT** que indica el error. Los valores posibles incluyen, entre otros, los que aparecen en la lista siguiente.

<dl> <dt>

\_puntero E
</dt> <dd>

No se encontró el entorno.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un complemento de orquestación puede llamar a este método para recuperar información de entorno sobre una máquina virtual de destino.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





