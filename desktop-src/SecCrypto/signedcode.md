---
description: Proporciona funcionalidad para firmar archivos ejecutables con una firma digital Authenticode.
ms.assetid: e6d4e694-471f-4d30-983c-6bc5d631d99e
title: Objeto SignedCode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e119a639af7cb6459e8e6ec8ae6416f9d067c56e8f81560fedc385abd518b840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118899344"
---
# <a name="signedcode-object"></a>Objeto SignedCode

\[El **objeto SignedCode** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use Platform Invocation Services (PInvoke) para llamar a las funciones [**SignerSignEx,**](signersignex.md) [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar contenido con una firma digital Authenticode. Para obtener información sobre PInvoke, vea [Tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). Las subsecciones .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 y .NET y CryptoAPI a través de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsecciones de la parte 2 de Extensión de criptografía de .NET con [CAPICOM y P/Invoke](/previous-versions/ms867087(v=msdn.10)) también pueden resultar útiles.\]

El **objeto SignedCode** proporciona funcionalidad para firmar archivos ejecutables con una firma digital Authenticode.

## <a name="when-to-use"></a>Cuándo se usa

El **objeto SignedCode** se usa para realizar las tareas siguientes:

-   Firmar archivos ejecutables.
-   Archivos ejecutables de marca de tiempo.
-   Determine si la firma del archivo ejecutable es válida.
-   Establezca o recupere la ruta de acceso al archivo ejecutable.
-   Recupere el firmante y el stamper de tiempo del archivo ejecutable.
-   Recupere una colección de los certificados para el archivo ejecutable.
-   Recupere una descripción o la dirección URL de la descripción del archivo ejecutable.

## <a name="members"></a>Miembros

El **objeto SignedCode** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SignedCode** tiene estos métodos.



| Método                                    | Descripción                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Firmar**](signedcode-sign.md)           | Crea una firma digital Authenticode y firma el archivo ejecutable especificado en la [**propiedad SignedCode.FileName.**](signedcode-filename.md)<br/>    |
| [**Timestamp**](signedcode-timestamp.md) | Crea una firma de marca de tiempo Authenticode en el archivo ejecutable firmado especificado en la [**propiedad SignedCode.FileName.**](signedcode-filename.md)<br/> |
| [**Verificación**](signedcode-verify.md)       | Comprueba la firma Authenticode en el archivo ejecutable firmado especificado en la [**propiedad SignedCode.FileName.**](signedcode-filename.md)<br/>          |



 

### <a name="properties"></a>Propiedades

El **objeto SignedCode** tiene estas propiedades.



| Propiedad                                                       | Tipo de acceso           | Descripción                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](signedcode-certificates.md)<br/>     | Solo lectura<br/>  | Colección [**Certificates que**](certificates.md) contiene todos los certificados del archivo ejecutable firmado.<br/>             |
| [**Descripción**](signedcode-description.md)<br/>       | Lectura/escritura<br/> | Cadena que contiene una descripción del archivo ejecutable firmado.<br/>                                                             |
| [**DescriptionURL**](signedcode-descriptionurl.md)<br/> | Lectura/escritura<br/> | Cadena que contiene la dirección HTTP de una descripción del archivo ejecutable firmado.<br/>                                         |
| [**Nombre**](signedcode-filename.md)<br/>             | Lectura/escritura<br/> | Cadena que contiene la ruta de acceso al archivo de contenido que contiene el archivo ejecutable.<br/> Esta es la propiedad predeterminada.<br/> |
| [**Firmante**](signedcode-signer.md)<br/>                 | Solo lectura<br/>  | Objeto [**Signer**](signer.md) que proporciona acceso al firmante del archivo ejecutable.<br/>                                    |
| [**Timestamper**](signedcode-timestamper.md)<br/>       | Solo lectura<br/>  | Objeto [**Signer**](signer.md) que proporciona acceso al marca de tiempo del archivo ejecutable.<br/>                              |



 

## <a name="remarks"></a>Comentarios

Se puede crear el objeto **SignedCode** y no es seguro para el scripting. El ProgID del **objeto SignedCode** es CAPICOM. SignedCode.1.

El archivo ejecutable debe ser de un tipo que se pueda firmar con la tecnología Authenticode, por ejemplo, archivos que tengan una extensión de nombre de archivo de .cab, .cat, .exe, .dll, .vbs o .ocx.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
