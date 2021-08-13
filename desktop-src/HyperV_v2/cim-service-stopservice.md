---
description: Marca el ritmo del servicio en estado detenido.
ms.assetid: d7469643-bccc-4f55-b2fc-d2bc2e392d84
title: Método StopService de la clase CIM_Service (administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b36cab1054e99ac306fb1b21fe9f08e0820974a0883e90655a180b07035b7f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647593"
---
# <a name="stopservice-method-of-the-cim_service-class-hyper-v-management"></a>Método StopService de la clase CIM_Service (administración de Hyper-V)

Marca el ritmo del servicio en estado detenido.

> [!Note]
>
> La semántica de este método se superpone con **el método RequestStateChange** que se hereda de [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md). Este método se mantiene porque se ha implementado ampliamente y su semántica simple de "detenerse" resulta práctica de usar.

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Servicio \_ CIM**](cim-service.md)
</dt> </dl>

 

 




