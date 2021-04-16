---
description: Establece o recupera el contenido de texto no cifrado de un mensaje que se va a aplicar sobre. Esta es la propiedad predeterminada.
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: Propiedad EnvelopedData. Content
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649802"
---
# <a name="envelopeddatacontent-property"></a>Propiedad EnvelopedData. Content

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propiedad de **contenido** establece o recupera el contenido de texto sin formato de un mensaje que se va a aplicar sobre. Esta es la propiedad predeterminada.

## <a name="syntax"></a>Sintaxis


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a>Valor de propiedad

El contenido de texto sin formato de un mensaje que se va a acercar.

## <a name="remarks"></a>Observaciones

La configuración de esta propiedad debe realizarse antes de llamar al método de [**cifrado**](envelopeddata-encrypt.md) . Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el [*Estado*](../secgloss/s-gly.md) completo del objeto y se pierde cualquier contenido cifrado en el objeto.

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

 

 
