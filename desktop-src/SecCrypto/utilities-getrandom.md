---
description: Genera un número aleatorio seguro mediante el proveedor de servicios criptográficos (CSP) predeterminado.
ms.assetid: 52c49f73-58b8-455f-9368-54f38de55776
title: Utilities. GetRandom (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.GetRandom
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b7e02c7df61c1a2d710189fb2e5e0a21cc0b504
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690371"
---
# <a name="utilitiesgetrandom-method"></a>Utilities. GetRandom (método)

\[El método **GetRandom** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.\]

El método **GetRandom** genera un número aleatorio seguro mediante el [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) predeterminado.

## <a name="syntax"></a>Sintaxis


```VB
Utilities.GetRandom( _
  [ ByVal Length ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Longitud* \[ en, opcional\]
</dt> <dd>

Longitud, en bytes, del número aleatorio que se va a crear. El valor predeterminado es 8 bytes.

</dd> <dt>

*EncodingType* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de [**\_ \_ tipo de codificación CAPICOM**](capicom-encoding-type.md) que indica el tipo de codificación que se va a utilizar para el número aleatorio generado. El valor predeterminado es el \_ binario codificado de CAPICOM \_ . Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ codificar \_ any**</dt> </dl>          | Este tipo de codificación solo se utiliza cuando los datos de entrada tienen un tipo de codificación desconocido. Si este valor se usa para especificar el tipo de codificación de la salida, \_ se usará CAPICOM encode \_ Base64 en su lugar. Introducido en CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM, codificación \_ \_ Base64**</dt> </dl> | Los datos se guardan como una cadena codificada en Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_código binario de codificación de CAPICOM \_**</dt> </dl> | Los datos se guardan como una secuencia binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una *longitud* de número de bytes generada aleatoriamente, con la codificación especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Sectores públicos**](utilities.md)
</dt> </dl>

 

 
