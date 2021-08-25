---
description: Se llama cuando no se usa el certificado devuelto por la devolución de llamada CertStoreProvFindCTL y, por tanto, se libera, en una llamada posterior a CertStoreProvFindCTL.
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: Función de devolución de llamada CertStoreProvFreeFindCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5f3f6d224ed19073408015b3b83b90a66e9402d9b838d50eb7a8381e312e0534
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877145"
---
# <a name="certstoreprovfreefindctl-callback-function"></a>Función de devolución de llamada CertStoreProvFreeFindCTL

Se llama a la función de devolución de llamada **CertStoreProvFreeFindCTL** cuando no se usó el certificado devuelto por la devolución de llamada [**CertStoreProvFindCTL**](certstoreprovfindctl.md) y, por tanto, se liberó en una llamada posterior a **CertStoreProvFindCTL.** Antes de llamar a la devolución de llamada CLOSE, el proveedor debe liberar todos los certificados devueltos por la devolución de llamada [**CertStoreProvFindCTL**](certstoreprovfindctl.md) mediante **CertStoreProvFindCTL** o **CertStoreProvFreeFindCTL.**

## <a name="syntax"></a>Sintaxis


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hStoreProv* \[ En\]
</dt> <dd>

**Identificador de HCERTSTOREPROV** a un [*almacén de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCtlContext* \[ En\]
</dt> <dd>

Puntero a una [**estructura CONTEXT \_ de CTL.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

</dd> <dt>

*pvStoreProvFindInfo* \[ En\]
</dt> <dd>

Puntero a un búfer que contiene información de buscar.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Cualquier valor de marca necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la función se realiza correctamente o **FALSE** si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CertStoreProvFindCTL**](certstoreprovfindctl.md)
</dt> <dt>

[**CONTEXTO DE \_ CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
