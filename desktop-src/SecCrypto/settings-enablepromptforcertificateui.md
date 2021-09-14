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
ms.openlocfilehash: e494c98e2a828b512b0bb66dc2a44cba8c37792c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160730"
---
# <a name="settingsenablepromptforcertificateui-property"></a>Configuración. EnablePromptForCertificateUI, propiedad

\[La **propiedad EnablePromptForCertificateUI** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos.\]

La **propiedad EnablePromptForCertificateUI** establece o recupera un valor booleano que especifica si la interfaz de usuario solicita la identidad de un firmante o remitente.

## <a name="syntax"></a>Sintaxis


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true,** se puede usar la interfaz de usuario que solicita la identidad de un firmante o remitente. El valor predeterminado es **false**.

> [!Note]  
> Al establecer esta propiedad no se deshabilitan las advertencias que se generan antes de que se haga cualquier uso de clave privada desde una aplicación basada en web.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Configuración**](settings.md)
</dt> </dl>

 

 




