---
title: Método RemoveDesktopAssignment de la clase Win32_RDMSDesktopAssignment
description: Quita una asignación de escritorio.
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- Método RemoveDesktopAssignment Servicios de Escritorio remoto
- Método RemoveDesktopAssignment Servicios de Escritorio remoto, clase Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment de clase Servicios de Escritorio remoto, método RemoveDesktopAssignment
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
ms.openlocfilehash: 6645a79efc970cf7c3288d0765e9aac8cac68a89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686200"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Método RemoveDesktopAssignment de la \_ clase RDMSDesktopAssignment de Win32

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

*CollectionAlias* \[ de\]
</dt> <dd>

El alias de la colección.

</dd> <dt>

*DesktopName* \[ de\]
</dt> <dd>

Nombre del escritorio.

</dd> <dt>

*UserDomain* \[ de\]
</dt> <dd>

El nombre de dominio de la cuenta de usuario.

</dd> <dt>

*Nombre de usuario* \[ de\]
</dt> <dd>

El nombre de la cuenta de usuario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                              |
| Espacio de nombres<br/>                | RDMs raíz de \\ cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ RDMSDesktopAssignment**](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





