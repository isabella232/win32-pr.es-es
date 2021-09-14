---
description: La interfaz ISCardDatabase proporciona los métodos para realizar las operaciones de base de datos del administrador de recursos de tarjeta inteligente.
ms.assetid: 56db3bc0-33c3-4b9c-a4a7-374fc491d8fd
title: Interfaz ISCardDatabase (Scardmgr.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171253"
---
# <a name="iscarddatabase-interface"></a>Interfaz ISCardDatabase

\[La **interfaz ISCardDatabase** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

La **interfaz ISCardDatabase proporciona** los métodos para realizar las operaciones [*de*](../secgloss/s-gly.md) base de datos del administrador de recursos de [*tarjeta*](../secgloss/r-gly.md) inteligente. Estas operaciones incluyen la [](../secgloss/r-gly.md)enumeración de tarjetas inteligentes conocidas, lectores y grupos de lectores, además de recuperar las interfaces compatibles con una tarjeta inteligente y su proveedor de [*servicios principal.*](../secgloss/p-gly.md)

> [!Note]  
> El identificador del proveedor de servicios principal es un GUID COM que se puede usar para crear instancias y usar los objetos COM para una tarjeta específica.

 

En el ejemplo siguiente se muestra un uso típico de la **interfaz ISCardDatabase.** En este caso, la **interfaz ISCardDatabase** se usa para enumerar todas las tarjetas inteligentes conocidas.

**Para enviar una transacción a una tarjeta específica**

1.  Cree una **interfaz ISCardDatabase.**
2.  Llame [**a ListCards**](iscarddatabase-listcards.md) para recuperar todas las tarjetas inteligentes conocidas basadas en una [*cadena ATR*](../secgloss/a-gly.md) o en sus interfaces admitidas.
3.  Libere la **interfaz ISCardDatabase.**

## <a name="members"></a>Members

La **interfaz ISCardDatabase** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardDatabase también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ISCardDatabase** tiene estos métodos.



| Método                                                          | Descripción                                                                                                                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetProviderCardId**](iscarddatabase-getprovidercardid.md)   | Recupera el identificador del proveedor de [*servicios principal*](../secgloss/p-gly.md) para una tarjeta inteligente específica.<br/> |
| [**ListCardInterfaces**](iscarddatabase-listcardinterfaces.md) | Recupera los identificadores de interfaz (GUID) de todas las interfaces compatibles con una tarjeta inteligente específica.<br/>                                                                                 |
| [**ListCards**](iscarddatabase-listcards.md)                   | Recupera todos los nombres de tarjeta inteligente que coinciden con un conjunto específico de identificadores de interfaz [*(GUID)*](../secgloss/a-gly.md)o una cadena ATR .<br/> |
| [**ListReaderGroups**](iscarddatabase-listreadergroups.md)     | Recupera los nombres de los grupos [*de lectores de*](../secgloss/r-gly.md) los que el administrador de recursos tiene conocimiento.<br/>                        |
| [**ListReaders**](iscarddatabase-listreaders.md)               | Recupere los nombres de los [*lectores de*](../secgloss/r-gly.md) los que el administrador de recursos tiene conocimientos.<br/>                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardDatabase se define como \_ 1461AAC8-6810-11D0-918F-00AA00C18068<br/>       |



 

 
