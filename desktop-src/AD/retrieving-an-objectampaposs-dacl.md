---
title: Recuperación de la DACL de un objeto
description: El descriptor de seguridad de un objeto puede contener una lista de control de acceso discrecional (DACL).
ms.assetid: 93b16094-9923-4886-804f-4e989fbf6977
ms.tgt_platform: multiple
keywords:
- DACL AD
- DACL AD, recuperar DACL de un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db74cb235b5cb322f0edf3dc4cfb32f50b4c00c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104358798"
---
# <a name="retrieving-an-objects-dacl"></a>Recuperación de la DACL de un objeto

El descriptor de seguridad de un objeto puede contener una lista de control de acceso discrecional (DACL). Una DACL contiene cero o más entradas de control de acceso (ACE) que identifican a los usuarios y grupos que pueden tener acceso al objeto. Si una DACL está vacía (es decir, contiene cero ACE), no se concede ningún acceso explícitamente, por lo que el acceso se deniega implícitamente. Sin embargo, si el descriptor de seguridad de un objeto no tiene una DACL, el objeto no está protegido y todos los usuarios tienen acceso completo.

Para recuperar la DACL de un objeto, debe ser el propietario del objeto o tener acceso de **\_ control de lectura** al objeto.

Para obtener y establecer la DACL de un objeto de directorio, use la interfaz [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . Con C++, el método [**IADsSecurityDescriptor:: get \_ DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) devuelve un puntero [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Llame a **QueryInterface** en ese puntero **IDispatch** para obtener una interfaz [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) y use los métodos de esa interfaz para tener acceso a las ACE individuales de la DACL. El procedimiento para modificar una DACL se describe en [establecer derechos de acceso en un objeto](setting-access-rights-on-an-object.md).

Para enumerar las ACE, use el método [**IADsAccessControlList:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) . El método devuelve un puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Llame a **QueryInterface** en ese puntero **IUnknown** para obtener una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) . Use el método [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) para enumerar las ACE de la ACL. Cada ACE se devuelve como una **variante** que contiene un puntero [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (el miembro **VT** es el **\_ envío de VT**). Llame a **QueryInterface** en ese puntero **IDispatch** para obtener una interfaz [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para la ACE. Puede usar los métodos de la interfaz **IADsAccessControlEntry** para establecer o recuperar los componentes de una ACE.

Para obtener más información sobre las DACL y las ACE, vea los temas siguientes en el kit de desarrollo de software (SDK) de la plataforma.

-   [Listas de control de acceso (ACL)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Entradas de control de acceso (ACE)](/windows/desktop/SecAuthZ/access-control-entries)

 

 