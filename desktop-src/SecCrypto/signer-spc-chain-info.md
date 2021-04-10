---
description: Especifica un certificado de editor de software (SPC) y una cadena de certificados que se usan para firmar un documento.
ms.assetid: b65b4129-df92-410c-b372-b0c004f8bb03
title: Estructura de SIGNER_SPC_CHAIN_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SPC_CHAIN_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60279a60e6cdfbf43a1e2d9c45735b885d97a055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156496"
---
# <a name="signer_spc_chain_info-structure"></a>Estructura de \_ \_ información de cadena SPC de firmante \_

La estructura de **\_ \_ \_ información de cadena SPC del firmante** especifica un certificado de editor de [*software*](../secgloss/s-gly.md) (SPC) y una cadena de certificados que se usan para firmar un documento.

> [!Note]  
> Esta estructura no está definida en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SIGNER_SPC_CHAIN_INFO {
  DWORD      cbSize;
  LPCWSTR    pwszSpcFile;
  DWORD      dwCertPolicy;
  HCERTSTORE hCertStore;
} SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño de la estructura, en bytes.

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

Nombre del archivo SPC que se va a utilizar para firmar un documento.

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

 

 
