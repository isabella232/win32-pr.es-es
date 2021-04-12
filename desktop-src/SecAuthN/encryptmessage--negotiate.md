---
description: Cifra un mensaje para ofrecer privacidad mediante Negotiate.
ms.assetid: b80b3d64-9c0a-4602-9378-1e208f6593fc
title: EncryptMessage (Negotiate) (función)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 037866088f58fa1d70939b84062161a6e4f610b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361219"
---
# <a name="encryptmessage-negotiate-function"></a>EncryptMessage (Negotiate) (función)

La función **EncryptMessage (Negotiate)** cifra un mensaje para proporcionar [*privacidad*](../secgloss/p-gly.md). **EncryptMessage (Negotiate)** permite a la aplicación elegir entre los [*algoritmos criptográficos*](../secgloss/c-gly.md) admitidos por el mecanismo elegido. La función **EncryptMessage (Negotiate)** utiliza el [*contexto de seguridad*](../secgloss/s-gly.md) al que hace referencia el identificador de contexto. Algunos paquetes no tienen mensajes cifrados o descifrados, sino que proporcionan un [*hash*](../secgloss/h-gly.md) de integridad que se puede comprobar.

> [!Note]  
> Se puede llamar a **EncryptMessage (Negotiate)** y [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) al mismo tiempo desde dos subprocesos diferentes en un único contexto de la [*interfaz del proveedor de compatibilidad con seguridad*](../secgloss/s-gly.md) (SSPI) si un subproceso está cifrando y el otro está descifrando. Si se está cifrando más de un subproceso o se está descifrando más de un subproceso, cada subproceso debe obtener un contexto único.

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

*phContext* \[ en \] un identificador del [*contexto de seguridad*](../secgloss/s-gly.md) que se va a utilizar para cifrar el mensaje.

*fQOP* \[ en \] marcas específicas del paquete que indican la calidad de la protección. Un [*paquete de seguridad*](../secgloss/s-gly.md) puede usar este parámetro para habilitar la selección de [*algoritmos criptográficos*](../secgloss/c-gly.md).

Este parámetro puede ser la marca siguiente.

| Value                  | Significado                                                     |
|------------------------|-------------------------------------------------------------|
| SECQOP_WRAP_NO_ENCRYPT | Producir un encabezado o un finalizador, pero no cifrar el mensaje. |

> [!NOTE]
> KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.

*pMessage* \[ en, \] un puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que pueden ser de tipo SecBuffer \_ Data. Ese búfer contiene el mensaje que se va a cifrar. El mensaje está cifrado en su lugar, sobrescribiendo el contenido original de la estructura.

La función no procesa los búferes con el \_ atributo SECBUFFER ReadOnly.

La longitud de la estructura [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) que contiene el mensaje no debe ser mayor que **cbMaximumMessage**, que se obtiene a partir de la función [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md) ( \_ tamaños de flujo SECPKG ATTR \_ \_ ).

Las aplicaciones que no usan SSL deben proporcionar un [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) de tipo SecBuffer \_ padding.

*MessageSeqNo* \[ en \] el número de secuencia que la aplicación de transporte asignó al mensaje. Si la aplicación de transporte no mantiene los números de secuencia, este parámetro debe ser cero.

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve SEC \_ E \_ OK.

Si se produce un error en la función, devuelve uno de los siguientes códigos de error.

| Código devuelto                         | Descripción                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **búfer de s \_ E s \_ \_ demasiado \_ pequeño**      | El búfer de salida es demasiado pequeño. Para obtener más información, vea la sección Comentarios.                                                                   |
| **SEC \_ E \_ contexto \_ expirado**        | La aplicación hace referencia a un contexto que ya se ha cerrado. Una aplicación escrita correctamente no debe recibir este error. |
| **s \_ E \_ \_ sistema criptográfico \_ no válido** | No se admite el [*cifrado*](../secgloss/c-gly.md) elegido para el [*contexto de seguridad*](../secgloss/s-gly.md) .                                |
| **s \_ E \_ memoria insuficiente \_**    | No hay suficiente memoria disponible para completar la acción solicitada.                                                               |
| **s \_ E \_ identificador no válido \_**         | Se especificó un identificador de contexto que no es válido en el parámetro *phContext* .                                                       |
| **s \_ E \_ token no válido \_**          | No \_ se encontró ningún búfer de tipo de datos SECBUFFER.                                                                                            |
| **s \_ E \_ QOP \_ no \_ admitidos**     | La confidencialidad o la [*integridad*](../secgloss/i-gly.md) no son compatibles con el [*contexto de seguridad*](../secgloss/s-gly.md).             |

## <a name="remarks"></a>Observaciones

La función **EncryptMessage (Negotiate)** cifra un mensaje basado en el mensaje y la [*clave de sesión*](../secgloss/s-gly.md) de un [*contexto de seguridad*](../secgloss/s-gly.md).

Si la aplicación de transporte creó el [*contexto de seguridad*](../secgloss/s-gly.md) para admitir la detección de secuencias y el autor de la llamada proporciona un número de secuencia, la función incluye esta información con el mensaje cifrado. La inclusión de esta información protege contra la reproducción, inserción y supresión de mensajes. El [*paquete de seguridad*](../secgloss/s-gly.md) incorpora el número de secuencia que se pasa desde la aplicación de transporte.

> [!Note]  
> Estos búferes se deben proporcionar en el orden mostrado.

| Tipo de búfer                | Descripción                                                                                 |
|----------------------------|---------------------------------------------------------------------------------------------|
| SECBUFFER \_ encabezado de secuencia \_  | Utilizado de forma interna. No se requiere inicialización.                                                |
| datos de SECBUFFER \_            | Contiene el mensaje de [*texto simple*](../secgloss/s-gly.md) que se va a cifrar. |
| \_finalizador de flujo SECBUFFER \_ | Utilizado de forma interna. No se requiere inicialización.                                                |
| SECBUFFER \_ vacío           | Utilizado de forma interna. No se requiere inicialización. El tamaño puede ser cero.                              |

Para un rendimiento óptimo, las estructuras *pMessage* se deben asignar desde la memoria contigua.

**Windows XP:** Esta función también se conocía como **SealMessage**. Las aplicaciones ahora deben usar **EncryptMessage (Negotiate)** solamente.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|-------------------------------------------------|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows XP \[\]                |
| Servidor mínimo compatible | Solo aplicaciones de escritorio de Windows Server 2003 \[\]       |
| Encabezado                   | SSPI. h (incluir Security. h)                     |
| Biblioteca                  | SECUR32. lib                                     |
| Archivo DLL                      | Secur32.dll                                     |

## <a name="see-also"></a>Vea también

- [Funciones SSPI](authentication-functions.md#sspi-functions)
- [**AcceptSecurityContext (Negotiate)**](acceptsecuritycontext--negotiate.md)
- [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md)
- [**InitializeSecurityContext (negociar)**](initializesecuritycontext--negotiate.md)
- [**QueryContextAttributes (Negotiate)**](querycontextattributes--negotiate.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
