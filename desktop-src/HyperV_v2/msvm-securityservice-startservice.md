---
description: 'Método StartService de la Msvm_SecurityService : inicia el servicio.'
ms.assetid: 59918c15-7216-4cf7-9215-b27532febc72
title: Método StartService de la Msvm_SecurityService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31e16eea84cf61ace11c241b6409a5810f74b8f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111403"
---
# <a name="startservice-method-of-the-msvm_securityservice-class"></a>Método StartService de la clase SecurityService de Msvm \_

inicia el servicio.

## <a name="syntax"></a>Sintaxis


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si se ejecuta correctamente, devuelve 0; de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1703 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SecurityService de Msvm \_**](msvm-securityservice.md)
</dt> </dl>

 

 




