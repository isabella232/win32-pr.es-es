---
description: Cifra un mensaje para proporcionar privacidad mediante Kerberos.
ms.assetid: b9b6ca95-b986-4de7-bd28-994a5125ad05
title: Función EncryptMessage (Kerberos)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 89c6504fe8518e1c43d155ebce638dec1acfeb80
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575400"
---
# <a name="encryptmessage-kerberos-function"></a>Función EncryptMessage (Kerberos)

La **función EncryptMessage (Kerberos)** cifra un mensaje para proporcionar [*privacidad.*](../secgloss/p-gly.md) **EncryptMessage (Kerberos) permite** que una aplicación elija entre los [*algoritmos criptográficos*](../secgloss/c-gly.md) admitidos por el mecanismo elegido. La **función EncryptMessage (Kerberos)** usa el contexto [*de seguridad*](../secgloss/s-gly.md) al que hace referencia el identificador de contexto. Algunos paquetes no tienen mensajes que cifrar o descifrar, sino que proporcionan un hash de [*integridad*](../secgloss/h-gly.md) que se puede comprobar.

> [!Note]  
> Se puede llamar a **EncryptMessage (Kerberos)** y [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md) al mismo tiempo desde dos subprocesos diferentes en un único contexto de interfaz de proveedor de compatibilidad de seguridad [](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro se está descifrando. Si se cifra más de un subproceso o se descifra más de un subproceso, cada subproceso debe obtener un contexto único.

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

<dl> <dt>

*phContext* \[ En\]
</dt> <dd>

Identificador del contexto [*de seguridad que*](../secgloss/s-gly.md) se va a usar para cifrar el mensaje.

</dd> <dt>

*fQOP* \[ En\]
</dt> <dd>

Marcas específicas del paquete que indican la calidad de la protección. Un [*paquete de seguridad*](../secgloss/s-gly.md) puede usar este parámetro para habilitar la selección de [*algoritmos criptográficos*](../secgloss/c-gly.md).

Este parámetro puede ser la marca siguiente.


| Value | Significado | 
|-------|---------|
| <span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl><dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt></dl> | Generar un encabezado o finalizador, pero no cifrar el mensaje.<br /><blockquote>[!Note]<br />KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.</blockquote><br /> | 


</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Puntero a una [**estructura SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) En la entrada, la estructura hace referencia a una o varias [**estructuras SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que pueden ser de tipo SECBUFFER \_ DATA. Ese búfer contiene el mensaje que se va a cifrar. El mensaje se cifra en su lugar, sobrescribiendo el contenido original de la estructura .

La función no procesa búferes con el atributo \_ READONLY de SECBUFFER.

La longitud de la estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contiene el mensaje no debe ser mayor que **cbMaximumMessage**, que se obtiene de la función [**QueryContextAttributes (Kerberos) (SECPKG**](querycontextattributes--kerberos.md) \_ ATTR \_ STREAM \_ SIZES).

Las aplicaciones que no usan SSL deben proporcionar [**un SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de tipo SECBUFFER \_ PADDING.

</dd> <dt>

*MessageSeqNo* \[ En\]
</dt> <dd>

Número de secuencia que la aplicación de transporte asignó al mensaje. Si la aplicación de transporte no mantiene números de secuencia, este parámetro debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve SEC \_ E \_ OK.

Si se produce un error en la función, devuelve uno de los siguientes códigos de error.

| Código devuelto                                                                                                    | Descripción                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BÚFER \_ E DE SEGUNDO DEMASIADO \_ \_ \_ PEQUEÑO**</dt> </dl>      | El búfer de salida es demasiado pequeño. Para obtener más información, vea la sección Comentarios.                                                                                                                                                                 |
| <dl> <dt>**SEG \_ E \_ CONTEXT \_ EXPIRED**</dt> </dl>        | La aplicación hace referencia a un contexto que ya se ha cerrado. Una aplicación correctamente escrita no debe recibir este error.                                                                                               |
| <dl> <dt>**SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID**</dt> </dl> | No [*se admite*](../secgloss/c-gly.md) el cifrado elegido para el [*contexto*](../secgloss/s-gly.md) de seguridad.                                                                                                         |
| <dl> <dt>**S \_ E \_ MEMORIA \_ INSUFICIENTE**</dt> </dl>    | No hay suficiente memoria disponible para completar la acción solicitada.                                                                                                                                                             |
| <dl> <dt>**SEG \_ E \_ IDENTIFICADOR NO \_ VÁLIDO**</dt> </dl>         | Se especificó un identificador de contexto que no es válido en el *parámetro phContext.*                                                                                                                                                     |
| <dl> <dt>**SEC \_ E TOKEN NO \_ \_ VÁLIDO**</dt> </dl>          | No se encontró ningún búfer \_ de tipo DE DATOS SECBUFFER.                                                                                                                                                                                          |
| <dl> <dt>**SEG \_ E \_ QOP \_ NO \_ COMPATIBLE**</dt> </dl>     | El contexto de [*seguridad*](../secgloss/i-gly.md) no admite la confidencialidad ni la [*integridad.*](../secgloss/s-gly.md) |

## <a name="remarks"></a>Observaciones

La **función EncryptMessage (Kerberos)** cifra un mensaje basado en el mensaje y la clave [*de sesión*](../secgloss/s-gly.md) de un contexto de [*seguridad*](../secgloss/s-gly.md).

Si la aplicación de transporte creó [*el*](../secgloss/s-gly.md) contexto de seguridad para admitir la detección de secuencia y el autor de la llamada proporciona un número de secuencia, la función incluye esta información con el mensaje cifrado. La inclusión de esta información protege contra la reproducción, inserción y supresión de mensajes. El [*paquete de seguridad*](../secgloss/s-gly.md) incorpora el número de secuencia pasado desde la aplicación de transporte.

> [!Note]  
> Estos búferes deben proporcionarse en el orden mostrado.

| Tipo de búfer                           | Descripción                                                                                                                    |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Secbuffer \_ STREAM \_ HEADER<  | Utilizado de forma interna. No se requiere inicialización.                                                                       |
| DATOS \_ SECBUFFER            | Contiene el [*mensaje de texto no*](../secgloss/s-gly.md) cifrado que se va a cifrar. |
| FINALIZADOR DE \_ SECUENCIAS DE \_ SECBUFFER | Utilizado de forma interna. No se requiere inicialización.                                                                        |
| SECBUFFER \_ EMPTY           | Utilizado de forma interna. No se requiere inicialización. El tamaño puede ser cero.                                                      |

Para obtener un rendimiento óptimo, *las estructuras pMessage* se deben asignar desde la memoria contigua.

**Windows XP:** Esta función también se conocía como **SealMessage.** Las aplicaciones ahora solo **deben usar EncryptMessage (Kerberos).**

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|-------------------------------------------|
| Cliente mínimo compatible | Windows Solo \[ aplicaciones de escritorio XP\]          |
| Servidor mínimo compatible | Windows Solo aplicaciones de escritorio de Server 2003 \[\] |
| Encabezado                   | Sspi.h (incluir Security.h)               |
| Biblioteca                  | Secur32.lib                               |
| Archivo DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**AcceptSecurityContext (Kerberos)**](acceptsecuritycontext--kerberos.md)
</dt> <dt>

[**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)
</dt> <dt>

[**InitializeSecurityContext (Kerberos)**](initializesecuritycontext--kerberos.md)
</dt> <dt>

[**QueryContextAttributes (Kerberos)**](querycontextattributes--kerberos.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>
