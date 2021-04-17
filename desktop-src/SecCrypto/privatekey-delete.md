---
description: Elimina el contenedor de claves privadas al que hace referencia el objeto PrivateKey.
ms.assetid: 80bbe46b-1ec5-4d47-82b0-5a3177f86389
title: PrivateKey. Delete (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dc5778e631abba9eb8cf122ddb99a4692c988f4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670553"
---
# <a name="privatekeydelete-method"></a>PrivateKey. Delete (método)

\[El método **Delete** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**propiedad X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **Delete** elimina el contenedor de claves privadas al que hace referencia el objeto [**PrivateKey**](privatekey.md) .

## <a name="syntax"></a>Sintaxis


```VB
PrivateKey.Delete()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

> [!IMPORTANT]
> Este método elimina el contenedor de claves privadas al que hace referencia el objeto [**PrivateKey**](privatekey.md) así como todas las claves privadas del contenedor. Cualquier elemento cifrado con las claves públicas correspondientes a las claves privadas eliminadas ya no se podrá descifrar.

 

Este método produce CAPICOM \_ E \_ no \_ se permite cuando se genera un script desde una aplicación basada en Web.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
