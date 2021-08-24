---
description: Se llama cuando no se usa el certificado devuelto por la devolución de llamada CertStoreProvFindCert y, por tanto, se libera, en una llamada posterior a CertStoreProvFindCert.
ms.assetid: be882b56-027c-4540-9426-27d3c2b262e9
title: Función de devolución de llamada CertStoreProvFreeFindCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ab2a6ae1bd8199e7bed97626c83241223fc3943b94fcb387868331329d8740a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877305"
---
# <a name="certstoreprovfreefindcert-callback-function"></a>Función de devolución de llamada CertStoreProvFreeFindCert

Se llama a la función de devolución de llamada **CertStoreProvFreeFindCert** cuando no se usó el certificado devuelto por la devolución de llamada [**CertStoreProvFindCert**](certstoreprovfindcert.md) y, por tanto, se liberó en una llamada posterior a **CertStoreProvFindCert**. Antes de llamar a la devolución de llamada CLOSE, el proveedor debe liberar todos los certificados devueltos por la devolución de llamada [**CertStoreProvFindCert**](certstoreprovfindcert.md) mediante **CertStoreProvFindCert** o **CertStoreProvFreeFindCert.**

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CertStoreProvFreeFindCert(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCERT_CONTEXT pCertContext,
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

*pCertContext* \[ En\]
</dt> <dd>

Puntero a UN [**CONTEXTO \_ DE CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).

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

[**CONTEXTO \_ DE CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertStoreProvFindCert**](certstoreprovfindcert.md)
</dt> </dl>

 

 
