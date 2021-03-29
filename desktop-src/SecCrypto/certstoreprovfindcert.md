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
ms.openlocfilehash: 09701991d6b192d27f921642bfc960df819f9140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361014"
---
# <a name="certstoreprovfindcert-callback-function"></a>Función de devolución de llamada CertStoreProvFindCert

La función de devolución de llamada **CertStoreProvFindCert** enumera o busca el primer certificado o el siguiente en un [*almacén externo*](../secgloss/e-gly.md) que coincida con los criterios especificados.

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

*hStoreProv* \[ de\]
</dt> <dd>

Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pFindInfo* \[ de\]
</dt> <dd>

Un puntero a una estructura de [**\_ \_ \_ \_ información del Prov del almacén de certificados**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) que contiene todos los parámetros pasados a la función [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) .

</dd> <dt>

*pPrevCertContext* \[ de\]
</dt> <dd>

Un puntero a un [**\_ contexto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificado del certificado encontrado. En la primera llamada a la función, este parámetro debe establecerse en **null**. En las llamadas posteriores, debe establecerse en el puntero devuelto en el parámetro *ppProvCertContext* en la última llamada. La función de devolución de llamada libera un puntero no **nulo** que se pasa en este parámetro.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Los valores de marca necesarios.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Un puntero a un puntero a un búfer para devolver la información del proveedor de almacenamiento. Opcionalmente, la devolución de llamada puede devolver un puntero a información interna de búsqueda en este parámetro. Después de la primera llamada, este parámetro se establece en el puntero devuelto por la llamada anterior a la función.

</dd> <dt>

*ppProvCertContext* \[ enuncia\]
</dt> <dd>

Si la búsqueda se realiza correctamente, se devuelve un puntero al certificado encontrado en este parámetro.

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
</dt> <dt>

[**información de la búsqueda de almacén de certificados \_ \_ \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
