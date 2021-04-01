---
title: Propiedad EnableCredSspSupport de IMsRdpClientNonScriptable3
description: Especifica o recupera si el proveedor de servicios de seguridad de credenciales (CredSSP) está habilitado para esta conexión.
ms.assetid: 770da50b-2a93-4274-9b6f-c24c13f08549
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad EnableCredSspSupport
- Servicios de Escritorio remoto de la propiedad EnableCredSspSupport, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad EnableCredSspSupport
- Servicios de Escritorio remoto de la propiedad EnableCredSspSupport, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad EnableCredSspSupport
- Servicios de Escritorio remoto de la propiedad EnableCredSspSupport, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad EnableCredSspSupport
- Servicios de Escritorio remoto de la propiedad EnableCredSspSupport, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad EnableCredSspSupport
- Servicios de Escritorio remoto de la propiedad EnableCredSspSupport, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad EnableCredSspSupport
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.EnableCredSspSupport
- IMsRdpClientNonScriptable3.get_EnableCredSspSupport
- IMsRdpClientNonScriptable3.put_EnableCredSspSupport
- IMsRdpClientNonScriptable4.EnableCredSspSupport
- IMsRdpClientNonScriptable4.get_EnableCredSspSupport
- IMsRdpClientNonScriptable4.put_EnableCredSspSupport
- IMsRdpClientNonScriptable5.EnableCredSspSupport
- IMsRdpClientNonScriptable5.get_EnableCredSspSupport
- IMsRdpClientNonScriptable5.put_EnableCredSspSupport
- MsRdpClient5.EnableCredSspSupport
- MsRdpClient6.EnableCredSspSupport
- MsRdpClient7.EnableCredSspSupport
- MsRdpClient8.EnableCredSspSupport
- MsRdpClient9.EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2330b800d15f95a7b59a01735de971dd4b212d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150220"
---
# <a name="imsrdpclientnonscriptable3enablecredsspsupport-property"></a>IMsRdpClientNonScriptable3:: EnableCredSspSupport (propiedad)

Especifica o recupera si el proveedor de servicios de seguridad de credenciales (CredSSP) está habilitado para esta conexión.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica si CredSSP está habilitado para esta conexión.

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

 

 





