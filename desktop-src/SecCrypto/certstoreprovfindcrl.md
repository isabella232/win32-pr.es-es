---
description: Enumera o busca la primera CRL o la siguiente en un almacén externo que coincida con los criterios especificados.
ms.assetid: caf218f5-f379-4cb6-bb4b-4767b846d45c
title: Función de devolución de llamada CertStoreProvFindCRL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: eebcc990da0cd2d866325200223e9e654e45e055299a8b384a613dc9841c2799
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126685"
---
# <a name="certstoreprovfindcrl-callback-function"></a>Función de devolución de llamada CertStoreProvFindCRL

La función de devolución de llamada **CertStoreProvFindCRL** enumera o busca [](../secgloss/e-gly.md) la primera o la siguiente [*CRL*](../secgloss/c-gly.md) en un almacén externo que coincida con los criterios especificados.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CertStoreProvFindCRL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCRL_CONTEXT               pPrevCrlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCRL_CONTEXT               *ppProvCrlContext
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

Puntero a una estructura FIND INFO de [**CERT \_ STORE \_ PROV \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) que contiene todos los parámetros pasados a la [**función CertFindCRLInStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)

</dd> <dt>

*pPrevCrlContext* \[ En\]
</dt> <dd>

Puntero a una [**estructura CRL \_ CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) de la última CRL encontrada. En la primera llamada a la función, este parámetro debe establecerse en **NULL.** En las llamadas posteriores, se debe establecer en el puntero devuelto en el *parámetro ppProvCRLContext* en la última llamada. La función **de** devolución de llamada libera un puntero que no es NULL pasado en este parámetro.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Cualquier valor de marca necesario.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Puntero a un puntero a un búfer para devolver la información del proveedor de almacén. Opcionalmente, la devolución de llamada puede devolver un puntero a la información de la buscar interna en este parámetro. Después de la primera llamada, este parámetro se establece en el puntero devuelto por la llamada anterior a la función .

</dd> <dt>

*ppProvCrlContext* \[ out\]
</dt> <dd>

Si se encuentra correctamente, se devuelve un puntero a la CRL encontrada en este parámetro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la función se realiza correctamente o **FALSE** si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CERT \_ STORE \_ PROV \_ FIND \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[**CONTEXTO \_ DE CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
