---
title: Propiedad IMsRdpClientNonScriptable5 AllowPromptingForCredentials
description: Especifica si el control Escritorio remoto ActiveX puede solicitar credenciales al usuario.
ms.assetid: 9a780886-39ee-4d3b-9a54-fa209708d9f8
ms.tgt_platform: multiple
keywords:
- Propiedad AllowPromptingForCredentials Servicios de Escritorio remoto
- Propiedad AllowPromptingForCredentials Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable5
- Interfaz IMsRdpClientNonScriptable5 Servicios de Escritorio remoto , propiedad AllowPromptingForCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.get_AllowPromptingForCredentials
- IMsRdpClientNonScriptable5.put_AllowPromptingForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea0fb854b5bb12533032cd6608228d81584cd8d9f4e99bccd8a5ba76b624f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138758"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a>Propiedad IMsRdpClientNonScriptable5::AllowPromptingForCredentials

Especifica si el control Escritorio remoto ActiveX puede solicitar credenciales al usuario. Si esta propiedad contiene **VARIANT \_ TRUE**, se pueden solicitar credenciales al usuario. Si esta propiedad contiene **VARIANT \_ FALSE**, no se pueden solicitar credenciales al usuario.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_AllowPromptingForCredentials(
  [in]          VARIANT_BOOL fAllow
);

HRESULT get_AllowPromptingForCredentials(
  [out, retval] VARIANT_BOOL *pfAllow
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica el nuevo valor de propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 se define como 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





