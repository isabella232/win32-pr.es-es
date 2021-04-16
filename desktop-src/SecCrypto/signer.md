---
description: Establece el firmante de un objeto SignedData o SignedCode.
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: Objeto de firmante
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
ms.openlocfilehash: 974341eb996f2b5d3701757a5352ef56e2837390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671495"
---
# <a name="signer-object"></a>Objeto de firmante

\[El objeto de **firmante** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El objeto de **firmante** establece el firmante de un objeto [**SignedData**](signeddata.md) o [**SignedCode**](signedcode.md) . El [**certificado**](certificate.md) del objeto **firmante** debe tener una clave privada disponible que pueda usarse para firmar datos.

## <a name="members"></a>Miembros

El objeto de **firmante** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto de **firmante** tiene estos métodos.



| Método                      | Descripción                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [**Cargar**](signer-load.md) | Carga un certificado de firma desde un archivo PFX especificado.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto de **firmante** tiene estas propiedades.



| Propiedad                                                                     | Tipo de acceso           | Descripción                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticatedAttributes**](signer-authenticatedattributes.md)<br/> | Solo lectura<br/>  | Colección de atributos autenticados.<br/>                                                                                                                                                                                                                                                                                      |
| [**Certificado**](signer-certificate.md)<br/>                         | Lectura/escritura<br/> | Objeto de [**certificado**](certificate.md) que representa el certificado de un firmante de los datos.<br/> Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el [*Estado*](../secgloss/s-gly.md) completo del objeto.<br/> Esta es la propiedad predeterminada.<br/> |
| [**IAM**](signer-chain.md)<br/>                                     | Solo lectura<br/>  | Cadena del firmante.<br/>                                                                                                                                                                                                                                                                                                         |
| [**Opciones**](signer-options.md)<br/>                                 | Lectura/escritura<br/> | Establece o recupera la opción de certificado del firmante.<br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Observaciones

Se puede crear el objeto **firmante** y es seguro para el scripting. El ProgID del objeto de **firmante** es CAPICOM. Firmante. 2.

**CAPICOM 1. *x*:** el ProgID del objeto de **firmante** es CAPICOM. Firmante. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
