---
description: Cifra un mensaje para proporcionar privacidad.
ms.assetid: 2e09f262-9c3e-4db2-9285-017f5e1810c7
title: EncryptMessage (general) (función) (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 3c661f5f529700db19683966783c1aa0793e376b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720322"
---
# <a name="encryptmessage-general-function"></a>EncryptMessage (general), función

La función **EncryptMessage (general)** cifra un mensaje para proporcionar [*privacidad*](../secgloss/p-gly.md). **EncryptMessage (general)** permite que una aplicación Elija entre los [*algoritmos criptográficos*](../secgloss/c-gly.md) admitidos por el mecanismo elegido. La función **EncryptMessage (general)** utiliza el [*contexto de seguridad*](../secgloss/s-gly.md) al que hace referencia el identificador de contexto. Algunos paquetes no tienen mensajes cifrados o descifrados, sino que proporcionan un [*hash*](../secgloss/h-gly.md) de integridad que se puede comprobar.

Al usar el [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) implícita (SSP), esta función solo está disponible como un mecanismo SASL.

Cuando se usa Schannel SSP, esta función cifra los mensajes mediante una [*clave de sesión*](../secgloss/s-gly.md) negociada con la parte remota que recibirá el mensaje. El algoritmo de cifrado viene determinado por el conjunto de [ [*cifrado*](../secgloss/c-gly.md)]([*cipher*](../secgloss/c-gly.md)-suites-in-schannel.md) en uso.

> [!Note]  
> Se puede llamar a **EncryptMessage (general)** y [**DecryptMessage (general)**](decryptmessage--general.md) al mismo tiempo desde dos subprocesos diferentes en un único contexto de la [*interfaz del proveedor de compatibilidad con seguridad*](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro está descifrando. Si se está cifrando más de un subproceso o se está descifrando más de un subproceso, cada subproceso debe obtener un contexto único.

Para obtener información sobre el uso de esta función con un SSP específico, vea los temas siguientes.

| Tema                                                            | Descripción                                               |
|------------------------------------------------------------------|-----------------------------------------------------------|
| [**EncryptMessage (Resumen)**](encryptmessage--digest.md)       | Cifra un mensaje para ofrecer privacidad mediante síntesis.    |
| [**EncryptMessage (Kerberos)**](encryptmessage--kerberos.md)   | Cifra un mensaje para ofrecer privacidad mediante Kerberos.  |
| [**EncryptMessage (Negotiate)**](encryptmessage--negotiate.md) | Cifra un mensaje para ofrecer privacidad mediante Negotiate. |
| [**EncryptMessage (NTLM)**](encryptmessage--ntlm.md)           | Cifra un mensaje para ofrecer privacidad mediante NTLM.      |
| [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)   | Cifra un mensaje para ofrecer privacidad mediante Schannel.  |

## <a name="syntax"></a>Sintaxis

```C++
SECURITY_STATUS SEC_Entry EncryptMessage(
  _In_    PCtxtHandle    phContext,
  _In_    ULONG          fQOP,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo
);
```
## <a name="parameters"></a>Parámetros

*phContext* \[ de\]

Identificador del contexto de [*seguridad*](../secgloss/s-gly.md) que se va a utilizar para cifrar el mensaje.

*fQOP* \[ de\]

Marcas específicas del paquete que indican la calidad de la protección. Un [*paquete de seguridad*](../secgloss/s-gly.md) puede usar este parámetro para habilitar la selección de [*algoritmos criptográficos*](../secgloss/c-gly.md).

Al usar el SSP de síntesis, este parámetro debe establecerse en cero.

Este parámetro puede ser una de las marcas siguientes.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Value</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Producir un encabezado o un finalizador, pero no cifrar el mensaje.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.</blockquote><br/></td></tr><tr class="even"><td><span id="SECQOP_WRAP_OOB_DATA"></span><span id="secqop_wrap_oob_data"></span><dl> <dt><strong>SECQOP_WRAP_OOB_DATA</strong></dt> </dl></td><td>Envíe un mensaje de alerta de Schannel. En este caso, el parámetro <em>pMessage</em> debe contener un código de evento SSL/TLS estándar de dos bytes. Este valor solo es compatible con el SSP de Schannel.<br/></td></tr></tbody></table>

*pMessage* \[ in, out\]

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Uno de ellos puede ser de tipo SECBUFFER \_ Data. Ese búfer contiene el mensaje que se va a cifrar. El mensaje está cifrado en su lugar, sobrescribiendo el contenido original de la estructura.

La función no procesa los búferes con el \_ atributo SECBUFFER ReadOnly.

La longitud de la estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contiene el mensaje no debe ser mayor que **cbMaximumMessage**, que se obtiene a partir de la función [**QueryContextAttributes (general)**](querycontextattributes--general.md) ( \_ tamaños de flujo SECPKG ATTR \_ \_ ).

Al usar el SSP de síntesis, debe haber un segundo búfer de tipo SECBUFFER \_ padding o sec \_ \_ Data buffer para almacenar la información de la [*firma*](../secgloss/d-gly.md#_security_digital_signature_gly) . Para obtener el tamaño del búfer de salida, llame a la función [**QueryContextAttributes (general)**](querycontextattributes--general.md) y especifique los tamaños de SECPKG \_ ATTR \_ . La función devolverá una estructura de [**\_ tamaños de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . El tamaño del búfer de salida es la suma de los valores de los miembros **cbMaxSignature** y **cbBlockSize** .

Las aplicaciones que no usan SSL deben proporcionar un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de tipo SecBuffer \_ padding.

*MessageSeqNo* \[ de\]

Número de secuencia que la aplicación de transporte asignó al mensaje. Si la aplicación de transporte no mantiene los números de secuencia, este parámetro debe ser cero.

Al usar el SSP de síntesis, este parámetro debe establecerse en cero. El SSP de síntesis administra la numeración de secuencias internamente.

Cuando se usa Schannel SSP, este parámetro debe establecerse en cero. Schannel SSP no utiliza números de secuencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.

Si se produce un error en la función, devuelve uno de los siguientes códigos de error.

| Código devuelto                         | Descripción                                                                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **búfer de s \_ E s \_ \_ demasiado \_ pequeño**      | El búfer de salida es demasiado pequeño. Para obtener más información, vea la sección Comentarios.                                                                                                          |
| **SEC \_ E \_ contexto \_ expirado**        | La aplicación hace referencia a un contexto que ya se ha cerrado. Una aplicación escrita correctamente no debe recibir este error.                                        |
| **s \_ E \_ \_ sistema criptográfico \_ no válido** | No se admite el [*cifrado*](../secgloss/c-gly.md) elegido para el [*contexto de seguridad*](../secgloss/s-gly.md) .                                                                       |
| **s \_ E \_ memoria insuficiente \_**    | No hay suficiente memoria disponible para completar la acción solicitada.                                                                                                      |
| **s \_ E \_ identificador no válido \_**         | Se especificó un identificador de contexto que no es válido en el parámetro *phContext* .                                                                                              |
| **s \_ E \_ token no válido \_**          | No \_ se encontró ningún búfer de tipo de datos SECBUFFER.                                                                                                                                   |
| **s \_ E \_ QOP \_ no \_ admitidos**     | La confidencialidad o la [*integridad*](../secgloss/i-gly.md) no son compatibles con el [*contexto de seguridad*](../secgloss/s-gly.md). |

## <a name="remarks"></a>Observaciones

La función **EncryptMessage (general)** cifra un mensaje basado en el mensaje y la [*clave de sesión*](../secgloss/s-gly.md) de un [*contexto de seguridad*](../secgloss/s-gly.md).

Si la aplicación de transporte creó el [*contexto de seguridad*](../secgloss/s-gly.md) para admitir la detección de secuencias y el autor de la llamada proporciona un número de secuencia, la función incluye esta información con el mensaje cifrado. La inclusión de esta información protege contra la reproducción, inserción y supresión de mensajes. El [*paquete de seguridad*](../secgloss/s-gly.md) incorpora el número de secuencia que se pasa desde la aplicación de transporte.

Cuando use el SSP de síntesis, obtenga el tamaño del búfer de salida mediante una llamada a la función [**QueryContextAttributes (general)**](querycontextattributes--general.md) y especifique los tamaños de SECPKG \_ ATTR \_ . La función devolverá una estructura de [**\_ tamaños de SecPkgContext**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_sizes) . El tamaño del búfer de salida es la suma de los valores de los miembros **cbMaxSignature** y **cbBlockSize** .

Cuando se usa con el SSP de Schannel, el parámetro *pMessage* debe contener una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) con los siguientes búferes.

> [!Note]  
> Estos búferes se deben proporcionar en el orden mostrado.

| Tipo de búfer                | Descripción                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| SECBUFFER \_ encabezado de secuencia \_  | Utilizado de forma interna. No se requiere inicialización.                                                |
| datos de SECBUFFER \_            | Contiene el mensaje de [*texto simple*](../secgloss/s-gly.md) que se va a cifrar. |
| \_finalizador de flujo SECBUFFER \_ | Utilizado de forma interna. No se requiere inicialización.                                                |
| SECBUFFER \_ vacío           | Utilizado de forma interna. No se requiere inicialización. El tamaño puede ser cero.                              |

Cuando use el SSP de Schannel, determine el tamaño máximo de cada uno de los búferes mediante una llamada a la función [**QueryContextAttributes (general)**](querycontextattributes--general.md) y especifique el \_ atributo SECPKG ATTR \_ Stream \_ sizes. Esta función devuelve una [**estructura SecPkgContext \_ StreamSizes**](/windows/win32/api/sspi/ns-sspi-secpkgcontext_streamsizes) cuyos miembros contienen los tamaños máximos para los búferes de encabezado (miembro **cbHeader** ), mensaje (miembro **cbMaximumMessage** ) y finalizador (miembro **cbTrailer** ).

Para un rendimiento óptimo, las estructuras *pMessage* se deben asignar desde la memoria contigua.

**Windows XP/2000:** Esta función también se conocía como **SealMessage**. Las aplicaciones ahora deben usar **EncryptMessage (general)** solamente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows XP \[\]                                                            |
| Servidor mínimo compatible | Solo aplicaciones de escritorio de Windows Server 2003 \[\]                                                   |
| Encabezado                   | <dl> <dt>SSPI. h (incluir Security. h)</dt> </dl> |
| Biblioteca                  | <dl> <dt>SECUR32. lib</dt> </dl>                 |
| Archivo DLL                      | <dl> <dt>Secur32.dll</dt> </dl>                 |

## <a name="see-also"></a>Vea también

- [Funciones SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (general)**](acceptsecuritycontext--general.md)
- [**DecryptMessage (general)**](decryptmessage--general.md)
- [**InitializeSecurityContext (general)**](initializesecuritycontext--general.md)
- [**QueryContextAttributes (general)**](querycontextattributes--general.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
