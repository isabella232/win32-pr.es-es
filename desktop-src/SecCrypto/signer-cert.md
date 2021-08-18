---
description: Especifica un certificado usado para firmar un documento. El certificado se puede almacenar en un archivo de certificado Publisher software (SPC) o en un almacén de certificados.
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: SIGNER_CERT estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT
api_type:
- NA
api_location: ''
ms.openlocfilehash: d31670575db045430e78b6c6b3182f4561b0d4784c1e1c0da95ff8629154d2c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898878"
---
# <a name="signer_cert-structure"></a>SIGNER \_ CERT (estructura)

La **estructura \_ SIGNER CERT** especifica un certificado que [*se*](../secgloss/c-gly.md) usa para firmar un documento. El certificado se puede almacenar en un archivo [*de certificado Publisher software*](../secgloss/s-gly.md) (SPC) o en un almacén de [*certificados*](../secgloss/c-gly.md).

> [!Note]  
> Esta estructura no se define en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo como se muestra en este tema.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _SIGNER_CERT {
  DWORD cbSize;
  DWORD dwCertChoice;
  union {
    LPCWSTR                pwszSpcFile;
    SIGNER_CERT_STORE_INFO *pCertStoreInfo;
    SIGNER_SPC_CHAIN_INFO  *pSpcChainInfo;
  };
  HWND  hwnd;
} SIGNER_CERT, *PSIGNER_CERT;
```



## <a name="members"></a>Miembros

<dl> <dt>

**cbSize**
</dt> <dd>

Tamaño, en bytes, de la estructura .

</dd> <dt>

**dwCertChoice**
</dt> <dd>

Especifica cómo se almacena el certificado. Este miembro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <dt>**FIRMANTE \_ CERT \_ SPC \_ FILE**</dt> <dt>1</dt> </dl>    | El certificado se almacena en un archivo SPC. El **miembro pwszSpcFile** contiene la ruta de acceso y el nombre de archivo del archivo SPC.<br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <dt>**FIRMANTE \_ CERT \_ STORE**</dt> <dt>2</dt> </dl>              | El certificado se almacena en un almacén de certificados. El **miembro pCertStoreInfo contiene** un puntero a una estructura [**\_ SIGNER CERT STORE \_ \_ INFO**](signer-cert-store-info.md) que especifica el almacén de certificados en el que se almacena el certificado.<br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <dt>**FIRMANTE \_ CERT \_ SPC \_ CHAIN**</dt> <dt>3</dt> </dl> | El certificado se almacena en un archivo SPC y está asociado a una cadena de certificados. El **miembro pSpcChainInfo** contiene un puntero a una estructura [**SIGNER \_ SPC CHAIN \_ \_ INFO**](signer-spc-chain-info.md) que contiene la información de cadena del certificado.<br/> |



 

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

Puntero a una cadena Unicode terminada en NULL que contiene la ruta de acceso y el nombre de archivo del archivo SPC en el que se almacena el certificado. Este miembro solo se usa si el **miembro dwCertChoice** contiene **SIGNER \_ CERT \_ SPC \_ FILE**.

</dd> <dt>

**pCertStoreInfo**
</dt> <dd>

Puntero a una estructura [**SIGNER \_ CERT STORE \_ \_ INFO**](signer-cert-store-info.md) que especifica el almacén de certificados en el que se almacena el certificado. Este miembro solo se usa si el **miembro dwCertChoice** contiene **SIGNER \_ CERT \_ STORE**.

</dd> <dt>

**pSpcChainInfo**
</dt> <dd>

Puntero a una estructura [**SIGNER \_ SPC \_ CHAIN \_ INFO**](signer-spc-chain-info.md) que contiene la información de cadena del certificado. Este miembro solo se usa si el **miembro dwCertChoice** contiene **SIGNER \_ CERT \_ SPC \_ CHAIN**.

</dd> <dt>

**Hwnd**
</dt> <dd>

Identificador de la ventana que se usará como propietario de los cuadros de diálogo que se muestran. Este miembro no se usa actualmente y se omite.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
