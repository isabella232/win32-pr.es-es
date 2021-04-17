---
description: Especifica un certificado usado para firmar un documento. El certificado se puede almacenar en un archivo de certificado de editor de software (SPC) o en un almacén de certificados.
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: Estructura de SIGNER_CERT
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
ms.openlocfilehash: a14f955749e98ca34cda0be2c57a3d5c546afc41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278425"
---
# <a name="signer_cert-structure"></a>Estructura del \_ certificado del firmante

La estructura del certificado del **firmante \_** especifica un [*certificado*](../secgloss/c-gly.md) usado para firmar un documento. El certificado se puede almacenar en un archivo de [*certificado de editor de software*](../secgloss/s-gly.md) (SPC) o en un almacén de [*certificados*](../secgloss/c-gly.md).

> [!Note]  
> Esta estructura no está definida en ningún archivo de encabezado. Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.

 

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

Tamaño de la estructura, en bytes.

</dd> <dt>

**dwCertChoice**
</dt> <dd>

Especifica cómo se almacena el certificado. Este miembro puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                                          | Significado                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <dt>**Firmante \_ \_ \_ Archivo SPC de certificado**</dt> <dt>1</dt> </dl>    | El certificado se almacena en un archivo SPC. El miembro **pwszSpcFile** contiene la ruta de acceso y el nombre del archivo SPC.<br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <dt>**Firmante \_ \_Almacén de certificados**</dt> <dt>2</dt> </dl>              | El certificado se almacena en un almacén de certificados. El miembro **pCertStoreInfo** contiene un puntero a una estructura de [**\_ \_ \_ información del almacén**](signer-cert-store-info.md) de certificados del firmante que especifica el almacén de certificados en el que se almacena el certificado.<br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <dt>**Firmante \_ \_ \_ Cadena SPC de CERT**</dt> <dt></dt> </dl> | El certificado se almacena en un archivo SPC y está asociado a una cadena de certificados. El miembro **pSpcChainInfo** contiene un puntero a una estructura de [**\_ \_ \_ información de cadena SPC de firmante**](signer-spc-chain-info.md) que contiene la información de la cadena para el certificado.<br/> |



 

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

Puntero a una cadena Unicode terminada en null que contiene la ruta de acceso y el nombre del archivo SPC en el que se almacena el certificado. Este miembro solo se utiliza si el miembro **dwCertChoice** contiene el **\_ \_ \_ archivo SPC del certificado del firmante**.

</dd> <dt>

**pCertStoreInfo**
</dt> <dd>

Puntero a una estructura de [**\_ \_ \_ información del almacén**](signer-cert-store-info.md) de certificados del firmante que especifica el almacén de certificados en el que se almacena el certificado. Este miembro solo se utiliza si el miembro **dwCertChoice** contiene el **\_ \_ almacén de certificados del firmante**.

</dd> <dt>

**pSpcChainInfo**
</dt> <dd>

Puntero a una estructura de [**\_ \_ \_ información de cadena SPC de firmante**](signer-spc-chain-info.md) que contiene la información de cadena para el certificado. Este miembro solo se utiliza si el miembro **dwCertChoice** contiene la **\_ \_ \_ cadena SPC del certificado del firmante**.

</dd> <dt>

**identificador**
</dt> <dd>

Identificador de la ventana que se va a usar como propietario de los cuadros de diálogo que se muestran. Este miembro no se utiliza actualmente y se omite.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
