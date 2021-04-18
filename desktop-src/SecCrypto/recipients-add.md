---
description: Agrega un objeto de certificado a una colección de destinatarios.
ms.assetid: 2a1b9e0f-ccbf-4042-871b-397de6b6fc35
title: Recipients. Add (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 255d17485e3423d50cd86b092c2120605f0f1106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670654"
---
# <a name="recipientsadd-method"></a>Recipients. Add (método)

\[El método **Add** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El método **Add** agrega un objeto de [**certificado**](certificate.md) a una colección de [**destinatarios**](recipients.md) .

## <a name="syntax"></a>Sintaxis


```VB
Recipients.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Certificado* \[ de de\]
</dt> <dd>

Expresión que se resuelve en el objeto de [**certificado**](certificate.md) que se va a agregar a la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> <dt>

[**Recipients**](recipients.md)
</dt> </dl>

 

 
