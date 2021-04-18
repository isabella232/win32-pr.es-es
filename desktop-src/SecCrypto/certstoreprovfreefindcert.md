---
description: Se llama cuando no se usó el certificado devuelto por la devolución de llamada CertStoreProvFindCert y, por tanto, se libera, en una llamada subsiguiente a CertStoreProvFindCert.
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
ms.openlocfilehash: 320145ebfe95d1e678193ea1b11e7cb0d5294c69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668102"
---
# <a name="certstoreprovfreefindcert-callback-function"></a>Función de devolución de llamada CertStoreProvFreeFindCert

Se llama a la función de devolución de llamada **CertStoreProvFreeFindCert** cuando no se usó el certificado devuelto por la devolución de llamada [**CertStoreProvFindCert**](certstoreprovfindcert.md) y, por tanto, se libera, en una llamada subsiguiente a **CertStoreProvFindCert**. Antes de que se llame a la devolución de llamada de cierre, el proveedor debe liberar todos los certificados devueltos por la devolución de llamada de [**CertStoreProvFindCert**](certstoreprovfindcert.md) mediante **CertStoreProvFindCert** o **CertStoreProvFreeFindCert**.

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

*hStoreProv* \[ de\]
</dt> <dd>

Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCertContext* \[ de\]
</dt> <dd>

Un puntero a un [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).

</dd> <dt>

*pvStoreProvFindInfo* \[ de\]
</dt> <dd>

Un puntero a un búfer que contiene información de búsqueda.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Los valores de marca necesarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si la función se ejecuta correctamente o **false** si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**contexto de certificado \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertStoreProvFindCert**](certstoreprovfindcert.md)
</dt> </dl>

 

 
