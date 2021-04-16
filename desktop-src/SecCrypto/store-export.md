---
description: Copia el contenido de un almacén de certificados abierto en una cadena codificada.
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Store. Export (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dbf4a2912cb62935447daa1589b6829c5a96488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671404"
---
# <a name="storeexport-method"></a>Store. Export (método)

\[El método de **exportación** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**clase X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **Export** copia el contenido de un [*almacén de certificados*](../secgloss/c-gly.md) abierto en una cadena codificada.

## <a name="syntax"></a>Sintaxis


```VB
Store.Export( _
  [ ByVal SaveAs ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Guardar como* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de [ \_ \_ Guardar \_ como \_ tipo de almacenamiento de CAPICOM](capicom-store-save-as-type.md) que indica el formato de la operación de exportación. El valor predeterminado es CAPICOM \_ Store \_ Save \_ como \_ serializado. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                     | Significado                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <dt>**el \_ almacén \_ de CAPICOM se guardó \_ como \_ serializado**</dt> </dl> | El almacén se guarda en formato serializado.<br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <dt>**El \_ almacén \_ de CAPICOM se guarda \_ como \_ pkcs7**</dt> </dl>                | El almacén se guarda en \# formato PKCS 7.<br/>   |



 

</dd> <dt>

*EncodingType* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de [ \_ \_ tipo de codificación CAPICOM](capicom-encoding-type.md) que indica el tipo de codificación del almacén exportado. El valor predeterminado es CAPICOM \_ encode \_ Base64. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ codificar \_ any**</dt> </dl>          | Este tipo de codificación solo se utiliza cuando los datos de entrada tienen un tipo de codificación desconocido. Si este valor se usa para especificar el tipo de codificación de la salida, \_ se usará CAPICOM encode \_ Base64 en su lugar. Introducido en CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM, codificación \_ \_ Base64**</dt> </dl> | Los datos se guardan como una cadena codificada en Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_código binario de codificación de CAPICOM \_**</dt> </dl> | Los datos se guardan como una secuencia binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una cadena que contiene los certificados del almacén en el formato de codificación especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Store**](store.md)
</dt> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
