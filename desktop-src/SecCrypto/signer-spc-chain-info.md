---
description: Especifica un certificado de Publisher software (SPC) y una cadena de certificados que se usan para firmar un documento.
ms.assetid: b65b4129-df92-410c-b372-b0c004f8bb03
title: SIGNER_SPC_CHAIN_INFO estructura
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
ms.openlocfilehash: ff646da815604082024f7a811f21e786abaece7b8e34944d9bd229c4624ed511
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898638"
---
# <a name="signer_spc_chain_info-structure"></a>Estructura SIGNER \_ SPC \_ CHAIN \_ INFO

La **estructura SIGNER \_ SPC CHAIN \_ \_ INFO** especifica un certificado de [*Publisher*](../secgloss/s-gly.md) software (SPC) y una cadena de certificados que se usan para firmar un documento.

> [!Note]  
> Esta estructura no está definida en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo como se muestra en este tema.

 

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

Tamaño, en bytes, de la estructura .

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

Nombre del archivo SPC que se va a usar para firmar un documento.

</dd> <dt>

**dwCertPolicy**
</dt> <dd>

Especifica cómo se agregan certificados a la firma. Para buscar la cadena de certificados, se comprueban los almacenes MY, CA, ROOT y SPC, además del almacén especificado por el **miembro hCertStore.** Este miembro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <dt>**SIGNER \_ CERT \_ POLICY \_ CHAIN**</dt> <dt>2 (0x2)</dt> </dl>                           | Agregue solo certificados en la cadena de certificados.<br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <dt>**SIGNER \_ CERT \_ POLICY CHAIN NO \_ \_ \_ ROOT**</dt> <dt>8 (0x8)</dt> </dl> | Agregue solo certificados en la cadena de certificados, excepto el certificado raíz.<br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <dt>**SIGNER \_ ALMACÉN \_ DE DIRECTIVAS DE \_ CERT**</dt> <dt>1 (0x1)</dt> </dl>                           | Agregue todos los certificados en el almacén especificado por el **miembro hCertStore.** Esta marca puede ser una combinación or bit a bit con cualquiera de los otros valores posibles para este miembro.<br/> |



 

</dd> <dt>

**hCertStore**
</dt> <dd>

Opcional. Identificador de un almacén de certificados adicional.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CERTIFICADO DE \_ FIRMANTE**](signer-cert.md)
</dt> </dl>

 

 
