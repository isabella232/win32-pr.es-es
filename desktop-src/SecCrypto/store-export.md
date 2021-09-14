---
description: Copia el contenido de un almacén de certificados abierto en una cadena codificada.
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Método Store.Export
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170857"
---
# <a name="storeexport-method"></a>Método Store.Export

\[El **método Export** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Export** copia el contenido de un almacén de certificados [*abierto*](../secgloss/c-gly.md) en una cadena codificada.

## <a name="syntax"></a>Sintaxis


```VB
Store.Export( _
  [ ByVal SaveAs ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SaveAs* \[ in, opcional\]
</dt> <dd>

Valor de la [enumeración CAPICOM \_ STORE SAVE AS \_ \_ \_ TYPE](capicom-store-save-as-type.md) que indica el formato de la operación de exportación. El valor predeterminado es CAPICOM \_ STORE \_ SAVE AS \_ \_ SERIALIZED. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                     | Significado                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <dt>**CAPICOM \_ STORE \_ SAVE \_ AS \_ SERIALIZED**</dt> </dl> | El almacén se guarda en formato serializado.<br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <dt>**CAPICOM \_ STORE \_ SAVE \_ AS \_ PKCS7**</dt> </dl>                | El almacén se guarda en formato PKCS \# 7.<br/>   |



 

</dd> <dt>

*EncodingType* \[ in, opcional\]
</dt> <dd>

Valor de la enumeración [CAPICOM \_ ENCODING \_ TYPE](capicom-encoding-type.md) que indica el tipo de codificación del almacén exportado. El valor predeterminado es CAPICOM \_ ENCODE \_ BASE64. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ ENCODE \_ ANY**</dt> </dl>          | Este tipo de codificación solo se usa cuando los datos de entrada tienen un tipo de codificación desconocido. Si este valor se usa para especificar el tipo de codificación de la salida, se usará CAPICOM \_ ENCODE \_ BASE64 en su lugar. Introducido en CAPICOM 2.0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ ENCODE \_ BASE64**</dt> </dl> | Los datos se guardan como una cadena codificada en base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM \_ ENCODE \_ BINARY**</dt> </dl> | Los datos se guardan como una secuencia binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una cadena que contiene los certificados del almacén con el formato de codificación especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tienda**](store.md)
</dt> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> </dl>

 

 
