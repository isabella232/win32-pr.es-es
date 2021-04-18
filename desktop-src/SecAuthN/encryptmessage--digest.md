---
description: Cifra un mensaje para ofrecer privacidad mediante síntesis.
ms.assetid: 0045e931-929b-40c4-a524-5664d2fc5170
title: Función EncryptMessage (digest) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 13bcaa5b91f165321d03e229416741b90a978dc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720323"
---
# <a name="encryptmessage-digest-function"></a>EncryptMessage (síntesis) (función)

La función **EncryptMessage (síntesis)** cifra un mensaje para proporcionar [*privacidad*](../secgloss/p-gly.md). **EncryptMessage (síntesis)** permite que la aplicación Elija entre los [*algoritmos criptográficos*](../secgloss/c-gly.md) admitidos por el mecanismo elegido. La función **EncryptMessage (síntesis)** utiliza el [*contexto de seguridad*](../secgloss/s-gly.md) al que hace referencia el identificador de contexto. Algunos paquetes no tienen mensajes cifrados o descifrados, sino que proporcionan un [*hash*](../secgloss/h-gly.md) de integridad que se puede comprobar.

Esta función solo está disponible como un mecanismo SASL.

> [!Note]  
> Se puede llamar a **EncryptMessage (digest)** y [**DecryptMessage (digest)**](decryptmessage--digest.md) al mismo tiempo desde dos subprocesos diferentes en un único contexto de la [*interfaz del proveedor de compatibilidad con seguridad*](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro está descifrando. Si se está cifrando más de un subproceso o se está descifrando más de un subproceso, cada subproceso debe obtener un contexto único.

 

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

*phContext* \[ de\]
</dt> <dd>

Identificador del contexto de [*seguridad*](../secgloss/s-gly.md) que se va a utilizar para cifrar el mensaje.

</dd> <dt>

*fQOP* \[ de\]
</dt> <dd>

Marcas específicas del paquete que indican la calidad de la protección. Un [*paquete de seguridad*](../secgloss/s-gly.md) puede usar este parámetro para habilitar la selección de [*algoritmos criptográficos*](../secgloss/c-gly.md).

Al usar el SSP de síntesis, este parámetro debe establecerse en cero.

</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que pueden ser de tipo SecBuffer \_ Data. Ese búfer contiene el mensaje que se va a cifrar. El mensaje está cifrado en su lugar, sobrescribiendo el contenido original de la estructura.

La función no procesa los búferes con el \_ atributo SECBUFFER ReadOnly.

La longitud de la estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contiene el mensaje no debe ser mayor que **cbMaximumMessage**, que se obtiene a partir de la función [**QueryContextAttributes (digest)**](querycontextattributes--digest.md) ( \_ tamaños de flujo SECPKG ATTR \_ \_ ).

Al usar el SSP de síntesis, debe haber un segundo búfer de tipo SECBUFFER \_ padding o sec \_ \_ Data buffer para almacenar la información de la [*firma*](../secgloss/d-gly.md#_security_digital_signature_gly) . Para obtener el tamaño del búfer de salida, llame a la función [**QueryContextAttributes (digest)**](querycontextattributes--digest.md) y especifique los tamaños de SECPKG \_ ATTR \_ . La función devolverá una estructura de [**\_ tamaños de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . El tamaño del búfer de salida es la suma de los valores de los miembros **cbMaxSignature** y **cbBlockSize** .

Las aplicaciones que no usan SSL deben proporcionar un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de tipo SecBuffer \_ padding.

</dd> <dt>

*MessageSeqNo* \[ de\]
</dt> <dd>

Número de secuencia que la aplicación de transporte asignó al mensaje. Si la aplicación de transporte no mantiene los números de secuencia, este parámetro debe ser cero.

Al usar el SSP de síntesis, este parámetro debe establecerse en cero. El SSP de síntesis administra la numeración de secuencias internamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.

Si se produce un error en la función, devuelve uno de los siguientes códigos de error.



| Código devuelto                                                                                                    | Descripción                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**búfer de s \_ E s \_ \_ demasiado \_ pequeño**</dt> </dl>      | El búfer de salida es demasiado pequeño. Para obtener más información, vea la sección Comentarios.<br/>                                                                                                                                                                 |
| <dl> <dt>**SEC \_ E \_ contexto \_ expirado**</dt> </dl>        | La aplicación hace referencia a un contexto que ya se ha cerrado. Una aplicación escrita correctamente no debe recibir este error.<br/>                                                                                               |
| <dl> <dt>**s \_ E \_ \_ sistema criptográfico \_ no válido**</dt> </dl> | No se admite el [*cifrado*](../secgloss/c-gly.md) elegido para el [*contexto de seguridad*](../secgloss/s-gly.md) .<br/>                                                                                                         |
| <dl> <dt>**s \_ E \_ memoria insuficiente \_**</dt> </dl>    | No hay suficiente memoria disponible para completar la acción solicitada.<br/>                                                                                                                                                             |
| <dl> <dt>**s \_ E \_ identificador no válido \_**</dt> </dl>         | Se especificó un identificador de contexto que no es válido en el parámetro *phContext* .<br/>                                                                                                                                                     |
| <dl> <dt>**s \_ E \_ token no válido \_**</dt> </dl>          | No \_ se encontró ningún búfer de tipo de datos SECBUFFER.<br/>                                                                                                                                                                                          |
| <dl> <dt>**s \_ E \_ QOP \_ no \_ admitidos**</dt> </dl>     | La confidencialidad o la [*integridad*](../secgloss/i-gly.md) no son compatibles con el [*contexto de seguridad*](../secgloss/s-gly.md).<br/> |



 

## <a name="remarks"></a>Observaciones

La función **EncryptMessage (síntesis)** cifra un mensaje basado en el mensaje y la [*clave de sesión*](../secgloss/s-gly.md) de un [*contexto de seguridad*](../secgloss/s-gly.md).

Si la aplicación de transporte creó el [*contexto de seguridad*](../secgloss/s-gly.md) para admitir la detección de secuencias y el autor de la llamada proporciona un número de secuencia, la función incluye esta información con el mensaje cifrado. La inclusión de esta información protege contra la reproducción, inserción y supresión de mensajes. El [*paquete de seguridad*](../secgloss/s-gly.md) incorpora el número de secuencia que se pasa desde la aplicación de transporte.

Cuando use el SSP de síntesis, obtenga el tamaño del búfer de salida mediante una llamada a la función [**QueryContextAttributes (digest)**](querycontextattributes--digest.md) y especifique los tamaños de SECPKG \_ ATTR \_ . La función devolverá una estructura de [**\_ tamaños de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . El tamaño del búfer de salida es la suma de los valores de los miembros **cbMaxSignature** y **cbBlockSize** .

> [!Note]  
> Estos búferes se deben proporcionar en el orden mostrado.

 



| Tipo de búfer                           | Descripción                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| SECBUFFER \_ encabezado de secuencia \_<br/>  | Utilizado de forma interna. No se requiere inicialización.<br/>                                                                        |
| datos de SECBUFFER \_<br/>            | Contiene el mensaje de [*texto simple*](../secgloss/s-gly.md) que se va a cifrar.<br/> |
| \_finalizador de flujo SECBUFFER \_<br/> | Utilizado de forma interna. No se requiere inicialización.<br/>                                                                        |
| SECBUFFER \_ vacío<br/>           | Utilizado de forma interna. No se requiere inicialización. El tamaño puede ser cero.<br/>                                                      |



 

Para un rendimiento óptimo, las estructuras *pMessage* se deben asignar desde la memoria contigua.

**Windows XP:** Esta función también se conocía como **SealMessage**. Las aplicaciones ahora deben usar **EncryptMessage (digest)** solamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>SECUR32. lib</dt> </dl>                 |
| Archivo DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Resumen)**](acceptsecuritycontext--digest.md)
</dt> <dt>

[**DecryptMessage (Resumen)**](decryptmessage--digest.md)
</dt> <dt>

[**InitializeSecurityContext (Resumen)**](initializesecuritycontext--digest.md)
</dt> <dt>

[**QueryContextAttributes (Resumen)**](querycontextattributes--digest.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
