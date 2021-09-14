---
description: Permite abrir y administrar una conexión a una tarjeta inteligente.
ms.assetid: f49f76e6-eed9-4e85-b48f-29f7bad40218
title: Interfaz ISCard (Scardmgr.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071254"
---
# <a name="iscard-interface"></a>Interfaz ISCard

\[La **interfaz ISCard** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

La **interfaz ISCard** permite abrir y administrar una conexión a una [*tarjeta inteligente.*](../secgloss/s-gly.md) Cada conexión a una tarjeta requiere una única instancia correspondiente de la **interfaz ISCard.**

El administrador de [*recursos de tarjeta inteligente*](../secgloss/r-gly.md) debe estar disponible cada vez que se crea una instancia de **ISCard.** Si este servicio no está disponible, se producirá un error en la creación de la interfaz.

En el ejemplo siguiente se muestra un uso típico de la **interfaz ISCard.** La **interfaz ISCard** se usa para conectarse a la tarjeta inteligente, enviar una [*transacción*](../secgloss/t-gly.md)y liberar la tarjeta inteligente.

**Para enviar una transacción a una tarjeta específica**

1.  Cree una **interfaz ISCard.**
2.  Adjunte a una tarjeta inteligente especificando un lector de [*tarjetas*](../secgloss/r-gly.md) inteligentes o usando un identificador válido establecido previamente.
3.  Cree comandos de transacción con las interfaces de tarjeta inteligente [**ISCardCmd**](iscardcmd.md)e [**ISCardISO7816.**](iscardiso7816.md)
4.  Use **ISCard** para enviar los comandos de transacción para su procesamiento mediante la tarjeta inteligente.
5.  Use **ISCard** para liberar la tarjeta inteligente.
6.  Libere la **interfaz ISCard.**

## <a name="members"></a>Members

La **interfaz ISCard** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCard** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz ISCard** tiene estos métodos.



| Método                                          | Descripción                                                                                                                                                                                                                     |
|:------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscard-attachbyhandle.md) | Asocia un objeto a un identificador de tarjeta inteligente abierto y configurado.<br/>                                                                                                                                                      |
| [**AttachByReader**](iscard-attachbyreader.md) | Abre la tarjeta inteligente en el lector con nombre.<br/>                                                                                                                                                                            |
| [**Separar**](iscard-detach.md)                 | Cierra la conexión abierta a la tarjeta inteligente.<br/>                                                                                                                                                                        |
| [**LockSCard**](iscard-lockscard.md)           | Reclama acceso exclusivo a la tarjeta inteligente.<br/>                                                                                                                                                                           |
| [**Reinstale**](iscard-reattach.md)             | Restablece y reinicializa la tarjeta inteligente.<br/>                                                                                                                                                                             |
| [**Transacción**](iscard-transaction.md)       | Ejecuta una operación de escritura y lectura en el objeto de comando de tarjeta inteligente [*(unidad de datos del protocolo de aplicación).*](../secgloss/a-gly.md)<br/> |
| [**UnlockScard**](iscard-unlockscard.md)       | Libera el acceso exclusivo a la tarjeta inteligente.<br/>                                                                                                                                                                         |



 

### <a name="properties"></a>Propiedades

La **interfaz ISCard** tiene estas propiedades.



| Propiedad.                                               | Tipo de acceso          | Descripción                                                                                                                                                                                    |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atr**](iscard-get-atr.md)<br/>               | Solo lectura<br/> | Recupera la [*cadena ATR*](../secgloss/a-gly.md) de la tarjeta inteligente.<br/>                                                                   |
| [**CardHandle**](iscard-get-cardhandle.md)<br/> | Solo lectura<br/> | Recupera el identificador de la tarjeta inteligente conectada.<br/>                                                                                                                                  |
| [**Contexto**](iscard-get-context.md)<br/>       | Solo lectura<br/> | Recupera el identificador de [*contexto actual del administrador de*](../secgloss/r-gly.md) recursos.<br/>                            |
| [**Protocolo**](iscard-get-protocol.md)<br/>     | Solo lectura<br/> | Recupera el identificador del protocolo actualmente en uso en la tarjeta inteligente.<br/>                                                                                                        |
| [**Status**](iscard-get-status.md)<br/>         | Solo lectura<br/> | Recupera el estado [*actual en el*](../secgloss/s-gly.md) que se encuentra [*la*](../secgloss/s-gly.md) tarjeta inteligente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCard se define como \_ 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



 

 
