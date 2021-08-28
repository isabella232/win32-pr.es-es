---
title: Método GetVirtualDesktopAssignedToUser de la Win32_RDMSVirtualDesktop clase
description: Recupera el escritorio virtual asignado al usuario especificado.
ms.assetid: cbc22c45-4492-4651-b164-a6fd717c5ab4
ms.tgt_platform: multiple
keywords:
- Método GetVirtualDesktopAssignedToUser Servicios de Escritorio remoto
- Método GetVirtualDesktopAssignedToUser Servicios de Escritorio remoto , Win32_RDMSVirtualDesktop clase
- Win32_RDMSVirtualDesktop clase Servicios de Escritorio remoto , método GetVirtualDesktopAssignedToUser
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
ms.openlocfilehash: fce30afea4a95ed462bfb1b456788fa54f045097c16c3d65070cdb343e928237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059553"
---
# <a name="getvirtualdesktopassignedtouser-method-of-the-win32_rdmsvirtualdesktop-class"></a>Método GetVirtualDesktopAssignedToUser de la clase \_ RDMSVirtualDesktop de Win32

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

*CollectionAlias* \[ En\]
</dt> <dd>

Alias de la colección de escritorios virtuales que contiene el escritorio virtual.

</dd> <dt>

*UserName* \[ En\]
</dt> <dd>

Nombre de usuario del usuario.

</dd> <dt>

*UserDomain* \[ En\]
</dt> <dd>

Nombre de dominio del usuario.

</dd> <dt>

*VMName* \[ out\]
</dt> <dd>

Recibe el nombre de la máquina virtual del escritorio virtual.

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

 

 





