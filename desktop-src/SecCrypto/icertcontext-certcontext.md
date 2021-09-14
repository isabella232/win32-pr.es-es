---
description: Establece o recupera el contexto de PCCERT \_ de un certificado.
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: ICertContext::CertContext, propiedad
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265316"
---
# <a name="icertcontextcertcontext-property"></a>ICertContext::CertContext, propiedad

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

La **propiedad CertContext** establece o recupera el CONTEXTO DE PCCERT \_ de un certificado.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a>Valor de propiedad

EL CONTEXTO DE \_ PCCERT del certificado.

## <a name="error-codes"></a>Códigos de error

Si los métodos de acceso de **propiedad \_ ponen CertContext** y **\_ obtienen CertContext** correctamente, devuelven S \_ OK.

Cualquier otro **valor HRESULT** indica que se ha dado error en la llamada.

## <a name="remarks"></a>Observaciones

Debe llamar al método [**FreeContext**](icertcontext-freecontext.md) o a la [**función CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) para liberar el contexto.

Si establece la **propiedad CertContext,** se restablece el estado de todo [**el objeto Certificate.**](certificate.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




