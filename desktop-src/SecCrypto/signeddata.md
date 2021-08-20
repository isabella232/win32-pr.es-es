---
description: Proporciona propiedades y métodos para establecer el contenido que se va a firmar con una firma digital, firmar o cofirmar datos digitalmente y comprobar la firma digital de los datos firmados. El mensaje firmado está en formato PKCS \# 7.
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
ms.openlocfilehash: ec8d4b874f9269e4850b87ad65aab52563d007c805924bb0ab83f9ce76f8f38e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973735"
---
# <a name="signeddata-object"></a>Objeto SignedData

\[El **objeto SignedData** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **objeto SignedData** proporciona propiedades y métodos para establecer el contenido que se va a firmar con una firma [*digital,*](../secgloss/d-gly.md)firmar o cofirmar datos digitalmente y comprobar la firma digital de los datos firmados. El mensaje firmado está en formato PKCS \# 7.

Una firma de datos, si se comprueba, demuestra la asociación entre un firmante y los datos y muestra que los datos no se cambiaron de ninguna manera después de crear la firma.

## <a name="members"></a>Miembros

El **objeto SignedData** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SignedData** tiene estos métodos.



| Método                              | Descripción                                                         |
|:------------------------------------|:--------------------------------------------------------------------|
| [**Cosign**](signeddata-cosign.md) | Firma un mensaje ya firmado.<br/>                       |
| [**Firmar**](signeddata-sign.md)     | Crea una firma digital en el contenido que se va a firmar.<br/> |
| [**Comprobación**](signeddata-verify.md) | Determina la validez de una firma o firmas.<br/>    |



 

### <a name="properties"></a>Propiedades

El **objeto SignedData** tiene estas propiedades.



| Propiedad                                                   | Tipo de acceso           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](signeddata-certificates.md)<br/> | Solo lectura<br/>  | Recupera la colección [**Certificates**](certificates.md) de los datos firmados.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**Contenido**](signeddata-content.md)<br/>           | Lectura/escritura<br/> | Datos que se firmarán. Esta propiedad se debe inicializar antes de llamar [**al método Sign.**](signeddata-sign.md)<br/> Cuando se restablece el valor de esta propiedad, [](../secgloss/s-gly.md) directa o indirectamente, se restablece todo el estado del objeto y se pierde cualquier firma asociada al objeto antes de cambiar la propiedad.<br/> Esta es la propiedad predeterminada.<br/> |
| [**Firmantes**](signeddata-signers.md)<br/>           | Solo lectura<br/>  | Recupera la colección [**Signers**](signers.md) que representa los creadores de firmas de los datos.<br/>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Comentarios

Se puede crear el objeto **SignedData** y es seguro para el scripting. El ProgID del **objeto SignedData** es CAPICOM. SignedData.1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
