---
title: Propiedad MsRdpWorkspace de IMsRdpClientShell2
description: Recupera un puntero a la interfaz IMsRdpWorkspace, que se usa para administrar Conexión de RemoteApp y Escritorio credenciales y conexiones.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad MsRdpWorkspace
- Propiedad MsRdpWorkspace Servicios de Escritorio remoto, interfaz IMsRdpClientShell2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientShell2, propiedad MsRdpWorkspace
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802948"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a>IMsRdpClientShell2:: MsRdpWorkspace (propiedad)

Recupera un puntero a la interfaz [**IMsRdpWorkspace**](imsrdpworkspace.md) , que se usa para administrar conexión de RemoteApp y escritorio credenciales y conexiones.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Dirección de un puntero a la interfaz [**IMsRdpWorkspace**](imsrdpworkspace.md) .

## <a name="remarks"></a>Observaciones

La interfaz [**IMsRdpWorkspace**](imsrdpworkspace.md) no se expone como una interfaz personalizada. Solo se puede acceder a él a través de métodos [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                             |
| Archivo DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

