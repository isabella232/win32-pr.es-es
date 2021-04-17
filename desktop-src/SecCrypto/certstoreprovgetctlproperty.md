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
ms.openlocfilehash: e30a9e735d44fc5681d5cd3932baaf3cc90aa30d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668101"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a>Función de devolución de llamada CertStoreProvGetCTLProperty

La función de devolución de llamada **CertStoreProvGetCTLProperty** recupera una propiedad especificada de una [*lista de certificados de confianza*](../secgloss/c-gly.md) (CTL).

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

*hStoreProv* \[ de\]
</dt> <dd>

Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pCtlContext* \[ de\]
</dt> <dd>

Puntero a una estructura [**de \_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .

</dd> <dt>

*dwPropId* \[ de\]
</dt> <dd>

Indica un identificador de propiedad.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Los valores de marca necesarios.

</dd> <dt>

*pvData* \[ enuncia\]
</dt> <dd>

Puntero a un búfer que va a contener el puntero a una estructura de [**\_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) que va a devolver la función. Para obtener el valor de *pcbData* antes de asignar memoria para el búfer, este parámetro se puede establecer en **null** en una primera llamada a la función.

</dd> <dt>

*pcbData* \[ in, out\]
</dt> <dd>

Un puntero a un **valor DWORD** que indica la longitud del búfer *pvData* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve un valor distinto de cero.

Si se produce un error en la función, devuelve cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_contexto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
