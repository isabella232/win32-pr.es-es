---
title: Método AddDesktopAssignment de la clase Win32_RDMSDesktopAssignment
description: Agregar una asignación de escritorio.
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- Método AddDesktopAssignment Servicios de Escritorio remoto
- Método AddDesktopAssignment Servicios de Escritorio remoto, clase Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment de clase Servicios de Escritorio remoto, método AddDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.AddDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 571273e76b0bb45b748f1587e5a831fcf1e36b0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905157"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Método AddDesktopAssignment de la \_ clase RDMSDesktopAssignment de Win32

Agregar una asignación de escritorio

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddDesktopAssignment(
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

 

 





