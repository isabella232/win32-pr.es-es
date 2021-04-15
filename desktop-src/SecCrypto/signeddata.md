---
description: Proporciona propiedades y métodos para establecer el contenido que se va a firmar con una firma digital, para firmar o cofirmar datos digitalmente, y para comprobar la firma digital de los datos firmados. El mensaje firmado está en \# formato PKCS 7.
ms.assetid: 500437e8-a637-4e89-9ac9-aa3ea20d437f
title: Objeto SignedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d0424826f7dc5d041b877ced1cd7f50490d7801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690057"
---
# <a name="signeddata-object"></a>Objeto SignedData

\[El objeto **SignedData** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El objeto **SignedData** proporciona propiedades y métodos para establecer el contenido que se va a firmar con una [*firma digital*](../secgloss/d-gly.md), firmar o cofirmar datos digitalmente y comprobar la firma digital de los datos firmados. El mensaje firmado está en \# formato PKCS 7.

Una firma de datos, si se comprueba, demuestra la asociación entre un firmante y los datos, y muestra que los datos no se cambiaron de ningún modo una vez creada la firma.

## <a name="members"></a>Miembros

El objeto **SignedData** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SignedData** tiene estos métodos.



| Método                              | Descripción                                                         |
|:------------------------------------|:--------------------------------------------------------------------|
| [**Firmar**](signeddata-cosign.md) | Firma un mensaje ya firmado.<br/>                       |
| [**Sesión**](signeddata-sign.md)     | Crea una firma digital en el contenido que se va a firmar.<br/> |
| [**Ver**](signeddata-verify.md) | Determina la validez de una firma o signaturas.<br/>    |



 

### <a name="properties"></a>Propiedades

El objeto **SignedData** tiene estas propiedades.



| Propiedad                                                   | Tipo de acceso           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](signeddata-certificates.md)<br/> | Solo lectura<br/>  | Recupera la colección de [**certificados**](certificates.md) de los datos firmados.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**Contenido**](signeddata-content.md)<br/>           | Lectura/escritura<br/> | Datos que se van a firmar. Esta propiedad se debe inicializar antes de que se llame al método [**Sign**](signeddata-sign.md) .<br/> Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el [*Estado*](../secgloss/s-gly.md) completo del objeto y se pierde cualquier firma asociada al objeto antes de que se cambiara la propiedad.<br/> Esta es la propiedad predeterminada.<br/> |
| [**Firmantes**](signeddata-signers.md)<br/>           | Solo lectura<br/>  | Recupera la colección de [**firmantes**](signers.md) que representa los creadores de firmas de los datos.<br/>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

Se puede crear el objeto **SignedData** y es seguro para el scripting. El ProgID del objeto **SignedData** es CAPICOM. SignedData. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
