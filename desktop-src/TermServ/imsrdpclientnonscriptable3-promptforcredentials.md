---
title: Propiedad IMsRdpClientNonScriptable3 PromptForCredentials (Wuapi. h)
description: Especifica o recupera si el cuadro de diálogo solicitar credenciales está habilitado para la conexión.
ms.assetid: 252ec5bd-bd52-40d4-ae48-b2c00c0720c0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PromptForCredentials
- Propiedad PromptForCredentials Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad PromptForCredentials
- Propiedad PromptForCredentials Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad PromptForCredentials
- Propiedad PromptForCredentials Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad PromptForCredentials
- Servicios de Escritorio remoto de la propiedad PromptForCredentials, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad PromptForCredentials
- Servicios de Escritorio remoto de la propiedad PromptForCredentials, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad PromptForCredentials
- Servicios de Escritorio remoto de la propiedad PromptForCredentials, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad PromptForCredentials
- Servicios de Escritorio remoto de la propiedad PromptForCredentials, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad PromptForCredentials
- Servicios de Escritorio remoto de la propiedad PromptForCredentials, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad PromptForCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.PromptForCredentials
- IMsRdpClientNonScriptable3.get_PromptForCredentials
- IMsRdpClientNonScriptable3.put_PromptForCredentials
- IMsRdpClientNonScriptable4.PromptForCredentials
- IMsRdpClientNonScriptable4.get_PromptForCredentials
- IMsRdpClientNonScriptable4.put_PromptForCredentials
- IMsRdpClientNonScriptable5.PromptForCredentials
- IMsRdpClientNonScriptable5.get_PromptForCredentials
- IMsRdpClientNonScriptable5.put_PromptForCredentials
- MsRdpClient5.PromptForCredentials
- MsRdpClient6.PromptForCredentials
- MsRdpClient7.PromptForCredentials
- MsRdpClient8.PromptForCredentials
- MsRdpClient9.PromptForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f913937c9a2ff01d4aabeaba48dcbdc8ddb21d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359672"
---
# <a name="imsrdpclientnonscriptable3promptforcredentials-property"></a>IMsRdpClientNonScriptable3::P propiedad romptForCredentials

Especifica o recupera si el cuadro de diálogo solicitar credenciales está habilitado para la conexión.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_PromptForCredentials(
  [in]  VARIANT_BOOL fPrompt
);

HRESULT get_PromptForCredentials(
  [out] VARIANT_BOOL *pfPrompt
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica si el cuadro de diálogo solicitar credenciales está habilitado para la conexión.

## <a name="error-codes"></a>Códigos de error

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Encabezado<br/>                   | <dl> <dt>Wuapi. h</dt> </dl>            |
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

 

 





