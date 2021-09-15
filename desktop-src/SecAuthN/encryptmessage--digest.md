---
description: Cifra un mensaje para proporcionar privacidad mediante Digest.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: Función EncryptMessage (Digest) (Sspi.h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13bcaa5b91f165321d03e229416741b90a978dc6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569437"
---
# <a name="encryptmessage-digest-function"></a>Función EncryptMessage (Digest)

La **función EncryptMessage (Digest)** cifra un mensaje para proporcionar [*privacidad.*](../secgloss/p-gly.md) **EncryptMessage (Digest) permite** a la aplicación elegir entre [*algoritmos criptográficos*](../secgloss/c-gly.md) admitidos por el mecanismo elegido. La **función EncryptMessage (Digest)** usa el contexto [*de seguridad*](../secgloss/s-gly.md) al que hace referencia el identificador de contexto. Algunos paquetes no tienen mensajes que cifrar o descifrar, sino que proporcionan un hash de [*integridad*](../secgloss/h-gly.md) que se puede comprobar.

Esta función solo está disponible como mecanismo SASL.

> [!Note]  
> Se puede llamar a **EncryptMessage (Digest)** y [**DecryptMessage (Digest)**](decryptmessage--digest.md) al mismo tiempo desde dos subprocesos diferentes en un único contexto de interfaz de proveedor de compatibilidad de seguridad [](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro está descifrando. Si se cifra más de un subproceso o se descifra más de un subproceso, cada subproceso debe obtener un contexto único.

 

## <a name="syntax"></a>Sintaxis


```C++
SECURITY_STATUS SEC_ENTRY EncryptMessage(
  PCtxtHandle    phContext,
  unsigned long  fQOP,
  PSecBufferDesc pMessage,
  unsigned long  MessageSeqNo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phContext* \[ En\]
</dt> <dd>

Identificador del contexto [*de seguridad que*](../secgloss/s-gly.md) se va a usar para cifrar el mensaje.

</dd> <dt>

*fQOP* \[ En\]
</dt> <dd>

Marcas específicas del paquete que indican la calidad de la protección. Un [*paquete de seguridad*](../secgloss/s-gly.md) puede usar este parámetro para habilitar la selección de [*algoritmos criptográficos*](../secgloss/c-gly.md).

Cuando se usa el SSP de resumen, este parámetro debe establecerse en cero.

</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) En la entrada, la estructura hace referencia a una o varias [**estructuras SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que pueden ser de tipo SECBUFFER \_ DATA. Ese búfer contiene el mensaje que se va a cifrar. El mensaje se cifra en su lugar, sobrescribiendo el contenido original de la estructura .

La función no procesa búferes con el atributo \_ READONLY de SECBUFFER.

La longitud de la estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contiene el mensaje no debe ser mayor que **cbMaximumMessage**, que se obtiene de la función [**QueryContextAttributes (Digest) (SECPKG**](querycontextattributes--digest.md) \_ ATTR \_ STREAM \_ SIZES).

Cuando se usa el SSP de resumen, debe haber un segundo búfer de tipo SECBUFFER PADDING o SEC BUFFER DATA para contener \_ \_ información de \_ [*firma.*](../secgloss/d-gly.md#_security_digital_signature_gly) Para obtener el tamaño del búfer de salida, llame a la función [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) y especifique SECPKG \_ ATTR \_ SIZES. La función devolverá una estructura [**SecPkgContext \_ Sizes.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) El tamaño del búfer de salida es la suma de los valores de los **miembros cbMaxSignature** **y cbBlockSize.**

Las aplicaciones que no usan SSL deben proporcionar [**un SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de tipo SECBUFFER \_ PADDING.

</dd> <dt>

*MessageSeqNo* \[ En\]
</dt> <dd>

Número de secuencia que la aplicación de transporte asignó al mensaje. Si la aplicación de transporte no mantiene números de secuencia, este parámetro debe ser cero.

Cuando se usa el SSP de resumen, este parámetro debe establecerse en cero. El SSP de resumen administra la numeración de secuencia internamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve SEC \_ E \_ OK.

Si se produce un error en la función, devuelve uno de los siguientes códigos de error.



| Código devuelto                                                                                                    | Descripción                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BÚFER \_ E DE SEGUNDO DEMASIADO \_ \_ \_ PEQUEÑO**</dt> </dl>      | El búfer de salida es demasiado pequeño. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                 |
| <dl> <dt>**SEG \_ E \_ CONTEXT \_ EXPIRED**</dt> </dl>        | La aplicación hace referencia a un contexto que ya se ha cerrado. Una aplicación correctamente escrita no debe recibir este error.<br/>                                                                                               |
| <dl> <dt>**SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID**</dt> </dl> | No [*se admite*](../secgloss/c-gly.md) el cifrado elegido para el [*contexto*](../secgloss/s-gly.md) de seguridad.<br/>                                                                                                         |
| <dl> <dt>**S \_ E \_ MEMORIA \_ INSUFICIENTE**</dt> </dl>    | No hay suficiente memoria disponible para completar la acción solicitada.<br/>                                                                                                                                                             |
| <dl> <dt>**SEG \_ E \_ IDENTIFICADOR NO \_ VÁLIDO**</dt> </dl>         | Se especificó un identificador de contexto que no es válido en el *parámetro phContext.*<br/>                                                                                                                                                     |
| <dl> <dt>**SEC \_ E TOKEN NO \_ \_ VÁLIDO**</dt> </dl>          | No se encontró ningún búfer \_ de tipo DE DATOS SECBUFFER.<br/>                                                                                                                                                                                          |
| <dl> <dt>**SEG \_ E \_ QOP \_ NO \_ COMPATIBLE**</dt> </dl>     | El contexto de [*seguridad*](../secgloss/i-gly.md) no admite la confidencialidad ni la [*integridad.*](../secgloss/s-gly.md)<br/> |



 

## <a name="remarks"></a>Observaciones

La **función EncryptMessage (Digest)** cifra un mensaje basado en el mensaje y la clave [*de sesión*](../secgloss/s-gly.md) de un contexto de [*seguridad*](../secgloss/s-gly.md).

Si la aplicación de transporte creó [*el*](../secgloss/s-gly.md) contexto de seguridad para admitir la detección de secuencia y el autor de la llamada proporciona un número de secuencia, la función incluye esta información con el mensaje cifrado. La inclusión de esta información protege contra la reproducción, inserción y supresión de mensajes. El [*paquete de seguridad*](../secgloss/s-gly.md) incorpora el número de secuencia pasado desde la aplicación de transporte.

Cuando use el SSP de resumen, obtenga el tamaño del búfer de salida llamando a la función [**QueryContextAttributes (Digest)**](querycontextattributes--digest.md) y especificando SECPKG \_ ATTR \_ SIZES. La función devolverá una estructura [**SecPkgContext \_ Sizes.**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) El tamaño del búfer de salida es la suma de los valores de los **miembros cbMaxSignature** **y cbBlockSize.**

> [!Note]  
> Estos búferes deben proporcionarse en el orden mostrado.

 



| Tipo de búfer                           | Descripción                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| SECBUFFER \_ STREAM \_ HEADER<br/>  | Utilizado de forma interna. No se requiere inicialización.<br/>                                                                        |
| DATOS DE \_ SECBUFFER<br/>            | Contiene el [*mensaje de texto no*](../secgloss/s-gly.md) cifrado que se va a cifrar.<br/> |
| FINALIZADOR DE \_ SECUENCIAS DE \_ SECBUFFER<br/> | Utilizado de forma interna. No se requiere inicialización.<br/>                                                                        |
| SECBUFFER \_ EMPTY<br/>           | Utilizado de forma interna. No se requiere inicialización. El tamaño puede ser cero.<br/>                                                      |



 

Para obtener un rendimiento óptimo, *las estructuras pMessage* se deben asignar desde la memoria contigua.

**Windows XP:** Esta función también se conocía como **SealMessage.** Las aplicaciones ahora solo **deben usar EncryptMessage (Digest).**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Sspi.h (incluir Security.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Secur32.lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Digest)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**DecryptMessage (digest)**](decryptmessage--digest.md)
</dt> <dt>

[**InitializeSecurityContext (Digest)**](initializesecuritycontext--digest.md)
</dt> <dt>

[**QueryContextAttributes (digest)**](querycontextattributes--digest.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
