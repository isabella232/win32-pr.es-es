---
description: Establece el firmante de un objeto SignedData o SignedCode.
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: Objeto signer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4da0f63c64a85290d5b36cad046446a9a0feedcd897869a0df1932ee2532a687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898517"
---
# <a name="signer-object"></a>Objeto signer

\[El **objeto Signer** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase CmsSigner en**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **objeto Signer** establece el firmante de un [**objeto SignedData**](signeddata.md) [**o SignedCode.**](signedcode.md) El [**certificado**](certificate.md) del **objeto Signer** debe tener una clave privada disponible que se pueda usar para firmar los datos.

## <a name="members"></a>Miembros

El **objeto Signer** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Signer** tiene estos métodos.



| Método                      | Descripción                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [**Cargar**](signer-load.md) | Carga un certificado de firma desde un archivo PFX especificado.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto Signer** tiene estas propiedades.



| Propiedad                                                                     | Tipo de acceso           | Descripción                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticatedAttributes**](signer-authenticatedattributes.md)<br/> | Solo lectura<br/>  | Colección de atributos autenticados.<br/>                                                                                                                                                                                                                                                                                      |
| [**Certificado**](signer-certificate.md)<br/>                         | Lectura/escritura<br/> | Objeto [**Certificate**](certificate.md) que representa el certificado de un firmante de los datos.<br/> Cuando se restablece el valor de esta propiedad, directa o indirectamente, se restablece [*todo*](../secgloss/s-gly.md) el estado del objeto.<br/> Esta es la propiedad predeterminada.<br/> |
| [**Cadena**](signer-chain.md)<br/>                                     | Solo lectura<br/>  | Cadena del firmante.<br/>                                                                                                                                                                                                                                                                                                         |
| [**Opciones**](signer-options.md)<br/>                                 | Lectura/escritura<br/> | Establece o recupera la opción de certificado del firmante.<br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentarios

Se puede crear el objeto **Signer** y es seguro para el scripting. El ProgID del **objeto Signer** es CAPICOM. Signer.2.

**CAPICOM 1. *x:*** el ProgID del objeto **Signer** es CAPICOM. Signer.1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
