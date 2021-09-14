---
title: ItsRemoteProgram RemoteProgramMode, propiedad
description: Modo remoteApp Windows Server 2008 R2.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- Propiedad RemoteProgramMode Servicios de Escritorio remoto
- Propiedad RemoteProgramMode Servicios de Escritorio remoto , interfaz ITSRemoteProgram
- Interfaz ITSRemoteProgram Servicios de Escritorio remoto , propiedad RemoteProgramMode
- Propiedad RemoteProgramMode Servicios de Escritorio remoto , interfaz ITSRemoteProgram2
- Interfaz ITSRemoteProgram2 Servicios de Escritorio remoto , propiedad RemoteProgramMode
- Propiedad RemoteProgramMode Servicios de Escritorio remoto , interfaz ITSRemoteProgram3
- Interfaz ITSRemoteProgram3 Servicios de Escritorio remoto , propiedad RemoteProgramMode
topic_type:
- apiref
api_name:
- ITSRemoteProgram.RemoteProgramMode
- ITSRemoteProgram.get_RemoteProgramMode
- ITSRemoteProgram.put_RemoteProgramMode
- ITSRemoteProgram2.RemoteProgramMode
- ITSRemoteProgram2.get_RemoteProgramMode
- ITSRemoteProgram2.put_RemoteProgramMode
- ITSRemoteProgram3.RemoteProgramMode
- ITSRemoteProgram3.get_RemoteProgramMode
- ITSRemoteProgram3.put_RemoteProgramMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8582824e2f6349e37b125ffd974847b602ad6fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968136"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a>ITSRemoteProgram::RemoteProgramMode, propiedad

Modo remoteApp Windows Server 2008 R2.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_RemoteProgramMode(
  [in]  VARIANT_BOOL vboolRemoteProgramMode
);

HRESULT get_RemoteProgramMode(
  [out] VARIANT_BOOL *pvboolRemoteProgramMode
);
```



## <a name="property-value"></a>Valor de propiedad

Modo RemoteApp. Si se establece en **VARIANT \_ TRUE,** el modo RemoteApp está habilitado y la sesión remota hospedará programas RemoteApp. Si se establece **en VARIANT \_ FALSE** (valor predeterminado), el modo RemoteApp no está habilitado. La sesión remota hospedará un escritorio remoto.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID ITSRemoteProgram se define como \_ FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





