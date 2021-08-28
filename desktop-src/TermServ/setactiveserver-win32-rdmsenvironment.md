---
title: Método SetActiveServer de la Win32_RDMSEnvironment clase
description: Establece el FQDN del entorno Escritorio remoto Management Services (RDMS) en el nodo actual.
ms.assetid: ed7b71cf-c3a4-4d2f-856a-31332f94fac9
ms.tgt_platform: multiple
keywords:
- Método SetActiveServer Servicios de Escritorio remoto
- Método SetActiveServer Servicios de Escritorio remoto , Win32_RDMSEnvironment clase
- Win32_RDMSEnvironment clase Servicios de Escritorio remoto , método SetActiveServer
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68a8f9c6661e78932893ef25278234fb4c944d22297cb87cc95aebe9bc8d8ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865495"
---
# <a name="setactiveserver-method-of-the-win32_rdmsenvironment-class"></a>Método SetActiveServer de la clase \_ RDMSEnvironment de Win32

Establece el FQDN del entorno Escritorio remoto Management Services (RDMS) en el nodo actual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetActiveServer();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ de CIMv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_RDMSEnvironment de Win32**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





