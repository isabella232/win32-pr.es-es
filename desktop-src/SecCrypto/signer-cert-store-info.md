---
description: Especifica el almacén de certificados utilizado para firmar un documento.
ms.assetid: aabad010-6fa3-4677-bd73-b8c52d68dbc8
title: Estructura de SIGNER_CERT_STORE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT_STORE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 197bd4855a7d2afec4c0b23662365e5f9197e302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686986"
---
# <a name="signer_cert_store_info-structure"></a>Estructura de \_ \_ información del almacén de certificados del firmante \_

La estructura de **\_ \_ \_ información del almacén** de certificados del firmante especifica el almacén de certificados que se usa para firmar un documento.

> [!Note]  
> Esta estructura no está definida en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SIGNER_CERT_STORE_INFO {
  DWORD          cbSize;
  PCCERT_CONTEXT pSigningCert;
  DWORD          dwCertPolicy;
  HCERTSTORE     hCertStore;
} SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño de la estructura, en bytes.

</dd> <dt>

**pSigningCert**
</dt> <dd>

Puntero a una estructura [**de \_ contexto**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificado para el certificado de firma.

</dd> <dt>

**dwCertPolicy**
</dt> <dd>

Especifica cómo se agregan los certificados a la firma. Para encontrar la cadena de certificados, se comprueban los almacenes mis, CA, raíz y SPC, además del almacén especificado por el miembro **hCertStore** . Este miembro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <dt>**Firmante \_ \_ \_ Cadena de directiva de certificado**</dt> <dt>2 (0X2)</dt> </dl>                           | Agregue solo certificados en la cadena de certificados.<br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <dt>**Firmante \_ Cadena de directiva de certificado \_ \_ \_ sin \_ raíz**</dt> <dt>8 (0x8)</dt> </dl> | Agregue solo certificados en la cadena de certificados, excluido el certificado raíz.<br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <dt>**Firmante \_ \_ \_ Almacén de directivas de certificado**</dt> <dt>1 (0x1)</dt> </dl>                           | Agregue todos los certificados en el almacén especificado por el miembro **hCertStore** . Esta marca puede ser **una combinación OR bit a bit** con cualquiera de los otros valores posibles para este miembro.<br/> |



 

</dd> <dt>

**hCertStore**
</dt> <dd>

Opcional. Identificador de un almacén de certificados adicional.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**certificado del firmante \_**](signer-cert.md)
</dt> </dl>

 

 




