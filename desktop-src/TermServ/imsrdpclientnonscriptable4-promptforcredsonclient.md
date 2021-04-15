---
title: Propiedad PromptForCredsOnClient de IMsRdpClientNonScriptable4
description: Especifica si el control de cliente muestra un cuadro de diálogo que solicita las credenciales.
ms.assetid: 426676be-0150-4a33-acd0-26423966f32a
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PromptForCredsOnClient
- Propiedad PromptForCredsOnClient Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad PromptForCredsOnClient
- Propiedad PromptForCredsOnClient Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad PromptForCredsOnClient
- Servicios de Escritorio remoto de la propiedad PromptForCredsOnClient, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad PromptForCredsOnClient
- Servicios de Escritorio remoto de la propiedad PromptForCredsOnClient, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad PromptForCredsOnClient
- Servicios de Escritorio remoto de la propiedad PromptForCredsOnClient, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad PromptForCredsOnClient
- Servicios de Escritorio remoto de la propiedad PromptForCredsOnClient, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad PromptForCredsOnClient
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PromptForCredsOnClient
- IMsRdpClientNonScriptable4.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable4.put_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.PromptForCredsOnClient
- IMsRdpClientNonScriptable5.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.put_PromptForCredsOnClient
- MsRdpClient6.PromptForCredsOnClient
- MsRdpClient7.PromptForCredsOnClient
- MsRdpClient8.PromptForCredsOnClient
- MsRdpClient9.PromptForCredsOnClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6443c503e107bb2edb164a17beedddb1bbbc88a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422431"
---
# <a name="imsrdpclientnonscriptable4promptforcredsonclient-property"></a>IMsRdpClientNonScriptable4::P propiedad romptForCredsOnClient

Especifica si el control de cliente muestra un cuadro de diálogo que solicita las credenciales.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_PromptForCredsOnClient(
  [in]  VARIANT_BOOL fPromptForCredsOnClient
);

HRESULT get_PromptForCredsOnClient(
  [out] VARIANT_BOOL *pfPromptForCredsOnClient
);
```



## <a name="property-value"></a>Valor de propiedad

Establece si el control de cliente muestra un cuadro de diálogo que solicita las credenciales.

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

 

 





