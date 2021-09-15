---
description: Establece o recupera el contenido de texto no cifrado de un mensaje que se va a envoltorio. Esta es la propiedad predeterminada.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: Propiedad EnvelopedData.Content
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ce87dba503d8e8eec2dc21a9024c1071b3255f3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476414"
---
# <a name="envelopeddatacontent-property"></a>Propiedad EnvelopedData.Content

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

La **propiedad Content** establece o recupera el contenido de texto no cifrado de un mensaje que se va a envoltorio. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Sintaxis


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a>Valor de propiedad

El contenido de texto no cifrado de un mensaje que se va a envoltorio.

## <a name="remarks"></a>Observaciones

El establecimiento de esta propiedad debe realizarse antes de llamar al método [**Encrypt.**](envelopeddata-encrypt.md) Cuando se restablece el valor de esta propiedad, [](../secgloss/s-gly.md) directa o indirectamente, se restablece todo el estado del objeto y se pierde cualquier contenido cifrado del objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
