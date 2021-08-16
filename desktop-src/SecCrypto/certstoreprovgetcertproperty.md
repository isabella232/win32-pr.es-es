---
description: Recupera una propiedad especificada de un certificado.
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: Función de devolución de llamada CertStoreProvGetCertProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c7d338c94c4e9655c125b0f70e3f2e8dfa732316a970c74c26e4a7fbced22671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769930"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a>Función de devolución de llamada CertStoreProvGetCertProperty

La **función de devolución de llamada CertStoreProvGetCertProperty** recupera una propiedad especificada de un certificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
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

**Identificador de HCERTSTOREPROV** a un [*almacén de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCertContext* \[ En\]
</dt> <dd>

Puntero a una [**estructura CERT \_ CONTEXT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

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

Puntero a un búfer que contiene el puntero a una estructura [**CERT \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) que va a devolver la función. Se puede establecer en **NULL en** una primera llamada a la función para obtener el valor de *pwData antes* de asignar memoria para el búfer.

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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CONTEXTO \_ DE CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
