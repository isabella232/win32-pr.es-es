---
description: Permite abrir y administrar una conexión a una tarjeta inteligente.
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: Interfaz ISCard (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7dbbeccdf6c3fa9d586c841de661ed351ec37d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544227"
---
# <a name="iscard-interface"></a>Interfaz ISCard

\[La interfaz **ISCard** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

La interfaz **ISCard** permite abrir y administrar una conexión a una [*tarjeta inteligente*](../secgloss/s-gly.md). Cada conexión a una tarjeta requiere una única instancia correspondiente de la interfaz **ISCard** .

El administrador de [*recursos*](../secgloss/r-gly.md) de tarjeta inteligente debe estar disponible cada vez que se cree una instancia de **ISCard** . Si este servicio no está disponible, se producirá un error en la creación de la interfaz.

En el ejemplo siguiente se muestra un uso típico de la interfaz **ISCard** . La interfaz **ISCard** se utiliza para conectarse a la tarjeta inteligente, enviar una [*transacción*](../secgloss/t-gly.md)y liberar la tarjeta inteligente.

**Para enviar una transacción a una tarjeta específica**

1.  Cree una interfaz **ISCard** .
2.  Asociar a una tarjeta inteligente especificando un [*lector*](../secgloss/r-gly.md) de tarjeta inteligente o usando un identificador válido previamente establecido.
3.  Cree comandos de transacción con las interfaces de tarjeta inteligente [**ISCardCmd**](iscardcmd.md)y [**ISCardISO7816**](iscardiso7816.md) .
4.  Use **ISCard** para enviar los comandos de la transacción para su procesamiento por la tarjeta inteligente.
5.  Use **ISCard** para liberar la tarjeta inteligente.
6.  Libere la interfaz **ISCard** .

## <a name="members"></a>Miembros

La interfaz **ISCard** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCard** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **ISCard** tiene estos métodos.



| Método                                          | Descripción                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscard-attachbyhandle.md) | Asocia un objeto a un identificador de tarjeta inteligente abierto y configurado.<br/>                                                                                                                                                      |
| [**AttachByReader**](iscard-attachbyreader.md) | Abre la tarjeta inteligente en el lector con nombre.<br/>                                                                                                                                                                            |
| [**Conecta**](iscard-detach.md)                 | Cierra la conexión abierta a la tarjeta inteligente.<br/>                                                                                                                                                                        |
| [**LockSCard**](iscard-lockscard.md)           | Notifica el acceso exclusivo a la tarjeta inteligente.<br/>                                                                                                                                                                           |
| [**Volver a adjuntar**](iscard-reattach.md)             | Restablece y reinicializa la tarjeta inteligente.<br/>                                                                                                                                                                             |
| [**Transacción**](iscard-transaction.md)       | Ejecuta una operación de escritura y lectura en el objeto de comando de tarjeta inteligente ([*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md)).<br/> |
| [**UnlockScard**](iscard-unlockscard.md)       | Libera el acceso exclusivo a la tarjeta inteligente.<br/>                                                                                                                                                                         |



 

### <a name="properties"></a>Propiedades

La interfaz **ISCard** tiene estas propiedades.



| Propiedad                                               | Tipo de acceso          | Descripción                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atr**](iscard-get-atr.md)<br/>               | Solo lectura<br/> | Recupera la [*cadena ATR*](../secgloss/a-gly.md) de la tarjeta inteligente.<br/>                                                                   |
| [**CardHandle**](iscard-get-cardhandle.md)<br/> | Solo lectura<br/> | Recupera el identificador de la tarjeta inteligente conectada.<br/>                                                                                                                                  |
| [**Context**](iscard-get-context.md)<br/>       | Solo lectura<br/> | Recupera el identificador de [*contexto del administrador de recursos*](../secgloss/r-gly.md) actual.<br/>                            |
| [**Protocolo**](iscard-get-protocol.md)<br/>     | Solo lectura<br/> | Recupera el identificador del protocolo actualmente en uso en la tarjeta inteligente.<br/>                                                                                                        |
| [**Status**](iscard-get-status.md)<br/>         | Solo lectura<br/> | Recupera el [*Estado*](../secgloss/s-gly.md) actual en el que se encuentra la [*tarjeta inteligente*](../secgloss/s-gly.md) .<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



 

 
