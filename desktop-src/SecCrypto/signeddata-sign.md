---
description: Crea una firma digital en el contenido que se va a firmar. Una firma digital consta de un hash del contenido que se va a firmar que se cifra mediante la clave privada del firmante.
ms.assetid: ee98a36c-f9a9-4247-ae48-7b1a10b92be4
title: Método SignedData.Sign
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
ms.openlocfilehash: 6ead7fb1c96b05d6945bb67937b215fd6d5d2422041250bee18e4be26edb2f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118899023"
---
# <a name="signeddatasign-method"></a>Método SignedData.Sign

\[El **método Sign** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **método Sign** crea una firma [*digital*](../secgloss/d-gly.md) en el contenido que se va a firmar. Una firma digital consta de un [*hash*](../secgloss/h-gly.md) del contenido que se va a firmar que se cifra mediante la clave privada del firmante. Este método solo se puede usar después de inicializar la propiedad [**SignedData.Content.**](signeddata-content.md) Si se llama al método **Sign** en un objeto que ya tiene una firma, se reemplaza la firma anterior. La firma se crea mediante el algoritmo de firma SHA1.

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

*Firmante* \[ in, opcional\]
</dt> <dd>

Referencia al objeto [**Signer**](signer.md) del firmante de los datos. El **objeto Signer** debe tener acceso a la [*clave privada*](../secgloss/p-gly.md) del certificado [*usado*](../secgloss/c-gly.md) para firmar. Este parámetro puede ser **NULL**; Para obtener más información, vea Comentarios.

</dd> <dt>

*bDetached* \[ in, opcional\]
</dt> <dd>

Si **es True**, se desasocian los datos que se firmarán; Es decir, el contenido firmado no se incluye como parte del objeto firmado. Para comprobar la firma en el contenido desasociado, una aplicación debe tener una copia del contenido original. El contenido desasociado se suele usar para reducir el tamaño de un objeto firmado que se va a enviar a través de la web, si el destinatario del mensaje firmado tiene una copia original de los datos firmados. El valor predeterminado es **False**.

</dd> <dt>

*EncodingType* \[ in, opcional\]
</dt> <dd>

Valor de la enumeración [CAPICOM \_ ENCODING \_ TYPE](capicom-encoding-type.md) que indica cómo se codificarán los datos firmados. El valor predeterminado es CAPICOM \_ ENCODE \_ BASE64. Este parámetro puede ser uno de los valores siguientes.



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
> Cuando se llama a este método desde un script web, el script debe usar la clave privada para crear una firma digital. Permitir que sitios web que no son de confianza usen su clave privada es un riesgo para la seguridad. Aparece un cuadro de diálogo que pregunta si el sitio web puede usar la clave privada cuando se llama por primera vez a este método. Si permite que el script use la clave privada para crear una firma digital y selecciona "No volver a mostrar este cuadro de diálogo", el cuadro de diálogo ya no aparecerá para ningún script dentro de ese dominio que use la clave privada para crear una firma digital. Sin embargo, los scripts fuera de ese dominio que intenten usar la clave privada para crear una firma digital seguirán haciendo que aparezca este cuadro de diálogo. Si no permite que el script use la clave privada y selecciona "No volver a mostrar este cuadro de diálogo", se rechazará automáticamente la capacidad de usar la clave privada para crear firmas digitales.

 

Dado que la creación de una firma [*digital*](../secgloss/d-gly.md) requiere el uso de una clave [*privada,*](../secgloss/p-gly.md)las aplicaciones basadas en web que intenten usar este método requerirán mensajes de interfaz de usuario que permitan al usuario aprobar el uso de la clave privada, por motivos de seguridad.

Los resultados siguientes se aplican al valor del parámetro *Signer:*

-   Si el *parámetro Signer* no es **NULL,** este método usa la clave privada a la que apunta el certificado asociado para cifrar la firma. Si la clave privada a la que apunta el certificado no está disponible, se produce un error en el método.
-   Si el *parámetro Signer* es **NULL** y hay exactamente un certificado en el almacén CURRENT USER MY que tiene acceso a una clave privada, ese certificado se usa para crear \_ la firma.
-   Si el *parámetro Signer* es **NULL**, [**Configuración. El**](settings-enablepromptforcertificateui.md) valor de la propiedad EnablePromptForCertificateUI es true y hay más de un certificado en el almacén MY DEL USUARIO ACTUAL con una clave privada disponible. Aparece un cuadro de diálogo que permite al usuario seleccionar qué certificado se \_ usa.
-   Si el *parámetro Signer* es **NULL** y el [**Configuración. La propiedad EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) es false y se produce un error en el método.
-   Si el *parámetro Signer* es **NULL** y no hay ningún certificado en el almacén CURRENT USER MY con una clave privada disponible, se produce \_ un error en el método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
