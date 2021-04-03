---
title: Propiedad PublisherCertificateChain de IMsRdpClientNonScriptable4
description: Controla la cadena de certificados del publicador. La cadena se almacena en una variante de tipo VT \_ BYREF que contiene un puntero a una estructura de contexto de cadena de certificados \_ \_ . Para obtener información acerca de las estructuras de VT \_ BYREF, consulte Variant y VARIANTARG.
ms.assetid: 27ab0aff-1aef-4701-abe0-849bf32c9773
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PublisherCertificateChain
- Propiedad PublisherCertificateChain Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad PublisherCertificateChain
- Propiedad PublisherCertificateChain Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad PublisherCertificateChain
- Servicios de Escritorio remoto de la propiedad PublisherCertificateChain, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad PublisherCertificateChain
- Servicios de Escritorio remoto de la propiedad PublisherCertificateChain, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad PublisherCertificateChain
- Servicios de Escritorio remoto de la propiedad PublisherCertificateChain, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad PublisherCertificateChain
- Servicios de Escritorio remoto de la propiedad PublisherCertificateChain, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad PublisherCertificateChain
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PublisherCertificateChain
- IMsRdpClientNonScriptable4.get_PublisherCertificateChain
- IMsRdpClientNonScriptable4.put_PublisherCertificateChain
- IMsRdpClientNonScriptable5.PublisherCertificateChain
- IMsRdpClientNonScriptable5.get_PublisherCertificateChain
- IMsRdpClientNonScriptable5.put_PublisherCertificateChain
- MsRdpClient6.PublisherCertificateChain
- MsRdpClient7.PublisherCertificateChain
- MsRdpClient8.PublisherCertificateChain
- MsRdpClient9.PublisherCertificateChain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7552483c2fc651ace1a9401e0555f90fb2584423
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905384"
---
# <a name="imsrdpclientnonscriptable4publishercertificatechain-property"></a>IMsRdpClientNonScriptable4::P propiedad ublisherCertificateChain

Controla la cadena de certificados del publicador. La cadena se almacena en una variante de tipo **VT \_ BYREF** que contiene un puntero a una estructura de [**\_ \_ contexto de cadena de certificados**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) . Para obtener información acerca de las estructuras de **VT \_ BYREF** , consulte [Variant y VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_PublisherCertificateChain(
  [in]  VARIANT *pVarCert
);

HRESULT get_PublisherCertificateChain(
  [out] VARIANT *pVarCert
);
```



## <a name="property-value"></a>Valor de propiedad

Establece la cadena de certificados del publicador. La cadena se almacena en una variante de tipo **VT \_ BYREF** que contiene un puntero a una estructura de [**\_ \_ contexto de cadena de certificados**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

