---
description: La interfaz ISCardLocate proporciona servicios para buscar una tarjeta inteligente por su nombre.
ms.assetid: add00705-69d5-4562-a74f-94c6864f6bd8
title: Interfaz ISCardLocate (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate
- ISCardLocate.ConfigureCardGuidSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e65a8315e796db032dfa6e9cb8898d19437bad05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244226"
---
# <a name="iscardlocate-interface"></a>Interfaz ISCardLocate

\[La **interfaz ISCardLocate** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

La **interfaz ISCardLocate** proporciona servicios para buscar una [*tarjeta inteligente*](../secgloss/s-gly.md) por su nombre.

Esta interfaz puede mostrar la interfaz de usuario [*de tarjeta inteligente*](../secgloss/u-gly.md) si es necesario.

En el escenario siguiente se muestra un uso típico de la **interfaz ISCardLocate.** La **interfaz ISCardLocate** se usa para compilar una unidad [*de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU).

**Para buscar una tarjeta específica con su nombre**

1.  Cree una **interfaz ISCardLocate.**
2.  Llame [**a ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) para buscar un nombre de tarjeta inteligente.
3.  Llame [**a FindCard**](iscardlocate-findcard.md) para buscar la tarjeta inteligente.
4.  Interpretará los resultados.
5.  Libere la **interfaz ISCardLocate.**

## <a name="members"></a>Members

La **interfaz ISCardLocate** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardLocate** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ISCardLocate** tiene estos métodos.



| Método                                                                  | Descripción                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| **ConfigureCardGuidSearch**                                             | Reservado para uso futuro.<br/>                                        |
| [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) | Especifica el nombre de la tarjeta que se usará en la búsqueda.<br/>               |
| [**FindCard**](iscardlocate-findcard.md)                               | Busca la tarjeta inteligente y abre una conexión válida a ella.<br/> |



 

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
| IID<br/>                      | IID ISCardLocate se define como \_ 1461AACD-6810-11D0-918F-00AA00C18068<br/>         |



 

 
