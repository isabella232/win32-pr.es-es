---
title: Método Join de la Win32_RDMSJoinedNode clase
description: Agrega un nodo a Escritorio remoto Management Services (RDMS).
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Combinación de métodos Servicios de Escritorio remoto
- Método join Servicios de Escritorio remoto , Win32_RDMSJoinedNode clase
- Win32_RDMSJoinedNode clase Servicios de Escritorio remoto método , Join
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Join
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204d83988f9a57d9fe0edf8daa6dc580676fc7395f98edcbece49674c0041aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605428"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a>Método Join de la clase \_ RDMSJoinedNode de Win32

Agrega un nodo a Escritorio remoto Management Services (RDMS).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NodeFQDN* \[ En\]
</dt> <dd>

Nombre de dominio completo del nodo.

</dd> <dt>

*NodeSID* \[ En\]
</dt> <dd>

Identificador de seguridad (SID) del nodo.

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

[**RdMSJoinedNode de Win32 \_**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





