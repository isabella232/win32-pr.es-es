---
description: Establece o recupera un valor booleano que especifica si se pueden usar los mensajes de la interfaz de usuario para el firmante o la identidad de un remitente.
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: Propiedad settings. EnablePromptForCertificateUI
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690540"
---
# <a name="settingsenablepromptforcertificateui-property"></a>Propiedad settings. EnablePromptForCertificateUI

\[La propiedad **EnablePromptForCertificateUI** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]

La propiedad **EnablePromptForCertificateUI** establece o recupera un valor booleano que especifica si se pueden usar los mensajes de la interfaz de usuario para el firmante o la identidad de un remitente.

## <a name="syntax"></a>Sintaxis


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true**, se puede usar la interfaz de usuario para solicitar un firmante o la identidad del remitente. El valor predeterminado es **false**.

> [!Note]  
> Al establecer esta propiedad, no se deshabilitan las advertencias generadas antes de que se realice un uso de clave privada desde una aplicación basada en Web.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración**](settings.md)
</dt> </dl>

 

 




