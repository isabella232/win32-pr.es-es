---
title: Método SetUserAssignment de la clase Win32_RDMSVirtualDesktop
description: Asigna un escritorio virtual a un usuario.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- Método SetUserAssignment Servicios de Escritorio remoto
- Método SetUserAssignment Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de clase Servicios de Escritorio remoto, método SetUserAssignment
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
ms.openlocfilehash: 5f02e1cc935e344edd6a9c52016052e082e08d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676925"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Método SetUserAssignment de la \_ clase RDMSVirtualDesktop de Win32

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

*Nombre de usuario* \[ de\]
</dt> <dd>

Nombre de usuario del usuario.

</dd> <dt>

*UserDomain* \[ de\]
</dt> <dd>

El nombre de dominio del usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | RDMs raíz de \\ CIMv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





