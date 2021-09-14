---
title: Propiedad MsRdpWorkspace de IMsRdpClientShell2
description: Recupera un puntero a la interfaz IMsRdpWorkspace, que se usa para administrar Conexión de RemoteApp y Escritorio credenciales y conexiones.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- Propiedad MsRdpWorkspace Servicios de Escritorio remoto
- Propiedad MsRdpWorkspace Servicios de Escritorio remoto , interfaz IMsRdpClientShell2
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
ms.openlocfilehash: 91eadd3f1b422e3da96d5bcd3a5178a2a0b0eb52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886097"
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

## <a name="remarks"></a>Observaciones

La [**interfaz IMsRdpWorkspace**](imsrdpworkspace.md) no se expone como una interfaz personalizada. Solo se puede acceder a través [de métodos IDispatch.](/windows/desktop/com/exposing-methods-through-idispatch)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                             |
| Archivo DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

