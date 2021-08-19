---
description: Crea una firma digital en el contenido firmado previamente.
ms.assetid: c0a3de75-afba-45ba-b701-2729f4495eda
title: Método SignedData.CoSign
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.CoSign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ed4feb55420ebf9d3bc43496fe3004a4d1b55e1ae8add4e3d5b40ec2ac4ba4ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973895"
---
# <a name="signeddatacosign-method"></a>Método SignedData.CoSign

\[El **método CoSign** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **método CoSign** crea una [*firma digital en*](../secgloss/d-gly.md) el contenido firmado previamente.

## <a name="syntax"></a>Sintaxis


```VB
SignedData.CoSign( _
  [ ByVal Signer ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Firmante* \[ in, opcional\]
</dt> <dd>

Referencia al objeto [**Signer**](signer.md) del firmante de los datos. El **objeto Signer** debe tener acceso a la clave privada del certificado usado para firmar. Este parámetro puede ser **NULL**; Para obtener más información, vea Comentarios.

</dd> <dt>

*EncodingType* \[ in, opcional\]
</dt> <dd>

Valor de la enumeración [**CAPICOM \_ ENCODING \_ TYPE**](capicom-encoding-type.md) que indica cómo se codificarán los datos firmados. El valor predeterminado es CAPICOM \_ ENCODE \_ BASE64. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ ENCODE \_ ANY**</dt> </dl>          | Este tipo de codificación solo se usa cuando los datos de entrada tienen un tipo de codificación desconocido. Si este valor se usa para especificar el tipo de codificación de la salida, se usará CAPICOM \_ ENCODE \_ BASE64 en su lugar. Introducido en CAPICOM 2.0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ ENCODE \_ BASE64**</dt> </dl> | Los datos se guardan como una cadena codificada en base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**CAPICOM \_ ENCODE \_ BINARY**</dt> </dl> | Los datos se guardan como una secuencia binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una cadena que contiene los datos codificados y firmados.

Si se produce un error en este método, se producirá un error. El **objeto Err** contendrá información adicional sobre el error.

## <a name="remarks"></a>Comentarios

> [!IMPORTANT]
> Cuando se llama a este método desde un script web, el script debe usar la [*clave privada*](../secgloss/p-gly.md) para crear una firma digital. Permitir que sitios web que no son de confianza usen su clave privada es un riesgo para la seguridad. Aparece un cuadro de diálogo que pregunta si el sitio web puede usar la clave privada cuando se llama por primera vez a este método. Si permite que el script use la clave privada para crear una firma digital y selecciona "No volver a mostrar este cuadro de diálogo", el cuadro de diálogo ya no aparecerá para ningún script dentro de ese dominio que use la clave privada para crear una firma digital. Sin embargo, los scripts fuera de ese dominio que intenten usar la clave privada para crear una firma digital seguirán haciendo que aparezca este cuadro de diálogo. Si no permite que el script use la clave privada y selecciona "No volver a mostrar este cuadro de diálogo", se rechazará automáticamente la capacidad de usar la clave privada para crear firmas digitales.

 

No se garantiza que los cosignadores estén en un orden determinado.

Los resultados siguientes se aplican al valor del parámetro *Signer:*

-   Si el *parámetro Signer* no es **NULL,** este método usa la clave privada a la que apunta el certificado asociado para cifrar la cofirma. Si la clave privada a la que apunta el certificado no está disponible, se produce un error en el método.
-   Si el *parámetro Signer* es **NULL** y hay exactamente un certificado en el almacén CURRENT USER MY que tiene acceso a una clave privada, ese certificado se usa para crear la \_ cofirma.
-   Si el *parámetro Signer* es **NULL**, [**Configuración. El**](settings-enablepromptforcertificateui.md) valor de la propiedad EnablePromptForCertificateUI es true y hay más de un certificado en el almacén MY DEL USUARIO ACTUAL con una clave privada disponible. Aparece un cuadro de diálogo que permite al usuario seleccionar qué certificado se \_ usa.
-   Si el *parámetro Signer* es **NULL** y el [**Configuración. La propiedad EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) es false y se produce un error en el método.
-   Si el *parámetro Signer* es **NULL** y no hay ningún certificado en el almacén CURRENT USER MY con una clave privada disponible, se produce \_ un error en el método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
