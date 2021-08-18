---
description: Llamado por CertDeleteCTLFromStore antes de eliminar una CTL del almacén.
ms.assetid: 6cda772f-7e94-414d-99fc-a90451ac0ccf
title: Función de devolución de llamada CertStoreProvDeleteCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvDeleteCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: befc031c1be441ad23c7a50563030775b625b81b66a9e1f92df4fb7c641fe73c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993095"
---
# <a name="certstoreprovdeletectl-callback-function"></a>Función de devolución de llamada CertStoreProvDeleteCTL

[**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) llama a la función de devolución de llamada **CertStoreProvDeleteCTL** antes de eliminar una CTL del almacén. Esta función determina si se puede eliminar una CTL.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CertStoreProvDeleteCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hStoreProv* \[ En\]
</dt> <dd>

**Identificador HCERTSTOREPROV** para un [*almacén de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCtlContext* \[ En\]
</dt> <dd>

Puntero a una [**estructura CTL \_ CONTEXT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Cualquier valor de marca necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si se puede eliminar una CTL del almacén.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



 

 
