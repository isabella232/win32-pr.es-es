---
title: Recuperar la DACL de un objeto
description: El descriptor de seguridad de un objeto puede contener una lista de control de acceso discrecional (DACL).
ms.assetid: 93b16094-9923-4886-804f-4e989fbf6977
ms.tgt_platform: multiple
keywords:
- DACL AD
- DACL AD , recuperación de la DACL de un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b515e6c5d28be7003734510300fc7f6d2de776b479b56e62ad521567c76dce4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025113"
---
# <a name="retrieving-an-objects-dacl"></a>Recuperar la DACL de un objeto

El descriptor de seguridad de un objeto puede contener una lista de control de acceso discrecional (DACL). Una DACL contiene cero o más entradas de control de acceso (ACE) que identifican a los usuarios y grupos que pueden acceder al objeto. Si una DACL está vacía (es decir, contiene cero ACE), no se concede acceso explícitamente, por lo que el acceso se deniega implícitamente. Sin embargo, si el descriptor de seguridad de un objeto no tiene una DACL, el objeto está desprotegido y todos los usuarios tienen acceso completo.

Para recuperar la DACL de un objeto, debe ser el propietario del objeto o tener acceso **DE \_ CONTROL** DE LECTURA al objeto.

Para obtener y establecer la DACL de un objeto de directorio, use la [**interfaz IADsSecurityDescriptor.**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) Con C++, [**el método IADsSecurityDescriptor::get \_ DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) devuelve un [**puntero IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Llame **a QueryInterface** en ese puntero **IDispatch** para obtener una interfaz [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) y use los métodos de esa interfaz para acceder a las ACE individuales en la DACL. El procedimiento para modificar una DACL se describe en [Establecer derechos de acceso en un objeto](setting-access-rights-on-an-object.md).

Para enumerar las ACE, use el [**método IADsAccessControlList::get \_ \_ NewEnum.**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) El método devuelve un [**puntero IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) Llame **a QueryInterface** en **ese puntero IUnknown** para obtener una [**interfaz IEnumVARIANT.**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) Use el [**método IEnumVARIANT::Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) para enumerar las ACE en la ACL. Cada ACE se devuelve como **una VARIANT** que contiene un [**puntero IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (el **miembro vt** es **VT \_ DISPATCH**). Llame **a QueryInterface** en **ese puntero IDispatch** para obtener una [**interfaz IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para la ACE. Puede usar los métodos de la **interfaz IADsAccessControlEntry** para establecer o recuperar los componentes de una ACE.

Para más información sobre las DACL y las ACE, consulte los temas siguientes en Platform Software Development Kit (SDK).

-   [Listas de control de acceso (ACL)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Entradas de control de acceso (ACE)](/windows/desktop/SecAuthZ/access-control-entries)

 

 