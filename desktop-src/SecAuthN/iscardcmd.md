---
description: Proporciona los métodos necesarios para construir y administrar una unidad de datos de protocolo de aplicación de tarjeta inteligente (APDU).
ms.assetid: fd84bb2e-27da-4670-b8e8-56c7948b78bb
title: Interfaz ISCardCmd (Scarddat. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104081998"
---
# <a name="iscardcmd-interface"></a>Interfaz ISCardCmd

\[La interfaz **ISCardCmd** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

La interfaz **ISCardCmd** proporciona los métodos necesarios para construir y administrar una [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) (APDU). Esta interfaz encapsula dos búferes:

-   El búfer APDU contiene la secuencia de comandos que se enviará a la tarjeta.
-   El búfer APDUReply contiene los datos devueltos por la tarjeta después de la ejecución del comando APDU (estos datos también se conocen como APDU de devolución).

En el ejemplo siguiente se muestra un uso típico de la interfaz **ISCardCmd** . La interfaz **ISCardCmd** se utiliza para compilar una APDU.

**Para enviar una transacción a una tarjeta específica**

1.  Cree una interfaz [**ISCard**](iscard.md) y conéctese a una tarjeta inteligente.
2.  Cree una interfaz **ISCardCmd** .
3.  Cree un comando APDU de tarjeta inteligente mediante la interfaz [**ISCardISO7816**](iscardiso7816.md) o uno de los métodos de compilación **ISCardCmd** .
4.  Ejecute el comando en la tarjeta inteligente llamando al método de interfaz [**ISCard**](iscard.md) adecuado.
5.  Evalúe la respuesta devuelta.
6.  Repita el procedimiento según sea necesario.
7.  Libere la interfaz **ISCardCmd** y otras según sea necesario.

## <a name="members"></a>Miembros

La interfaz **ISCardCmd** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardCmd** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **ISCardCmd** tiene estos métodos.



| Método                                       | Descripción                                                                                                |
|:---------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**BuildCmd**](iscardcmd-buildcmd.md)       | Construye un APDU de comando válido para la transmisión a una tarjeta inteligente.<br/>                               |
| [**Claridad**](iscardcmd-clear.md)             | Borra los búferes APDU y mensaje APDU de respuesta.<br/>                                             |
| [**Encapsular**](iscardcmd-encapsulate.md) | Encapsula el APDU de comando dado en otro APDU de comando para su transmisión a una tarjeta inteligente.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **ISCardCmd** tiene estas propiedades.



| Propiedad                                                              | Tipo de acceso           | Descripción                                                                                                                                                         |
|:----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AlternateClassId**](iscardcmd-get-alternateclassid.md)<br/> | Lectura/escritura<br/> | Valor de identificador de clase alternativo actual.<br/>                                                                                                                        |
| [**Categorías APDU**](iscardcmd-get-apdu.md)<br/>                         | Lectura/escritura<br/> | [*Unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) sin formato (APDU).<br/> |
| [**ApduLength**](iscardcmd-get-apdulength.md)<br/>             | Solo lectura<br/>  | Longitud de las APDU.<br/>                                                                                                                                      |
| [**ApduReply**](iscardcmd-get-apdureply.md)<br/>               | Lectura/escritura<br/> | Las [*APDU de respuesta*](../secgloss/r-gly.md).<br/>                                                                        |
| [**ApduReplyLength**](iscardcmd-get-apdureplylength.md)<br/>   | Lectura/escritura<br/> | Longitud de APDU de respuesta.<br/>                                                                                                                                |
| [**ClassId**](iscardcmd-get-classid.md)<br/>                   | Lectura/escritura<br/> | IDENTIFICADOR de clase de APDU.<br/>                                                                                                                                    |
| [**Data**](iscardcmd-get-data.md)<br/>                         | Solo lectura<br/>  | Campo de datos de APDU.<br/>                                                                                                                                  |
| [**InstructionId**](iscardcmd-get-instructionid.md)<br/>       | Lectura/escritura<br/> | IDENTIFICADOR byte de la instrucción de APDU.<br/>                                                                                                                       |
| [**LeField**](iscardcmd-get-lefield.md)<br/>                   | Solo lectura<br/>  | Campo de la APDU.<br/>                                                                                                                                    |
| [**Nad**](iscardcmd-put-nad.md)<br/>                           | Lectura/escritura<br/> | Dirección de nodo.<br/>                                                                                                                                            |
| [**P1**](iscardcmd-get-p1.md)<br/>                             | Lectura/escritura<br/> | Primer parámetro byte de APDU.<br/>                                                                                                                        |
| [**P2**](iscardcmd-get-p2.md)<br/>                             | Lectura/escritura<br/> | Segundo parámetro byte de APDU.<br/>                                                                                                                       |
| [**P3**](iscardcmd-get-p3.md)<br/>                             | Solo lectura<br/>  | Tercer parámetro byte de APDU.<br/>                                                                                                                        |
| [**ReplyNad**](iscardcmd-get-replynad.md)<br/>                 | Lectura/escritura<br/> | Dirección de nodo usada por la tarjeta en el mensaje de respuesta.<br/>                                                                                                      |
| [**ReplyStatus**](iscardcmd-get-replystatus.md)<br/>           | Lectura/escritura<br/> | La palabra de estado de mensaje [*APDU de respuesta*](../secgloss/r-gly.md) .<br/>                                                    |
| [**ReplyStatusSW1**](iscardcmd-get-replystatussw1.md)<br/>     | Solo lectura<br/>  | Responder al mensaje de APDU de SW1 de estado byte.<br/>                                                                                                                    |
| [**ReplyStatusSW2**](iscardcmd-get-replystatussw2.md)<br/>     | Solo lectura<br/>  | Responder al mensaje de APDU de SW2 de estado byte.<br/>                                                                                                                    |
| **Tipo**<br/>                                                   | Solo lectura<br/>  | Reservado para uso futuro.<br/>                                                                                                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd se define como D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



 

 
