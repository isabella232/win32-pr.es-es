---
title: Método GetUserAssignment de la Win32_RDMSVirtualDesktop clase
description: Recupera el nombre de usuario y el nombre de dominio del usuario asignado al escritorio virtual.
ms.assetid: 1887c49d-85df-4fb4-9b40-42fb7763bf95
ms.tgt_platform: multiple
keywords:
- Método GetUserAssignment Servicios de Escritorio remoto
- Método GetUserAssignment Servicios de Escritorio remoto , Win32_RDMSVirtualDesktop clase
- Win32_RDMSVirtualDesktop clase Servicios de Escritorio remoto , método GetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87293a471bb4f69b3f4c57de0f964fa0daa043cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374731"
---
# <a name="getuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Método GetUserAssignment de la clase \_ RDMSVirtualDesktop de Win32

Recupera el nombre de usuario y el nombre de dominio del usuario asignado al escritorio virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetUserAssignment(
  [out] string UserName,
  [out] string UserDomain
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UserName* \[ out\]
</dt> <dd>

Recibe el nombre de usuario.

</dd> <dt>

*UserDomain* \[ out\]
</dt> <dd>

Recibe el nombre de dominio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi.

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

[**RDMSVirtualDesktop de Win32 \_**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





