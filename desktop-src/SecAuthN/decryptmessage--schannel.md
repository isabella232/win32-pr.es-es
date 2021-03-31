---
description: Descifra un mensaje mediante Schannel.
ms.assetid: 5d7c8598-2d6b-4839-ae98-dff964bc962c
title: DecryptMessage (Schannel) (función)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: 6bfbb354be9f3553e5369b8ce1f8b4260eab8ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808683"
---
# <a name="decryptmessage-schannel-function"></a>DecryptMessage (Schannel) (función)

La función **DecryptMessage (Schannel)** descifra un mensaje. Algunos paquetes no cifran y descifran mensajes, sino que realizan y comprueban un [*hash*](../secgloss/h-gly.md)de integridad.


Esta función también se usa con el [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_GLY) de Schannel (SSP) para indicar una solicitud del remitente de un mensaje para una renegociación (rehacer) de los atributos de conexión o para cerrar la conexión.

> [!Note]  
> Se puede llamar a [**EncryptMessage (Schannel)**](encryptmessage--schannel.md) y **DecryptMessage (Schannel)** al mismo tiempo desde dos subprocesos diferentes en un único contexto de la [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md#_SECURITY_SECURITY_SUPPORT_PROVIDER_INTERFACE_GLY) (SSPI) si un subproceso está cifrando y el otro está descifrando. Si se está cifrando más de un subproceso o se está descifrando más de un subproceso, cada subproceso debe obtener un contexto único.


## <a name="syntax"></a>Sintaxis

```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```

## <a name="parameters"></a>Parámetros

*phContext* \[ de\]


Identificador del contexto de [*seguridad*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) que se va a utilizar para descifrar el mensaje.

*pMessage* \[ in, out\]

Puntero a una estructura [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En la entrada, la estructura hace referencia a una o varias estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Uno de ellos puede ser de tipo SECBUFFER \_ Data. Ese búfer contiene el mensaje cifrado. El mensaje cifrado se descifra en contexto y sobrescribe el contenido original de su búfer.

Cuando se usa Schannel SSP con contextos que no están orientados a la conexión, en la entrada, la estructura debe contener cuatro estructuras [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Exactamente un búfer debe ser de tipo SECBUFFER \_ y contener un mensaje cifrado, que se descifra en su lugar. Los búferes restantes se utilizan para la salida y deben ser de tipo SECBUFFER \_ vacío. En el caso de los contextos orientados a la conexión, \_ se debe proporcionar un búfer de tipo de datos SECBUFFER, como se indica para los contextos no orientados a la conexión. Además, \_ también se debe proporcionar un segundo búfer de tipo de token de SECBUFFER que contenga un token de seguridad.

*MessageSeqNo* \[ de\]

El número de secuencia esperado por la aplicación de transporte, si existe. Si la aplicación de transporte no mantiene los números de secuencia, este parámetro debe establecerse en cero.

Cuando se usa Schannel SSP, este parámetro debe establecerse en cero. Schannel SSP no utiliza números de secuencia.

*pfQOP* \[ enuncia\]

Puntero a una variable de tipo **ULong** que recibe marcas específicas del paquete que indican la calidad de la protección.

Cuando se usa Schannel SSP, este parámetro no se utiliza y debe establecerse en **null**.

Este parámetro puede ser la marca siguiente.

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Value</th><th>Significado</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>No se cifró el mensaje, pero se produjo un encabezado o un finalizador.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT tiene el mismo valor y el mismo significado.</blockquote><br/></td></tr></tbody></table>

## <a name="return-value"></a>Valor devuelto

Si la función comprueba que el mensaje se ha recibido en la secuencia correcta, la función devuelve SEC \_ E \_ OK.

Si la función no puede descifrar el mensaje, devuelve uno de los siguientes códigos de error.

| Código devuelto                     | Descripción                                                                                                    |
|---------------------------------|----------------------------------------------------------------------------------------------------------------|
| **s \_ E \_ identificador no válido \_**     | Se especificó un identificador de contexto que no es válido en el parámetro *phContext* . Se usa con el SSP de Schannel.     |
| **s \_ E \_ token no válido \_**      | Los búferes son del tipo incorrecto o no se encontró ningún búfer de tipo SECBUFFER \_ datos. Se usa con el SSP de Schannel.  |
| **s \_ E \_ mensaje \_ modificado**    | El mensaje se ha modificado. Se usa con el SSP de Schannel.                                                      |
| **s \_ E \_ fuera \_ de \_ secuencia**   | No se recibió el mensaje en la secuencia correcta.                                                          |
| **s \_ I en \_ contexto \_ expirado**    | El remitente del mensaje ha terminado de usar la conexión y ha iniciado un cierre. Para obtener información acerca de cómo iniciar o reconocer un cierre, vea [apagar una conexión Schannel](shutting-down-an-schannel-connection.md). Se usa con el SSP de Schannel. |
| **s \_ I \_ renegotiate**         | La parte remota requiere una nueva secuencia de protocolo de enlace o la aplicación acaba de iniciar un cierre. Vuelva al bucle de negociación y llame a [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) o [**InitializeSecurityContext (Schannel)**](initializesecuritycontext--schannel.md), Pass SECBUFFER_EXTRA devuelve de DecryptMessage (). No se admite la renegociación para el modo de kernel Schannel. El autor de la llamada debe omitir este valor devuelto o cerrar la conexión. Si se omite el valor, puede que el cliente o el servidor cierren la conexión como resultado. |


## <a name="remarks"></a>Observaciones

A veces, una aplicación leerá datos de la parte remota, intentará descifrarlo mediante **DecryptMessage (Schannel)** y detectará que **DecryptMessage (Schannel)** se ejecutó correctamente, pero los búferes de salida están vacíos. Este comportamiento es normal y las aplicaciones deben ser capaces de solucionarlo.

Cuando se usa Schannel SSP, la función [**DecryptMessage (general)**](decryptmessage--general.md) devuelve la \_ hora en que se \_ ha agotado el contexto I en que \_ el remitente del mensaje ha cerrado la conexión. Para obtener información acerca de cómo iniciar o reconocer un cierre, vea [apagar una conexión Schannel](shutting-down-an-schannel-connection.md).

Si usa TLS 1,0, puede que tenga que llamar varias veces a esta función, ajustando el búfer de entrada en cada llamada, para descifrar un mensaje completo.


La función **DecryptMessage (Schannel)** devuelve s \_ que realizo una \_ renegociación cuando el remitente del mensaje desea volver a negociar la conexión ([*contexto de seguridad*](../secgloss/s-gly.md)). Una aplicación controla una renegociación solicitada mediante una llamada a [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (lado del servidor) o a [**InitializeSecurityContext (Schannel**](initializesecuritycontext--schannel.md) ) (cliente) y pass SECBUFFER_EXTRA devueltos desde DecryptMessage (). Después de que esta llamada inicial devuelva un valor, continúe como si la aplicación estuviera creando una nueva conexión. Para obtener más información, vea [crear un contexto de seguridad de Schannel](creating-an-schannel-security-context.md).


## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------------------------|-------------------------------------------|
| Cliente mínimo compatible | Solo aplicaciones de escritorio de Windows XP \[\]          |
| Servidor mínimo compatible | Solo aplicaciones de escritorio de Windows Server 2003 \[\] |
| Encabezado                   | SSPI. h (incluir Security. h)               |
| Biblioteca                  | SECUR32. lib                               |
| Archivo DLL                      | Secur32.dll                               |

## <a name="see-also"></a>Vea también

- [Funciones SSPI](authentication-functions.md#sspi-functions)
- [**EncryptMessage (Schannel)**](encryptmessage--schannel.md)
- [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
- [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
