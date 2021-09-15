---
description: El objeto EnvelopedData proporciona propiedades y métodos para envolver datos para la privacidad mediante cifrado.
ms.assetid: 7c5f3e3d-6a70-455d-8921-20495eec4b3e
title: Objeto EnvelopedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5309061c6ab315a089a1e1d8b9488556cae9f31
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476408"
---
# <a name="envelopeddata-object"></a>Objeto EnvelopedData

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **objeto EnvelopedData proporciona** propiedades y métodos para envolver datos para la privacidad mediante cifrado. Para envolver datos, se genera una clave criptográfica de sesión. A [*continuación,*](../secgloss/s-gly.md) esa clave de sesión [](../secgloss/p-gly.md) se cifra para cada destinatario previsto mediante la clave pública de ese destinatario previsto desde el certificado del destinatario. Los datos cifrados y el conjunto de claves de sesión cifradas se pueden enviar a todos los destinatarios previstos. El mensaje generado está en formato PKCS \# 7.

## <a name="members"></a>Members

El **objeto EnvelopedData** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto EnvelopedData** tiene estos métodos.



| Método                                   | Descripción                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Descifrar**](envelopeddata-decrypt.md) | Descifra el contenido en sobre.<br/>                                                                      |
| [**Cifrar**](envelopeddata-encrypt.md) | Cifra el contenido, cifra una clave de sesión para cada destinatario y devuelve el BLOB cifrado.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto EnvelopedData** tiene estas propiedades.



| Propiedad.                                                  | Tipo de acceso           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](envelopeddata-algorithm.md)<br/>   | Lectura y escritura<br/> | Algoritmo de cifrado y [*longitud de clave*](../secgloss/k-gly.md).<br/>                                                                                                                                                                                                                                                                                                                              |
| [**Contenido**](envelopeddata-content.md)<br/>       | Lectura y escritura<br/> | El contenido de texto no cifrado de un mensaje que se va a envolvía. El establecimiento de esta propiedad debe realizarse antes [**de llamar al**](envelopeddata-encrypt.md) método Encrypt.<br/> Cuando se restablece el valor de esta propiedad, [](../secgloss/s-gly.md) directa o indirectamente, se restablece todo el estado del objeto y se pierde cualquier contenido cifrado del objeto.<br/> Esta es la propiedad predeterminada.<br/> |
| [**Recipients**](envelopeddata-recipients.md)<br/> | Solo lectura<br/>  | Colección de [**objetos Certificate**](certificate.md) para recibir el mensaje sobres.<br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Observaciones

Se **puede crear el objeto EnvelopedData** y es seguro para el scripting. El ProgID del **objeto EnvelopedData** es CAPICOM. EnvelopedData.1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
