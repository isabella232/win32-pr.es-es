---
title: Propiedad LaunchedViaClientShellInterface de IMsRdpClientNonScriptable4
description: Especifica si el usuario inició el control de cliente mediante la interfaz de acceso web de Escritorio remoto (acceso web de escritorio remoto).
ms.assetid: bf72c375-0eec-49c7-9f9a-c7545a95bdce
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad LaunchedViaClientShellInterface
- Propiedad LaunchedViaClientShellInterface Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad LaunchedViaClientShellInterface
- Propiedad LaunchedViaClientShellInterface Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad LaunchedViaClientShellInterface
- Servicios de Escritorio remoto de la propiedad LaunchedViaClientShellInterface, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad LaunchedViaClientShellInterface
- Servicios de Escritorio remoto de la propiedad LaunchedViaClientShellInterface, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad LaunchedViaClientShellInterface
- Servicios de Escritorio remoto de la propiedad LaunchedViaClientShellInterface, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad LaunchedViaClientShellInterface
- Servicios de Escritorio remoto de la propiedad LaunchedViaClientShellInterface, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad LaunchedViaClientShellInterface
- Servicios de Escritorio remoto de la propiedad LaunchedViaClientShellInterface, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad LaunchedViaClientShellInterface
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.put_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.put_LaunchedViaClientShellInterface
- MsRdpClient5.LaunchedViaClientShellInterface
- MsRdpClient6.LaunchedViaClientShellInterface
- MsRdpClient7.LaunchedViaClientShellInterface
- MsRdpClient8.LaunchedViaClientShellInterface
- MsRdpClient9.LaunchedViaClientShellInterface
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d5854a4e75be455035fd9a123418bd486932379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996596"
---
# <a name="imsrdpclientnonscriptable4launchedviaclientshellinterface-property"></a>IMsRdpClientNonScriptable4:: LaunchedViaClientShellInterface (propiedad)

Especifica si el usuario inició el control de cliente mediante la interfaz de acceso web de Escritorio remoto (acceso web de escritorio remoto).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_LaunchedViaClientShellInterface(
  [in]  VARIANT_BOOL fLaunchedViaClientShellInterface
);

HRESULT get_LaunchedViaClientShellInterface(
  [out]  VARIANT_BOOL *pfLaunchedViaClientShellInterface
);
```



## <a name="property-value"></a>Valor de propiedad

Establece la propiedad **LaunchedViaClientShellInterface** .

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





