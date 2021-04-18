---
title: Propiedad RemoteProgramMode de ITSRemoteProgram
description: Modo RemoteApp de Windows Server 2008 R2.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RemoteProgramMode
- Propiedad RemoteProgramMode Servicios de Escritorio remoto, interfaz ITSRemoteProgram
- Servicios de Escritorio remoto de la interfaz ITSRemoteProgram, propiedad RemoteProgramMode
- Propiedad RemoteProgramMode Servicios de Escritorio remoto, interfaz ITSRemoteProgram2
- Servicios de Escritorio remoto de la interfaz ITSRemoteProgram2, propiedad RemoteProgramMode
- Propiedad RemoteProgramMode Servicios de Escritorio remoto, interfaz ITSRemoteProgram3
- Servicios de Escritorio remoto de la interfaz ITSRemoteProgram3, propiedad RemoteProgramMode
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686016"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a>ITSRemoteProgram:: RemoteProgramMode (propiedad)

Modo RemoteApp de Windows Server 2008 R2.

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

Modo RemoteApp. Si se establece en **Variant \_ true**, el modo RemoteApp está habilitado y la sesión remota hospedará los programas de RemoteApp. Si se establece en **Variant \_ false** (el valor predeterminado), el modo RemoteApp no está habilitado. La sesión remota hospedará un escritorio remoto.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ ITSRemoteProgram se define como FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





