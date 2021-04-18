---
title: Propiedad AllowPromptingForCredentials de IMsRdpClientNonScriptable5
description: Especifica si el control ActiveX Escritorio remoto puede solicitar las credenciales al usuario.
ms.assetid: 9a780886-39ee-4d3b-9a54-fa209708d9f8
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AllowPromptingForCredentials
- Propiedad AllowPromptingForCredentials Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad AllowPromptingForCredentials
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
ms.openlocfilehash: c326a83a46b41d3578c958e24fd901beb7c7b321
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686240"
---
# <a name="imsrdpclientnonscriptable5allowpromptingforcredentials-property"></a>IMsRdpClientNonScriptable5:: AllowPromptingForCredentials (propiedad)

Especifica si el control ActiveX Escritorio remoto puede solicitar las credenciales al usuario. Si esta propiedad contiene **Variant \_ true**, se puede solicitar credenciales al usuario. Si esta propiedad contiene **Variant \_ false**, no se puede solicitar credenciales al usuario.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


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
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 se define como 4f6996d5-d7b1-412C-b0ff-063718566907<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





