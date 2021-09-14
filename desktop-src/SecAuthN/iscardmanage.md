---
description: Se usa para adjuntar a una tarjeta inteligente o lector específicos, para crear otras interfaces opcionales para realizar funciones de tarjeta inteligente específicas, para bloquear una tarjeta inteligente específica para uso exclusivo y para obtener el estado de una tarjeta inteligente o lector.
ms.assetid: 67077034-5bd0-4176-9dc7-774caba3d427
title: Interfaz ISCardManage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage
api_type:
- COM
api_location: ''
ms.openlocfilehash: cce31ea21701c098b09a0bd96360afb374a9bccc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244149"
---
# <a name="iscardmanage-interface"></a>Interfaz ISCardManage

\[La **interfaz ISCardManage** ya no está disponible para su uso a partir de Windows Server 2008, Windows Vista y Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

La siguiente definición de interfaz se proporciona como un estándar que se puede seguir al desarrollar un [*proveedor de servicios de tarjeta*](../secgloss/s-gly.md) [*inteligente*](../secgloss/c-gly.md).

Se **debe proporcionar la interfaz ISCardManage.** Se usa para adjuntar a [](../secgloss/s-gly.md) una tarjeta inteligente o lector específicos, [](../secgloss/r-gly.md)para crear otras interfaces opcionales para realizar funciones de tarjeta inteligente específicas, para bloquear una tarjeta inteligente específica para uso exclusivo y para obtener el estado de una tarjeta inteligente o lector. Como conjunto, estos servicios pueden ser responsables de mantener un contexto bien definido en el que una aplicación puede comunicarse con una [*tarjeta inteligente*](../secgloss/s-gly.md) o un [*lector*](../secgloss/r-gly.md).

A continuación se muestra un uso típico **de la interfaz ISCardManage.**

**Para conectarse a una tarjeta inteligente**

1.  Cree la **interfaz ISCardManage** asociada a la tarjeta.
2.  Conectar a una tarjeta inteligente mediante la asociación a un lector de tarjeta inteligente específico [**(AttachByIFD)**](iscardmanage-attachbyifd.md)o mediante un identificador adquirido previamente ([**AttachByHandle**](iscardmanage-attachbyhandle.md)).
3.  Cree otras interfaces para realizar operaciones de tarjeta inteligente [**(CreateCardAuth,**](iscardmanage-createcardauth.md) [**CreateFileAccess,**](iscardmanage-createfileaccess.md) [**CreateCHVerification**](iscardmanage-createchverification.md)o [**CreateInterface).**](iscardmanage-createinterface.md)
4.  Libere la tarjeta ([**Desasoyen**](iscardmanage-detach.md)).
5.  Libere la **interfaz ISCardManage** y otras según sea necesario.

## <a name="members"></a>Members

La **interfaz ISCardManage** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardManage** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ISCardManage** tiene estos métodos.



| Método                                                            | Descripción                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscardmanage-attachbyhandle.md)             | Permite a una aplicación crear un vínculo de comunicación a una tarjeta inteligente mediante un identificador devuelto por el administrador de recursos [*de tarjeta inteligente*](../secgloss/r-gly.md).<br/>                                              |
| [**AttachByIFD**](iscardmanage-attachbyifd.md)                   | Permite a una aplicación solicitar el establecimiento de un contexto para un lector específico al que se hace referencia con un nombre para mostrar.<br/>                                                                                                                                               |
| [**CreateCardAuth**](iscardmanage-createcardauth.md)             | Permite la creación de una [**interfaz ISCardAuth.**](iscardauth.md)<br/>                                                                                                                                                                                            |
| [**CreateCHVerification**](iscardmanage-createchverification.md) | Permite la creación de una [**interfaz ISCardVerify.**](iscardverify.md)<br/>                                                                                                                                                                                        |
| [**CreateFileAccess**](iscardmanage-createfileaccess.md)         | Permite la creación de una [**interfaz ISCardFileAccess.**](iscardfileaccess.md)<br/>                                                                                                                                                                                |
| [**CreateInterface**](iscardmanage-createinterface.md)           | Permite la creación de una interfaz.<br/>                                                                                                                                                                                                                            |
| [**Separar**](iscardmanage-detach.md)                             | Libera los datos adjuntos a una tarjeta inteligente o lector determinados asignados [**por AttachByHandle**](iscardmanage-attachbyhandle.md) [**o AttachByIFD,**](iscardmanage-attachbyifd.md) respectivamente.<br/>                                                                |
| [**Volver a conectar**](iscardmanage-reconnect.md)                       | Permite que una aplicación se vuelva a conectar [](iscardmanage-detach.md) a una tarjeta inteligente o lector sin tener que emitir una desasordenada seguida de [**AttachByHandle**](iscardmanage-attachbyhandle.md) o [**AttachByIFD,**](iscardmanage-attachbyifd.md) respectivamente.<br/> |
| [**SCardLock**](iscardmanage-scardlock.md)                       | Bloquea una tarjeta inteligente conectada o un lector para uso exclusivo.<br/>                                                                                                                                                                                                       |
| [**SCardUnlock**](iscardmanage-scardunlock.md)                   | Libera el uso exclusivo de la tarjeta inteligente o el lector conectados.<br/>                                                                                                                                                                                                   |
| [**Estado**](iscardmanage-status.md)                             | Permite que una aplicación obtenga el estado actual de la tarjeta inteligente o el lector.<br/>                                                                                                                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



 

 
