---
description: Proporciona los métodos necesarios para construir y administrar una unidad de datos del protocolo de aplicación de tarjeta inteligente (APDU).
ms.assetid: fd84bb2e-27da-4670-b8e8-56c7948b78bb
title: Interfaz ISCardCmd (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd
- ISCardCmd.Type
- ISCardCmd.get_Type
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f14291f3777dcdc8b661f96f94d987209100a365
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069142"
---
# <a name="iscardcmd-interface"></a>Interfaz ISCardCmd

\[La **interfaz ISCardCmd** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

La **interfaz ISCardCmd** proporciona los métodos necesarios para construir y administrar una [*unidad*](../secgloss/s-gly.md) de datos de protocolo de aplicación de tarjeta [*inteligente*](../secgloss/a-gly.md) (APDU). Esta interfaz encapsula dos búferes:

-   El búfer de APDU contiene la secuencia de comandos que se enviará a la tarjeta.
-   El búfer APDUReply contiene los datos devueltos desde la tarjeta después de la ejecución del comando APDU (estos datos también se conocen como APDU de devolución).

En el ejemplo siguiente se muestra un uso típico de la **interfaz ISCardCmd.** La **interfaz ISCardCmd** se usa para compilar una APDU.

**Para enviar una transacción a una tarjeta específica**

1.  Cree una [**interfaz ISCard**](iscard.md) y conéctese a una tarjeta inteligente.
2.  Cree una **interfaz ISCardCmd.**
3.  Cree un comando APDU de tarjeta inteligente mediante la [**interfaz ISCardISO7816**](iscardiso7816.md) o uno de los métodos **de compilación ISCardCmd.**
4.  Ejecute el comando en la tarjeta inteligente llamando al método de [**interfaz ISCard**](iscard.md) adecuado.
5.  Evalúe la respuesta devuelta.
6.  Repita el procedimiento según sea necesario.
7.  Libere la **interfaz ISCardCmd** y otras según sea necesario.

## <a name="members"></a>Members

La **interfaz ISCardCmd** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardCmd también** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz ISCardCmd** tiene estos métodos.



| Método                                       | Descripción                                                                                                |
|:---------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**BuildCmd**](iscardcmd-buildcmd.md)       | Construye una APDU de comando válida para la transmisión a una tarjeta inteligente.<br/>                               |
| [**Claro**](iscardcmd-clear.md)             | Borra los búferes de mensajes apdu y apdu de respuesta.<br/>                                             |
| [**Encapsular**](iscardcmd-encapsulate.md) | Encapsula el apdu de comando dado en otro comando APDU para la transmisión a una tarjeta inteligente.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz ISCardCmd** tiene estas propiedades.



| Propiedad                                                              | Tipo de acceso           | Descripción                                                                                                                                                         |
|:----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AlternateClassId**](iscardcmd-get-alternateclassid.md)<br/> | Lectura y escritura<br/> | Valor actual del identificador de clase alternativa.<br/>                                                                                                                        |
| [**Apdu**](iscardcmd-get-apdu.md)<br/>                         | Lectura y escritura<br/> | Unidad [*de datos del protocolo de aplicación*](../secgloss/a-gly.md) (APDU) sin procesar.<br/> |
| [**ApduLength**](iscardcmd-get-apdulength.md)<br/>             | Solo lectura<br/>  | Longitud de la APDU.<br/>                                                                                                                                      |
| [**ApduReply**](iscardcmd-get-apdureply.md)<br/>               | Lectura y escritura<br/> | [*Responder a APDU*](../secgloss/r-gly.md).<br/>                                                                        |
| [**ApduReplyLength**](iscardcmd-get-apdureplylength.md)<br/>   | Lectura y escritura<br/> | Longitud de la APDU de respuesta.<br/>                                                                                                                                |
| [**Classid**](iscardcmd-get-classid.md)<br/>                   | Lectura y escritura<br/> | Identificador de clase de la APDU.<br/>                                                                                                                                    |
| [**data**](iscardcmd-get-data.md)<br/>                         | Solo lectura<br/>  | Campo de datos de la APDU.<br/>                                                                                                                                  |
| [**InstructionId**](iscardcmd-get-instructionid.md)<br/>       | Lectura y escritura<br/> | Byte de id. de instrucción de la APDU.<br/>                                                                                                                       |
| [**LeField**](iscardcmd-get-lefield.md)<br/>                   | Solo lectura<br/>  | Campo Le de la APDU.<br/>                                                                                                                                    |
| [**Nad**](iscardcmd-put-nad.md)<br/>                           | Lectura y escritura<br/> | Dirección del nodo.<br/>                                                                                                                                            |
| [**P1**](iscardcmd-get-p1.md)<br/>                             | Lectura y escritura<br/> | Primer byte de parámetro de la APDU.<br/>                                                                                                                        |
| [**P2**](iscardcmd-get-p2.md)<br/>                             | Lectura y escritura<br/> | Segundo byte de parámetro de la APDU.<br/>                                                                                                                       |
| [**P3**](iscardcmd-get-p3.md)<br/>                             | Solo lectura<br/>  | Tercer byte de parámetro de la APDU.<br/>                                                                                                                        |
| [**ReplyNad**](iscardcmd-get-replynad.md)<br/>                 | Lectura y escritura<br/> | Dirección de nodo utilizada por la tarjeta en el mensaje de respuesta.<br/>                                                                                                      |
| [**ReplyStatus**](iscardcmd-get-replystatus.md)<br/>           | Lectura y escritura<br/> | [*Palabra de estado del mensaje de APDU*](../secgloss/r-gly.md) de respuesta.<br/>                                                    |
| [**ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)<br/>     | Solo lectura<br/>  | Responder al byte de estado SW1 del mensaje de APDU.<br/>                                                                                                                    |
| [**ReplyStatusSW2**](iscardcmd-get-replystatussw2.md)<br/>     | Solo lectura<br/>  | Responder al byte de estado SW2 del mensaje de APDU.<br/>                                                                                                                    |
| **Tipo**<br/>                                                   | Solo lectura<br/>  | Reservado para uso futuro.<br/>                                                                                                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardCmd se define como \_ D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



 

 
