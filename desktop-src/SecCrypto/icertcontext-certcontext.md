---
description: Establece o recupera el contexto PCCERT \_ de un certificado.
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: 'ICertContext:: CertContext (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 38bd1c704ca709fc1e4b6072bb68c2105dc5db9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671058"
---
# <a name="icertcontextcertcontext-property"></a>ICertContext:: CertContext (propiedad)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

La propiedad **CertContext** establece o recupera el contexto PCCERT \_ de un certificado.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a>Valor de propiedad

Contexto PCCERT \_ del certificado.

## <a name="error-codes"></a>Códigos de error

Si los métodos de acceso de propiedad **colocan \_ CertContext** y **Get \_ CertContext** se ejecutan correctamente, devuelven los valores \_ correctos.

Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.

## <a name="remarks"></a>Observaciones

Debe llamar al método [**FreeContext**](icertcontext-freecontext.md) o a la función [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) para liberar el contexto.

Si establece la propiedad **CertContext** , se restablece el estado del objeto de [**certificado**](certificate.md) completo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




