---
title: Método TestAndSetState de la clase Win32_RDSHServer
description: Compara el estado actual con el especificado. Si los dos coinciden, el estado se establece en un nuevo valor. Independientemente de la coincidencia, también se devuelve el estado actual.
ms.assetid: f1bb0076-251b-4c0d-92f9-1c460e1b26bb
ms.tgt_platform: multiple
keywords:
- Método TestAndSetState Servicios de Escritorio remoto
- Método TestAndSetState Servicios de Escritorio remoto, clase Win32_RDSHServer
- Win32_RDSHServer de clase Servicios de Escritorio remoto, método TestAndSetState
topic_type:
- apiref
api_name:
- Win32_RDSHServer.TestAndSetState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4c9b616c2a288f5f39b240d71b2611e25d45f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150387"
---
# <a name="testandsetstate-method-of-the-win32_rdshserver-class"></a>Método TestAndSetState de la \_ clase RDSHServer de Win32

Compara el estado actual con el especificado. Si los dos coinciden, el estado se establece en un nuevo valor. Independientemente de la coincidencia, también se devuelve el estado actual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 TestAndSetState(
  [in]  uint32 Comparand,
  [in]  uint32 NewState,
  [out] uint32 InitState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Comparand* \[ de\]
</dt> <dd>

Valor que se va a comparar con el estado actual; Si los dos valores coinciden, el estado se establece en *NewState*.

</dd> <dt>

*NewState* \[ de\]
</dt> <dd>

Nuevo valor del estado.

</dd> <dt>

*InitState* \[ enuncia\]
</dt> <dd>

Si se realiza correctamente o con errores, devuelve el estado actual.

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

[**Win32 \_ RDSHServer**](win32-rdshserver.md)
</dt> </dl>

 

 





