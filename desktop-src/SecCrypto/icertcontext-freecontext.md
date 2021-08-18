---
description: Libera un CONTEXTO DE PCCERT \_ adquirido a través de la propiedad CertContext.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: ICertContext::FreeContext (método)
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
ms.openlocfilehash: 06809d8950d62f1136b8efc25c8e5b4499e020dce956d65f9e0d4a0e349567de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006193"
---
# <a name="icertcontextfreecontext-method"></a>ICertContext::FreeContext (método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.\]

El **método FreeContext** libera un CONTEXTO DE PCCERT \_ adquirido a través de la propiedad [**CertContext.**](icertcontext-certcontext.md)

## <a name="syntax"></a>Sintaxis


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCertContext* \[ En\]
</dt> <dd>

Contexto de PCCERT \_ que se va a liberar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un HRESULT**. Un valor de S \_ OK indica que se ha correcto. Cualquier otro valor indica que se ha podido hacer la operación.

## <a name="remarks"></a>Comentarios

Este método no libera el contexto de PCCERT \_ incluido en un objeto [**Certificate.**](certificate.md) Solo se debe usar para liberar un CONTEXTO DE PCCERT \_ adquirido a través de la propiedad [**CertContext.**](icertcontext-certcontext.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ICertContext**](icertcontext.md)
</dt> </dl>

 

 




