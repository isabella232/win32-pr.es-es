---
title: Propiedad MsRdpWorkspace de IMsRdpClientShell2
description: Recupera un puntero a la interfaz IMsRdpWorkspace, que se usa para administrar Conexión de RemoteApp y Escritorio credenciales y conexiones.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- Propiedad MsRdpWorkspace Servicios de Escritorio remoto
- Interfaz de la propiedad MsRdpWorkspace Servicios de Escritorio remoto , IMsRdpClientShell2
- Interfaz IMsRdpClientShell2 Servicios de Escritorio remoto , propiedad MsRdpWorkspace
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6470f51ccae2efb6dc3d44a7b0a2a0310ad4230861d7d86262f34fd312fcfc5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854445"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a>IMsRdpClientShell2::MsRdpWorkspace, propiedad

Recupera un puntero a la [**interfaz IMsRdpWorkspace,**](imsrdpworkspace.md) que se usa para administrar Conexión de RemoteApp y Escritorio credenciales y conexiones.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Dirección de un puntero a la [**interfaz IMsRdpWorkspace.**](imsrdpworkspace.md)

## <a name="remarks"></a>Comentarios

La [**interfaz IMsRdpWorkspace**](imsrdpworkspace.md) no se expone como una interfaz personalizada. Solo se puede acceder a través [de métodos IDispatch.](/windows/desktop/com/exposing-methods-through-idispatch)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                             |
| Archivo DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

