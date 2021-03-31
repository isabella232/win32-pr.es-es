---
title: Propiedad RedirectDynamicDrives de IMsRdpClientNonScriptable3
description: Especifica o recupera si las unidades de Plug and Play conectadas dinámicamente (PnP) que se enumeran mientras están en una sesión están disponibles para la redirección.
ms.assetid: 11eb19fc-9711-4293-8054-f7975dadb492
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDrives
- Propiedad RedirectDynamicDrives Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad RedirectDynamicDrives
- Propiedad RedirectDynamicDrives Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad RedirectDynamicDrives
- Propiedad RedirectDynamicDrives Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad RedirectDynamicDrives
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDrives, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad RedirectDynamicDrives
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDrives, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad RedirectDynamicDrives
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDrives, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad RedirectDynamicDrives
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDrives, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad RedirectDynamicDrives
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDrives, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad RedirectDynamicDrives
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDrives
- IMsRdpClientNonScriptable3.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable3.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.RedirectDynamicDrives
- IMsRdpClientNonScriptable4.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.RedirectDynamicDrives
- IMsRdpClientNonScriptable5.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.put_RedirectDynamicDrives
- MsRdpClient5.RedirectDynamicDrives
- MsRdpClient6.RedirectDynamicDrives
- MsRdpClient7.RedirectDynamicDrives
- MsRdpClient8.RedirectDynamicDrives
- MsRdpClient9.RedirectDynamicDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19c0e6e20f7f73481f6f2ecbc50ab0eda512ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803884"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdrives-property"></a>IMsRdpClientNonScriptable3:: RedirectDynamicDrives (propiedad)

Especifica o recupera si las unidades de Plug and Play conectadas dinámicamente (PnP) que se enumeran mientras están en una sesión están disponibles para la redirección.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_RedirectDynamicDrives(
  [in]  VARIANT_BOOL fRedirectDynamicDrives
);

HRESULT get_RedirectDynamicDrives(
  [out] VARIANT_BOOL *pfRedirectDynamicDrives
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica si las unidades PnP conectadas dinámicamente que se enumeran mientras están en una sesión están disponibles para la redirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





