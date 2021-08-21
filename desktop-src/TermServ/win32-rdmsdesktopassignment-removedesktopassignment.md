---
title: Método RemoveDesktopAssignment de la Win32_RDMSDesktopAssignment clase
description: Quita una asignación de escritorio.
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- Método RemoveDesktopAssignment Servicios de Escritorio remoto
- Método RemoveDesktopAssignment Servicios de Escritorio remoto , Win32_RDMSDesktopAssignment clase
- Win32_RDMSDesktopAssignment clase Servicios de Escritorio remoto , método RemoveDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.RemoveDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae311ca8efd9d1a79287be1207bfc0f0cd5c7e6d7a9d45c40fb7591c1ee3839b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118849754"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Método RemoveDesktopAssignment de la clase \_ RDMSDesktopAssignment de Win32

Quita una asignación de escritorio

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*CollectionAlias* \[ En\]
</dt> <dd>

Alias de colección.

</dd> <dt>

*DesktopName* \[ En\]
</dt> <dd>

Nombre del escritorio.

</dd> <dt>

*UserDomain* \[ En\]
</dt> <dd>

Nombre de dominio de la cuenta de usuario.

</dd> <dt>

*UserName* \[ En\]
</dt> <dd>

Nombre de la cuenta de usuario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ cimv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_RDMSDesktopAssignment de Win32**](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





