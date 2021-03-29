---
description: Se llama cuando no se usó el certificado devuelto por la devolución de llamada CertStoreProvFindCRL y, por tanto, se libera, en una llamada subsiguiente a CertStoreProvFindCRL.
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
ms.openlocfilehash: b5f5443d58a86c8bab979d17d64dc693d94ae373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911786"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a>Función de devolución de llamada CertStoreProvFreeFindCRL

Se llama a la función de devolución de llamada **CertStoreProvFreeFindCRL** cuando no se usó el certificado devuelto por la devolución de llamada [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) y, por tanto, se libera, en una llamada subsiguiente a **CertStoreProvFindCRL**. Antes de que se llame a la devolución de llamada de cierre, el proveedor debe liberar todos los certificados devueltos por la devolución de llamada de [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) mediante **CertStoreProvFindCRL** o **CertStoreProvFreeFindCRL**.

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

*hStoreProv* \[ de\]
</dt> <dd>

Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCrlContext* \[ de\]
</dt> <dd>

Un puntero a un [**\_ contexto de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).

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

[**CertStoreProvFindCRL**](certstoreprovfindcrl.md)
</dt> <dt>

[**contexto de CRL \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
