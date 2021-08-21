---
title: Propiedad IsRemoteProgramClientInstalled de IMsRdpClientShell
description: Recupera si el cliente Conexión a Escritorio remoto (RDC) admite Windows de RemoteApp de Server 2008 R2.
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- Propiedad IsRemoteProgramClientInstalled Servicios de Escritorio remoto
- Propiedad IsRemoteProgramClientInstalled Servicios de Escritorio remoto , interfaz IMsRdpClientShell
- Interfaz de IMsRdpClientShell Servicios de Escritorio remoto , propiedad IsRemoteProgramClientInstalled
topic_type:
- apiref
api_name:
- IMsRdpClientShell.IsRemoteProgramClientInstalled
- IMsRdpClientShell.get_IsRemoteProgramClientInstalled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3073bb9a9e5890ff7a6a46bb9ea0c03964bf54f1c91550dbb2746385a11fa809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129768"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a>Propiedad IMsRdpClientShell::IsRemoteProgramClientInstalled

Recupera si el cliente Conexión a Escritorio remoto (RDC) admite Windows de RemoteApp de Server 2008 R2.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a>Valor de propiedad

Recupera si el cliente Conexión a Escritorio remoto (RDC) admite la funcionalidad RemoteApp.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsRdpClientShell se define como \_ d012ae6d-c19a-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





