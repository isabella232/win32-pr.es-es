---
description: La interfaz ISCardDatabase proporciona los métodos para realizar las operaciones de base de datos del administrador de recursos de tarjeta inteligente.
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: Interfaz ISCardDatabase (Scardmgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardDatabase
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1ae74c813b4d95cc9d02694ca9edb5c030e4f342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648203"
---
# <a name="iscarddatabase-interface"></a>Interfaz ISCardDatabase

\[La interfaz **ISCardDatabase** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

La interfaz **ISCardDatabase** proporciona los métodos para realizar las operaciones de base [*de datos del administrador de recursos de*](../secgloss/r-gly.md) [*tarjeta inteligente*](../secgloss/s-gly.md) . Entre estas operaciones se incluyen la enumeración de tarjetas inteligentes, [*lectores*](../secgloss/r-gly.md)y grupos de lectores conocidos, además de la recuperación de las interfaces admitidas por una tarjeta inteligente y su [*proveedor de servicios principal*](../secgloss/p-gly.md).

> [!Note]  
> El identificador del proveedor de servicios principal es un GUID COM que se puede utilizar para crear instancias y usar los objetos COM para una tarjeta específica.

 

En el ejemplo siguiente se muestra un uso típico de la interfaz **ISCardDatabase** . En este caso, la interfaz **ISCardDatabase** se usa para enumerar todas las tarjetas inteligentes conocidas.

**Para enviar una transacción a una tarjeta específica**

1.  Cree una interfaz **ISCardDatabase** .
2.  Llame a [**ListCards**](iscarddatabase-listcards.md) para recuperar todas las tarjetas inteligentes conocidas basadas en una [*cadena ATR*](../secgloss/a-gly.md) o en sus interfaces admitidas.
3.  Libere la interfaz **ISCardDatabase** .

## <a name="members"></a>Miembros

La interfaz **ISCardDatabase** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardDatabase** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ISCardDatabase** tiene estos métodos.



| Método                                                          | Descripción                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetProviderCardId**](iscarddatabase-getprovidercardid.md)   | Recupera el identificador del [*proveedor de servicios principal*](../secgloss/p-gly.md) de una tarjeta inteligente específica.<br/> |
| [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) | Recupera los identificadores de interfaz (GUID) de todas las interfaces admitidas por una tarjeta inteligente específica.<br/>                                                                                 |
| [**ListCards**](iscarddatabase-listcards.md)                   | Recupera todos los nombres de tarjetas inteligentes que coinciden con un conjunto específico de identificadores de interfaz (GUID) o una [*cadena ATR*](../secgloss/a-gly.md).<br/> |
| [**ListReaderGroups**](iscarddatabase-listreadergroups.md)     | Recupera los nombres de los [*grupos de lectores*](../secgloss/r-gly.md) de los que el administrador de recursos tiene conocimiento.<br/>                        |
| [**ListReaders**](iscarddatabase-listreaders.md)               | Recupere los nombres de los [*lectores*](../secgloss/r-gly.md) de los que el administrador de recursos tiene conocimiento.<br/>                                          |



 

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
| IID<br/>                      | IID \_ ISCardDatabase se define como 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



 

 
