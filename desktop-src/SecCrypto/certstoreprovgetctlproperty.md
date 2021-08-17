---
description: Recupera una propiedad especificada de una lista de certificados de confianza (CTL).
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: Función de devolución de llamada CertStoreProvGetCTLProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 1677c2cccbdf0b422696437736380bd0bb57542220a898332d72ec7a0562fd1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769764"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a>Función de devolución de llamada CertStoreProvGetCTLProperty

La **función de devolución de llamada CertStoreProvGetCTLProperty** recupera una propiedad especificada de una lista de certificados [*de confianza*](../secgloss/c-gly.md) (CTL).

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
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

Identificador **de HCERTSTOREPROV** para un [*almacén de certificados.*](../secgloss/c-gly.md)

</dd> <dt>

*pCtlContext* \[ En\]
</dt> <dd>

Puntero a una [**estructura CONTEXT \_ de CTL.**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)

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

Puntero a un búfer que contiene el puntero a una estructura [**CONTEXT \_ de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) que va a devolver la función. Para obtener el valor de *pwData antes* de asignar memoria para el búfer, este parámetro se puede establecer en **NULL** en una primera llamada a la función.

</dd> <dt>

*pwData* \[ in, out\]
</dt> <dd>

Puntero a un **DWORD** que indica la longitud del *búfer pvData.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve un valor distinto de cero.

Si se produce un error en la función, devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CONTEXTO DE \_ CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
