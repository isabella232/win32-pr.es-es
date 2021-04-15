---
description: Enumera o busca la primera o siguiente CRL en un almacén externo que coincida con los criterios especificados.
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
ms.openlocfilehash: b20b7a4b677356e59be9f2f6df47b260c12d2f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546307"
---
# <a name="certstoreprovfindcrl-callback-function"></a>Función de devolución de llamada CertStoreProvFindCRL

La función de devolución de llamada **CertStoreProvFindCRL** enumera o busca la primera o la siguiente [*CRL*](../secgloss/c-gly.md) en un [*almacén*](../secgloss/e-gly.md) externo que coincida con los criterios especificados.

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

*hStoreProv* \[ de\]
</dt> <dd>

Identificador de **HCERTSTOREPROV** de un [*almacén de certificados*](../secgloss/c-gly.md).

</dd> <dt>

*pFindInfo* \[ de\]
</dt> <dd>

Un puntero a una estructura de [**\_ \_ \_ \_ información del Prov del almacén de certificados**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) que contiene todos los parámetros pasados a la función [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) .

</dd> <dt>

*pPrevCrlContext* \[ de\]
</dt> <dd>

Puntero a una estructura [**de \_ contexto de CRL**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) de la última CRL encontrada. En la primera llamada a la función, este parámetro debe establecerse en **null**. En las llamadas posteriores, debe establecerse en el puntero devuelto en el parámetro *ppProvCRLContext* en la última llamada. La función de devolución de llamada libera un puntero no **nulo** que se pasa en este parámetro.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Los valores de marca necesarios.

</dd> <dt>

*ppvStoreProvFindInfo* \[ in, out\]
</dt> <dd>

Un puntero a un puntero a un búfer para devolver la información del proveedor de almacenamiento. Opcionalmente, la devolución de llamada puede devolver un puntero a información interna de búsqueda en este parámetro. Después de la primera llamada, este parámetro se establece en el puntero devuelto por la llamada anterior a la función.

</dd> <dt>

*ppProvCrlContext* \[ enuncia\]
</dt> <dd>

Si la búsqueda se realiza correctamente, se devuelve un puntero a la CRL encontrada en este parámetro.

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

[**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[**contexto de CRL \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
