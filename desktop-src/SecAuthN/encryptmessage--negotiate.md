---
description: Cifra un mensaje para proporcionar privacidad mediante Negotiate.
ms.assetid: b80b3d64-9c0a-4602-9378-1e208f6593fc
title: Función EncryptMessage (Negotiate)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: d4aac05a4ad030e72953cc997671b7d348cb2a598a0f56f80963f69847cdf357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008313"
---
# <a name="encryptmessage-negotiate-function"></a>Función EncryptMessage (Negotiate)

La **función EncryptMessage (Negotiate)** cifra un mensaje para proporcionar [*privacidad.*](../secgloss/p-gly.md) **EncryptMessage (Negotiate) permite** a la aplicación elegir entre los [*algoritmos criptográficos*](../secgloss/c-gly.md) admitidos por el mecanismo elegido. La **función EncryptMessage (Negotiate)** usa el [*contexto de seguridad*](../secgloss/s-gly.md) al que hace referencia el identificador de contexto. Algunos paquetes no tienen mensajes que cifrar o descifrar, sino que proporcionan un hash de [*integridad*](../secgloss/h-gly.md) que se puede comprobar.

> [!Note]  
> Se puede llamar a **EncryptMessage (Negotiate)** y [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) al mismo tiempo desde dos subprocesos diferentes en un único contexto de interfaz de proveedor de compatibilidad de seguridad [](../secgloss/s-gly.md) (SSPI) si se cifra un subproceso y el otro se descifra. Si se cifra más de un subproceso o se descifra más de un subproceso, cada subproceso debe obtener un contexto único.

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

*phContext* \[ en \] Identificador del contexto de seguridad [*que*](../secgloss/s-gly.md) se va a usar para cifrar el mensaje.

*fQOP* \[ en \] Marcas específicas del paquete que indican la calidad de la protección. Un [*paquete de seguridad*](../secgloss/s-gly.md) puede usar este parámetro para habilitar la selección de [*algoritmos criptográficos*](../secgloss/c-gly.md).

Este parámetro puede ser la marca siguiente.

| Value                  | Significado                                                     |
|------------------------|-------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | Generar un encabezado o finalizador, pero no cifrar el mensaje. |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.

*pMessage* \[ in, out \] Puntero a una estructura [**SecBufferDesc.**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) En la entrada, la estructura hace referencia a una o varias [**estructuras secBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que pueden ser de tipo SECBUFFER \_ DATA. Ese búfer contiene el mensaje que se va a cifrar. El mensaje se cifra en su lugar, sobrescribiendo el contenido original de la estructura.

La función no procesa búferes con el atributo SECBUFFER \_ READONLY.

La longitud de la estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contiene el mensaje no debe ser mayor que **cbMaximumMessage**, que se obtiene de la función [**QueryContextAttributes (Negotiate) (SECPKG**](querycontextattributes--negotiate.md) \_ ATTR \_ STREAM \_ SIZES).

Las aplicaciones que no usan SSL deben proporcionar [**un SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de tipo SECBUFFER \_ PADDING.

*MessageSeqNo* \[ en \] El número de secuencia que la aplicación de transporte asignó al mensaje. Si la aplicación de transporte no mantiene números de secuencia, este parámetro debe ser cero.

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve SEC \_ E \_ OK.

Si se produce un error en la función, devuelve uno de los siguientes códigos de error.

| Código devuelto                         | Descripción                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **BÚFER \_ E DE S DEMASIADO \_ \_ \_ PEQUEÑO**      | El búfer de salida es demasiado pequeño. Para obtener más información, vea la sección Comentarios.                                                                   |
| **SEG \_ E CONTEXT EXPIRED (CONTEXTO E DE SEC \_ E \_ EXPIRADO)**        | La aplicación hace referencia a un contexto que ya se ha cerrado. Una aplicación escrita correctamente no debe recibir este error. |
| **SEC \_ E \_ CRYPTO \_ SYSTEM \_ INVALID** | No [*se admite*](../secgloss/c-gly.md) el cifrado elegido para el [*contexto*](../secgloss/s-gly.md) de seguridad.                                |
| **S \_ E \_ MEMORIA \_ INSUFICIENTE**    | No hay suficiente memoria disponible para completar la acción solicitada.                                                               |
| **IDENTIFICADOR \_ NO VÁLIDO DE SEC E \_ \_**         | Se especificó un identificador de contexto que no es válido en el *parámetro phContext.*                                                       |
| **TOKEN \_ NO VÁLIDO DE SEC E \_ \_**          | No se encontró ningún \_ búfer de tipo DE DATOS SECBUFFER.                                                                                            |
| **SEG \_ E \_ QOP \_ NO \_ COMPATIBLE**     | El contexto de seguridad [*no*](../secgloss/i-gly.md) admite la confidencialidad ni la [*integridad.*](../secgloss/s-gly.md)             |

## <a name="remarks"></a>Comentarios

La **función EncryptMessage (Negotiate)** cifra un mensaje basado en el mensaje y la clave [*de sesión*](../secgloss/s-gly.md) de un contexto de [*seguridad*](../secgloss/s-gly.md).

Si la aplicación de transporte creó [*el*](../secgloss/s-gly.md) contexto de seguridad para admitir la detección de secuencia y el autor de la llamada proporciona un número de secuencia, la función incluye esta información con el mensaje cifrado. La inclusión de esta información protege contra la reproducción, inserción y supresión de mensajes. El [*paquete de seguridad*](../secgloss/s-gly.md) incorpora el número de secuencia que se pasa desde la aplicación de transporte.

> [!Note]  
> Estos búferes deben proporcionarse en el orden mostrado.

| Tipo de búfer                | Descripción                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| ENCABEZADO DE \_ SECUENCIA DE \_ SECBUFFER  | Utilizado de forma interna. No se requiere inicialización.                                                |
| DATOS DE \_ SECBUFFER            | Contiene el [*mensaje de texto no*](../secgloss/s-gly.md) cifrado que se va a cifrar. |
| FINALIZADOR DE \_ SECUENCIAS DE \_ SECBUFFER | Utilizado de forma interna. No se requiere inicialización.                                                |
| SECBUFFER \_ EMPTY           | Utilizado de forma interna. No se requiere inicialización. El tamaño puede ser cero.                              |

Para obtener un rendimiento óptimo, las *estructuras pMessage* se deben asignar desde la memoria contigua.

**Windows XP:** Esta función también se conocía como **SealMessage**. Las aplicaciones ahora solo **deben usar EncryptMessage (Negotiate).**

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|-------------------------------------------------|
| Cliente mínimo compatible | Windows XP \[ solo aplicaciones de escritorio\]                |
| Servidor mínimo compatible | Windows Solo aplicaciones de escritorio de Server 2003 \[\]       |
| Header                   | Sspi.h (incluir Security.h)                     |
| Biblioteca                  | Secur32.lib                                     |
| Archivo DLL                      | Secur32.dll                                     |

## <a name="see-also"></a>Vea también

- [Funciones SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md)
- [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md)
- [**InitializeSecurityContext (Negotiate)**](initializesecuritycontext--negotiate.md)
- [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
