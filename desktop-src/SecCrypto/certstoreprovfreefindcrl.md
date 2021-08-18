---
description: Se llama cuando no se usa el certificado devuelto por la devolución de llamada CertStoreProvFindCRL y, por tanto, se libera, en una llamada posterior a CertStoreProvFindCRL.
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: Función de devolución de llamada CertStoreProvFreeFindCRL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 1bf7e3b2518789bdf3755cefec0dcc27c88642c376cafca039ce5cc20533a068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769940"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a>Función de devolución de llamada CertStoreProvFreeFindCRL

Se llama a la función de devolución de llamada **CertStoreProvFreeFindCRL** cuando no se usó el certificado devuelto por la devolución de llamada [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) y, por tanto, se liberó en una llamada posterior a **CertStoreProvFindCRL**. Antes de llamar a la devolución de llamada CLOSE, el proveedor debe liberar todos los certificados devueltos por la devolución de llamada [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) mediante **CertStoreProvFindCRL** o **CertStoreProvFreeFindCRL.**

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
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

*pCrlContext* \[ En\]
</dt> <dd>

Puntero a UN [**CONTEXTO DE \_ CRL.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CertStoreProvFindCRL**](certstoreprovfindcrl.md)
</dt> <dt>

[**CONTEXTO \_ DE CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
