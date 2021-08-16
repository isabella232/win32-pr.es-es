---
description: Enumera o busca el primer certificado o el siguiente en un almacén externo que coincida con los criterios especificados.
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: Función de devolución de llamada CertStoreProvFindCert
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: a50a53e819fcfd12ff490b4e6642536c01d9a49b4e9345e7713bf0eb08a0fac6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770024"
---
# <a name="certstoreprovfindcert-callback-function"></a>Función de devolución de llamada CertStoreProvFindCert

La función de devolución de llamada **CertStoreProvFindCert** enumera o [](../secgloss/e-gly.md) busca el primer certificado o el siguiente en un almacén externo que coincida con los criterios especificados.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI CertStoreProvFindCert(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCERT_CONTEXT              pPrevCertContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCERT_CONTEXT              *ppProvCertContext
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

Puntero a una estructura FIND INFO de [**CERT \_ STORE \_ PROV \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) que contiene todos los parámetros pasados a la [**función CertFindCertificateInStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)

</dd> <dt>

*pPrevCertContext* \[ En\]
</dt> <dd>

Puntero a un [**CONTEXTO \_ CERT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) del certificado encontrado. En la primera llamada a la función, este parámetro debe establecerse en **NULL.** En las llamadas posteriores, se debe establecer en el puntero devuelto en el *parámetro ppProvCertContext* en la última llamada. La función **de** devolución de llamada libera un puntero que no es NULL pasado en este parámetro.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Cualquier valor de marca necesario.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Puntero a un puntero a un búfer para devolver la información del proveedor de almacén. Opcionalmente, la devolución de llamada puede devolver un puntero a la información de la buscar interna en este parámetro. Después de la primera llamada, este parámetro se establece en el puntero devuelto por la llamada anterior a la función .

</dd> <dt>

*ppProvCertContext* \[ out\]
</dt> <dd>

Si se encuentra correctamente, se devuelve un puntero al certificado encontrado en este parámetro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si la función se realiza correctamente o **FALSE** si se produce un error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CONTEXTO \_ DE CERTIFICADO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CERT \_ STORE \_ PROV \_ FIND \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
