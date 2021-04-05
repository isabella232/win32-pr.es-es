---
description: Lo llama CertDeleteCTLFromStore antes de eliminar una CTL del almacén.
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
ms.openlocfilehash: abeea0fdc3b6d77974b2c057d0e2ea98fe11e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908970"
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

*hStoreProv* \[ de\]
</dt> <dd>

Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCtlContext* \[ de\]
</dt> <dd>

Puntero a una estructura [**de \_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Los valores de marca necesarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si se puede eliminar una CTL del almacén.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



 

 
