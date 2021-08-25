---
description: Recupera una propiedad especificada de una CRL.
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: Función de devolución de llamada CertStoreProvGetCRLProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 2662c29ede9feec90b10869a4dc21277a8c6bdc6243e60ce894819e4b27dce5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877055"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a>Función de devolución de llamada CertStoreProvGetCRLProperty

La **función de devolución de llamada CertStoreProvGetCRLProperty** recupera una propiedad especificada de [*una CRL.*](../secgloss/c-gly.md)

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hStoreProv* \[ En\]
</dt> <dd>

**Identificador HCERTSTOREPROV** para un [*almacén de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCrlContext* \[ En\]
</dt> <dd>

Puntero a una [**estructura CONTEXT \_ de CRL.**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)

</dd> <dt>

*dwPropId* \[ En\]
</dt> <dd>

Indica un identificador de propiedad.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Cualquier valor de marca necesario.

</dd> <dt>

*pvData* \[ out\]
</dt> <dd>

Puntero a un búfer que contiene el puntero a una estructura CONTEXT de [**CRL \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) que va a devolver la función. Se puede establecer en **NULL en** una primera llamada a la función para obtener el valor de *pwData* antes de asignar memoria para el búfer.

</dd> <dt>

*pwData* \[ in, out\]
</dt> <dd>

Puntero a un **DWORD** que indica la longitud del *búfer pvData.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la función se realiza correctamente o **FALSE** si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CONTEXTO \_ DE CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
