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
ms.openlocfilehash: 08648c8b941874a6d1e1ed97d49f510694b998b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671644"
---
# <a name="signedcode-object"></a>Objeto SignedCode

\[El objeto **SignedCode** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md)y [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) de la API Win32 para firmar el contenido con una firma digital Authenticode. Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

El objeto **SignedCode** proporciona funcionalidad para firmar archivos ejecutables con una firma digital Authenticode.

## <a name="when-to-use"></a>Cuándo se usa

El objeto **SignedCode** se usa para realizar las siguientes tareas:

-   Firmar archivos ejecutables.
-   Archivos ejecutables de marca de tiempo.
-   Determine si la firma del archivo ejecutable es válida.
-   Establezca o recupere la ruta de acceso al archivo ejecutable.
-   Recupere el autor de firma y hora del archivo ejecutable.
-   Recupera una colección de los certificados para el archivo ejecutable.
-   Recupere una descripción o la dirección URL de la descripción del archivo ejecutable.

## <a name="members"></a>Miembros

El objeto **SignedCode** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SignedCode** tiene estos métodos.



| Método                                    | Descripción                                                                                                                                                         |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Sesión**](signedcode-sign.md)           | Crea una firma digital Authenticode y firma el archivo ejecutable especificado en la propiedad [**SignedCode. FileName**](signedcode-filename.md) .<br/>    |
| [**Indicaciones**](signedcode-timestamp.md) | Crea una firma de marca de tiempo Authenticode en el archivo ejecutable firmado especificado en la propiedad [**SignedCode. FileName**](signedcode-filename.md) .<br/> |
| [**Ver**](signedcode-verify.md)       | Comprueba la firma Authenticode del archivo ejecutable firmado especificado en la propiedad [**SignedCode. FileName**](signedcode-filename.md) .<br/>          |



 

### <a name="properties"></a>Propiedades

El objeto **SignedCode** tiene estas propiedades.



| Propiedad                                                       | Tipo de acceso           | Descripción                                                                                                                                |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](signedcode-certificates.md)<br/>     | Solo lectura<br/>  | Colección de [**certificados**](certificates.md) que contiene todos los certificados del archivo ejecutable firmado.<br/>             |
| [**Descripción**](signedcode-description.md)<br/>       | Lectura/escritura<br/> | Una cadena que contiene una descripción del archivo ejecutable firmado.<br/>                                                             |
| [**DescriptionURL**](signedcode-descriptionurl.md)<br/> | Lectura/escritura<br/> | Una cadena que contiene la dirección HTTP a una descripción del archivo ejecutable firmado.<br/>                                         |
| [**Extensión**](signedcode-filename.md)<br/>             | Lectura/escritura<br/> | Cadena que contiene la ruta de acceso al archivo de contenido que contiene el archivo ejecutable.<br/> Esta es la propiedad predeterminada.<br/> |
| [**Firmante**](signedcode-signer.md)<br/>                 | Solo lectura<br/>  | Objeto de [**firmante**](signer.md) que proporciona acceso al firmante del archivo ejecutable.<br/>                                    |
| [**Marca de tiempo**](signedcode-timestamper.md)<br/>       | Solo lectura<br/>  | Objeto de [**firmante**](signer.md) que proporciona acceso a la autor horaria del archivo ejecutable.<br/>                              |



 

## <a name="remarks"></a>Observaciones

El objeto **SignedCode** se puede crear y no es seguro para el scripting. El ProgID del objeto **SignedCode** es CAPICOM. SignedCode. 1.

El archivo ejecutable debe ser de un tipo que se pueda firmar con la tecnología Authenticode; por ejemplo, los archivos que tienen una extensión de nombre de archivo. cab,. cat,. exe,. dll,. vbs o. ocx.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
