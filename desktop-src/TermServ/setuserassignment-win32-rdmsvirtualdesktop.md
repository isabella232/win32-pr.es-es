---
title: Método SetUserAssignment de la Win32_RDMSVirtualDesktop clase
description: Asigna un escritorio virtual a un usuario.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- Método SetUserAssignment Servicios de Escritorio remoto
- Método SetUserAssignment Servicios de Escritorio remoto , Win32_RDMSVirtualDesktop clase
- Win32_RDMSVirtualDesktop clase Servicios de Escritorio remoto , método SetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38f87209ba8c8ebd82637f72cea2e798844e6081cd000f2161ee21681422e40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349416"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Método SetUserAssignment de la clase \_ RDMSVirtualDesktop de Win32

Asigna un escritorio virtual a un usuario.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetUserAssignment(
  [in] string UserName,
  [in] string UserDomain
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UserName* \[ En\]
</dt> <dd>

Nombre de usuario del usuario.

</dd> <dt>

*UserDomain* \[ En\]
</dt> <dd>

Nombre de dominio del usuario.

</dd> </dl>

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

[**RDMSVirtualDesktop de Win32 \_**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





