---
description: Coloca el servicio en estado iniciado.
ms.assetid: 8977b806-150c-4ddc-a471-3fdafdcb4a55
title: Método StartService de la clase CIM_Service (administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c0e30adbece838cb913f215abedc4aa86a2762d00f046a54bf2717eaeecdb56e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561815"
---
# <a name="startservice-method-of-the-cim_service-class-hyper-v-management"></a>Método StartService de la clase CIM_Service (administración de Hyper-V)

Coloca el servicio en estado iniciado.

> [!Note]
>
> La semántica de este método se superpone con **el método RequestStateChange** que se hereda de [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md). Este método se mantiene porque se ha implementado ampliamente y su semántica simple de "inicio" es cómoda de usar.

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

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

 

 




