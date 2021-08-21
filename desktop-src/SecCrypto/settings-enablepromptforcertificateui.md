---
description: Establece o recupera un valor booleano que especifica si la interfaz de usuario solicita la identidad de un firmante o remitente.
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: Configuración. EnablePromptForCertificateUI, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.EnablePromptForCertificateUI
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: effc6115586139fe47db677907fdfdac7ca14d7a9c9f27a49407d8ad762cf914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974435"
---
# <a name="settingsenablepromptforcertificateui-property"></a>Configuración. EnablePromptForCertificateUI, propiedad

\[La **propiedad EnablePromptForCertificateUI** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos.\]

La **propiedad EnablePromptForCertificateUI** establece o recupera un valor booleano que especifica si la interfaz de usuario solicita la identidad de un firmante o remitente.

## <a name="syntax"></a>Syntax


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true,** se puede usar la interfaz de usuario que solicita la identidad de un firmante o remitente. El valor predeterminado es **false**.

> [!Note]  
> Al establecer esta propiedad no se deshabilitan las advertencias que se generan antes de que se haga cualquier uso de clave privada desde una aplicación basada en web.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración**](settings.md)
</dt> </dl>

 

 




