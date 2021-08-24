---
title: Método AddDesktopAssignment de la Win32_RDMSDesktopAssignment clase
description: Agregue una asignación de escritorio.
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- Método AddDesktopAssignment Servicios de Escritorio remoto
- Método AddDesktopAssignment Servicios de Escritorio remoto , Win32_RDMSDesktopAssignment clase
- Win32_RDMSDesktopAssignment clase Servicios de Escritorio remoto , método AddDesktopAssignment
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
ms.openlocfilehash: 6c0d8145318cfd749772d2dcf417b71c6a1862ee31ec363957554e06b3aa6257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868225"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Método AddDesktopAssignment de la clase \_ RDMSDesktopAssignment de Win32

Adición de una asignación de escritorio

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



| Requisito | Value |
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

 

 





