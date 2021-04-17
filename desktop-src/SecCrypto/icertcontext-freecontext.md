---
description: Libera un \_ contexto PCCERT adquirido a través de la propiedad CertContext.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: 'ICertContext:: FreeContext (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.FreeContext
- CertContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e1f4c216f6e417726e60d5f2e2bd67387a51d352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671060"
---
# <a name="icertcontextfreecontext-method"></a>ICertContext:: FreeContext (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

El método **FreeContext** libera un \_ contexto PCCERT adquirido a través de la propiedad [**CertContext**](icertcontext-certcontext.md) .

## <a name="syntax"></a>Sintaxis


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCertContext* \[ de\]
</dt> <dd>

Contexto de PCCERT \_ que se va a liberar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **HRESULT**. Un valor de S \_ OK indica que se ha realizado correctamente. Cualquier otro valor indica que se produjo un error en la operación.

## <a name="remarks"></a>Observaciones

Este método no libera el contexto PCCERT \_ contenido dentro de un objeto de [**certificado**](certificate.md) . Solo se debe usar para liberar un contexto PCCERT \_ adquirido a través de la propiedad [**CertContext**](icertcontext-certcontext.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




