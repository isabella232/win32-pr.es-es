---
description: Crea una firma digital en el contenido que se va a firmar. Una firma digital consta de un hash del contenido que se va a firmar y que se cifra mediante la clave privada del firmante.
ms.assetid: ee98a36c-f9a9-4247-ae48-7b1a10b92be4
title: SignedData. Sign (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9f885bb110b51264bc6108ca8c0f881cc48f7710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690059"
---
# <a name="signeddatasign-method"></a>SignedData. Sign (método)

\[El método **Sign** está disponible para su uso en los sistemas operativos especificados en la sección requirements. En su lugar, use la [**clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El método **Sign** crea una [*firma digital*](../secgloss/d-gly.md) en el contenido que se va a firmar. Una firma digital consta de un [*hash*](../secgloss/h-gly.md) del contenido que se va a firmar y que se cifra mediante la clave privada del firmante. Este método solo se puede usar después de que se haya inicializado la propiedad [**SignedData. Content**](signeddata-content.md) . Si se llama al método **Sign** en un objeto que ya tiene una firma, se reemplaza la firma anterior. La firma se crea mediante el algoritmo de firma de SHA1.

## <a name="syntax"></a>Sintaxis


```VB
SignedData.Sign( _
  [ ByVal Signer ], _
  [ ByVal bDetached ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Firmante* \[ en, opcional\]
</dt> <dd>

Referencia al objeto [**firmante**](signer.md) del firmante de los datos. El objeto de **firmante** debe tener acceso a la [*clave privada*](../secgloss/p-gly.md) del [*certificado*](../secgloss/c-gly.md) usado para firmar. Este parámetro puede ser **null**; para obtener más información, vea la sección Comentarios.

</dd> <dt>

*bDetached* \[ en, opcional\]
</dt> <dd>

Si es **true**, se desasocian los datos que se van a firmar; es decir, el contenido que está firmado no se incluye como parte del objeto firmado. Para comprobar la firma en el contenido separado, una aplicación debe tener una copia del contenido original. El contenido separado se usa a menudo para reducir el tamaño de un objeto firmado que se va a enviar a través de la web, si el destinatario del mensaje firmado tiene una copia original de los datos firmados. El valor predeterminado es **False**.

</dd> <dt>

*EncodingType* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de [ \_ \_ tipo de codificación CAPICOM](capicom-encoding-type.md) que indica cómo se van a codificar los datos firmados. El valor predeterminado es CAPICOM \_ encode \_ Base64. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ codificar \_ any**</dt> </dl>          | Este tipo de codificación solo se utiliza cuando los datos de entrada tienen un tipo de codificación desconocido. Si este valor se usa para especificar el tipo de codificación de la salida, \_ se usará CAPICOM encode \_ Base64 en su lugar. Introducido en CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM, codificación \_ \_ Base64**</dt> </dl> | Los datos se guardan como una cadena codificada en Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_código binario de codificación de CAPICOM \_**</dt> </dl> | Los datos se guardan como una secuencia binaria pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una cadena que contiene los datos firmados y codificados.

Si se produce un error en este método, se producirá un error. El objeto **Err** contendrá información adicional sobre el error.

## <a name="remarks"></a>Observaciones

> [!IMPORTANT]
> Cuando se llama a este método desde un script Web, el script debe usar la clave privada para crear una firma digital. Permitir a los sitios web que no son de confianza usar su clave privada es un riesgo para la seguridad. Un cuadro de diálogo que pregunta si el sitio web puede usar su clave privada aparece cuando se llama por primera vez a este método. Si permite que el script use su clave privada para crear una firma digital y selecciona "no volver a mostrar este cuadro de diálogo", el cuadro de diálogo ya no aparecerá en ningún script del dominio que use la clave privada para crear una firma digital. Sin embargo, los scripts que se encuentran fuera de ese dominio y que intentan usar la clave privada para crear una firma digital seguirán provocando que aparezca este cuadro de diálogo. Si no permite que el script use su clave privada y selecciona "no volver a mostrar este cuadro de diálogo", se rechazará automáticamente la capacidad de usar la clave privada para crear firmas digitales en los scripts de ese dominio.

 

Dado que la creación de una [*firma digital*](../secgloss/d-gly.md) requiere el uso de una [*clave privada*](../secgloss/p-gly.md), las aplicaciones basadas en Web que intenten usar este método requerirán mensajes de interfaz de usuario que permitan al usuario aprobar el uso de la clave privada por motivos de seguridad.

Los resultados siguientes se aplican al valor del parámetro *Signer* :

-   Si el parámetro del *firmante* no es **null**, este método utiliza la clave privada a la que apunta el certificado asociado para cifrar la firma. Si no está disponible la clave privada a la que apunta el certificado, se produce un error en el método.
-   Si el parámetro de *firmante* es **null** y hay exactamente un certificado en el usuario actual \_ mi almacén que tiene acceso a una clave privada, ese certificado se usa para crear la firma.
-   Si el parámetro de *firmante* es **null**, el valor de la propiedad [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) es true y hay más de un certificado en el \_ usuario actual My Store con una clave privada disponible, aparece un cuadro de diálogo que permite al usuario seleccionar qué certificado se usa.
-   Si el parámetro de *firmante* es **null** y la propiedad [**Settings. EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) es false, se produce un error en el método.
-   Si el parámetro de *firmante* es **null** y no hay ningún certificado en el \_ usuario actual My Store con una clave privada disponible, se produce un error en el método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
