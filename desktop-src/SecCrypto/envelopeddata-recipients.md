---
description: Recupera la colección de destinatarios del mensaje con doble cifrado.
ms.assetid: de9cbf8e-f34c-4e08-89aa-b5ac842aa599
title: Propiedad EnvelopedData. Recipients
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f047b4a8c579fb7f327b7410965a326c4a2f255d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649707"
---
# <a name="envelopeddatarecipients-property"></a>Propiedad EnvelopedData. Recipients

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propiedad **Recipients** recupera la colección de destinatarios del mensaje con doble cifrado.

## <a name="syntax"></a>Sintaxis


```VB
EnvelopedData.Recipients As Recipients
```



## <a name="property-value"></a>Valor de propiedad

Colección de [**destinatarios**](recipients.md) que representa a los destinatarios del mensaje con doble cifrado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
