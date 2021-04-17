---
title: Método GetJoinedNodeCount de la clase Win32_RDMSJoinedNode
description: Obtiene el número de servidores que tienen instalados los roles especificados.
ms.assetid: ed2ae0b5-5cbc-4c11-a2ad-065f88dd5842
ms.tgt_platform: multiple
keywords:
- Método GetJoinedNodeCount Servicios de Escritorio remoto
- Método GetJoinedNodeCount Servicios de Escritorio remoto, clase Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode de clase Servicios de Escritorio remoto, método GetJoinedNodeCount
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.GetJoinedNodeCount
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ecc5c388814873aa690e9af5adda5081aad4d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676709"
---
# <a name="getjoinednodecount-method-of-the-win32_rdmsjoinednode-class"></a>Método GetJoinedNodeCount de la \_ clase RDMSJoinedNode de Win32

Obtiene el número de servidores que tienen instalados los roles especificados.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetJoinedNodeCount(
  [in]  uint32 roleType,
  [out] uint32 Count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*roleType* \[ de\]
</dt> <dd>

Un campo de bits que especifica los tipos de rol.

<dt>

0
</dt> <dd>

Todo

</dd> <dt>

1
</dt> <dd>

Conexión a Escritorio remoto Broker (RDCB)

</dd> <dt>

2
</dt> <dd>

Host de sesión de Escritorio remoto (RDSH)

</dd> <dt>

4
</dt> <dd>

Host de virtualización de Escritorio remoto (RDVH)

</dd> </dl> </dd> <dt>

*Recuento* \[ enuncia\]
</dt> <dd>

Si se ejecuta correctamente, devuelve el número de servidores con los roles especificados instalados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                              |
| Espacio de nombres<br/>                | RDMs raíz de \\ CIMv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ RDMSJoinedNode**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





