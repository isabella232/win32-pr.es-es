---
title: Método GetVirtualDesktopAssignedToUser de la clase Win32_RDMSVirtualDesktop
description: Recupera el escritorio virtual asignado al usuario especificado.
ms.assetid: cbc22c45-4492-4651-b164-a6fd717c5ab4
ms.tgt_platform: multiple
keywords:
- Método GetVirtualDesktopAssignedToUser Servicios de Escritorio remoto
- Método GetVirtualDesktopAssignedToUser Servicios de Escritorio remoto, clase Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop de clase Servicios de Escritorio remoto, método GetVirtualDesktopAssignedToUser
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopAssignedToUser
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcbbbed20b6b571e8867689ac901344af8e23b93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676599"
---
# <a name="getvirtualdesktopassignedtouser-method-of-the-win32_rdmsvirtualdesktop-class"></a>Método GetVirtualDesktopAssignedToUser de la \_ clase RDMSVirtualDesktop de Win32

Recupera el escritorio virtual asignado al usuario especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetVirtualDesktopAssignedToUser(
  [in]  string CollectionAlias,
  [in]  string UserName,
  [in]  string UserDomain,
  [out] string VMName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CollectionAlias* \[ de\]
</dt> <dd>

El alias de la colección de escritorios virtuales que contiene el escritorio virtual.

</dd> <dt>

*Nombre de usuario* \[ de\]
</dt> <dd>

Nombre de usuario del usuario.

</dd> <dt>

*UserDomain* \[ de\]
</dt> <dd>

El nombre de dominio del usuario.

</dd> <dt>

*VMName* \[ enuncia\]
</dt> <dd>

Recibe el nombre de la máquina virtual del escritorio virtual.

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

 

 





