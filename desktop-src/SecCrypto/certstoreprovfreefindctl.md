---
description: Se llama cuando no se usó el certificado devuelto por la devolución de llamada CertStoreProvFindCTL y, por tanto, se libera, en una llamada subsiguiente a CertStoreProvFindCTL.
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
ms.openlocfilehash: ff0c9c3b7be6b8a4cafd759c3411f5096ee8640b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687387"
---
# <a name="certstoreprovfreefindctl-callback-function"></a>Función de devolución de llamada CertStoreProvFreeFindCTL

Se llama a la función de devolución de llamada **CertStoreProvFreeFindCTL** cuando no se usó el certificado devuelto por la devolución de llamada [**CertStoreProvFindCTL**](certstoreprovfindctl.md) y, por tanto, se libera, en una llamada subsiguiente a **CertStoreProvFindCTL**. Antes de que se llame a la devolución de llamada de cierre, el proveedor debe liberar todos los certificados devueltos por la devolución de llamada de [**CertStoreProvFindCTL**](certstoreprovfindctl.md) mediante **CertStoreProvFindCTL** o **CertStoreProvFreeFindCTL**.

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

*hStoreProv* \[ de\]
</dt> <dd>

Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCtlContext* \[ de\]
</dt> <dd>

Puntero a una estructura [**de \_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .

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

[**CertStoreProvFindCTL**](certstoreprovfindctl.md)
</dt> <dt>

[**\_contexto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
