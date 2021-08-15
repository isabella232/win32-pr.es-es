---
description: Enumera o busca la primera CTL o la siguiente en un almacén externo que coincida con los criterios especificados.
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
ms.openlocfilehash: f3064b42961196a7522fba6d08ac684aa4421b26727cdf229854351c777a4b56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770014"
---
# <a name="certstoreprovfindctl-callback-function"></a>Función de devolución de llamada CertStoreProvFindCTL

La función de devolución de llamada **CertStoreProvFindCTL** enumera o [](../secgloss/e-gly.md) busca la primera o la siguiente [*CTL*](../secgloss/c-gly.md) en un almacén externo que coincida con los criterios especificados.

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

*hStoreProv* \[ En\]
</dt> <dd>

**Identificador HCERTSTOREPROV** para un [*almacén de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pFindInfo* \[ En\]
</dt> <dd>

Puntero a una estructura FIND INFO de [**CERT \_ STORE \_ \_ \_ PROV**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) que contiene todos los parámetros pasados a [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore). .

</dd> <dt>

*pPrevCtlContext* \[ En\]
</dt> <dd>

Puntero a una [**estructura CTL \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) de la última CTL encontrada. En la primera llamada a la función, este parámetro debe establecerse en **NULL.** En las llamadas posteriores, se debe establecer en el puntero devuelto en el *parámetro ppProvCTLContext* en la última llamada. La función **de** devolución de llamada libera un puntero que no es NULL pasado en este parámetro.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Cualquier valor de marca necesario.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Puntero a un puntero al búfer para devolver la información del proveedor de almacén. Opcionalmente, la devolución de llamada puede devolver un puntero a la información de la buscar interna en este parámetro. Después de la primera llamada, este parámetro se establece en el puntero devuelto por la llamada anterior a la función .

</dd> <dt>

*ppProvCtlContext* \[ out\]
</dt> <dd>

Si se encuentra correctamente, se devuelve un puntero a la CTL encontrada en este parámetro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la función se realiza correctamente o **FALSE** si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CERT \_ STORE \_ PROV \_ FIND \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[**CONTEXTO DE \_ CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
