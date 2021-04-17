---
description: Recupera una propiedad especificada de un certificado.
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: Función de devolución de llamada CertStoreProvGetCertProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 50de9a73438e2755e002570f921d15e6086a4b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666985"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a>Función de devolución de llamada CertStoreProvGetCertProperty

La función de devolución de llamada **CertStoreProvGetCertProperty** recupera una propiedad especificada de un certificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
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

*pCertContext* \[ de\]
</dt> <dd>

Puntero a una estructura [**de \_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .

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

Puntero a un búfer que va a contener el puntero a una estructura de [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) que va a devolver la función. Se puede establecer en **null** en una primera llamada a la función para obtener el valor de *pcbData* antes de asignar memoria para el búfer.

</dd> <dt>

*pcbData* \[ in, out\]
</dt> <dd>

Un puntero a un **valor DWORD** que indica la longitud del búfer *pvData* .

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
</dt> </dl>

 

 
