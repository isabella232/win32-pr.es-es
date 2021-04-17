---
description: Enumera o busca la primera o siguiente CTL en un almacén externo que coincida con los criterios especificados.
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: Función de devolución de llamada CertStoreProvFindCTL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 9454f918c9cbc5b6f90642d46fbb33573b70457f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668103"
---
# <a name="certstoreprovfindctl-callback-function"></a>Función de devolución de llamada CertStoreProvFindCTL

La función de devolución de llamada **CertStoreProvFindCTL** enumera o encuentra la primera o siguiente [*CTL*](../secgloss/c-gly.md) en un [*almacén externo*](../secgloss/e-gly.md) que coincide con los criterios especificados.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CertStoreProvFindCTL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCTL_CONTEXT               pPrevCtlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCTL_CONTEXT               *ppProvCtlContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hStoreProv* \[ de\]
</dt> <dd>

Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pFindInfo* \[ de\]
</dt> <dd>

Un puntero a una estructura de [**\_ \_ \_ \_ información de Prov del almacén de certificados**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) que contiene todos los parámetros pasados a [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore). .

</dd> <dt>

*pPrevCtlContext* \[ de\]
</dt> <dd>

Puntero a una estructura [**de \_ contexto de CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) de la última CTL encontrada. En la primera llamada a la función, este parámetro debe establecerse en **null**. En las llamadas posteriores, debe establecerse en el puntero devuelto en el parámetro *ppProvCTLContext* en la última llamada. La función de devolución de llamada libera un puntero no **nulo** que se pasa en este parámetro.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Los valores de marca necesarios.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Un puntero a un puntero a un búfer para devolver la información del proveedor de almacenamiento. Opcionalmente, la devolución de llamada puede devolver un puntero a información interna de búsqueda en este parámetro. Después de la primera llamada, este parámetro se establece en el puntero devuelto por la llamada anterior a la función.

</dd> <dt>

*ppProvCtlContext* \[ enuncia\]
</dt> <dd>

Si la búsqueda se realiza correctamente, se devuelve un puntero a la CTL encontrada en este parámetro.

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

[**información de la búsqueda de almacén de certificados \_ \_ \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[**\_contexto CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
