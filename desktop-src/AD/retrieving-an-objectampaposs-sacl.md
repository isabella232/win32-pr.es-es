---
title: Recuperar la SACL de un objeto
description: El descriptor de seguridad de un objeto de Active Directory Domain Services puede contener una lista de control de acceso del sistema (SACL).
ms.assetid: b1da91a2-d9b0-48a3-9de5-1e588209032d
ms.tgt_platform: multiple
keywords:
- DACL AD
- SACL AD, recuperar la SACL de un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 537846f2080aecdab8e22f5fce5bdfa36298fb74
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104358799"
---
# <a name="retrieving-an-objects-sacl"></a>Recuperar la SACL de un objeto

El descriptor de seguridad de un objeto de Active Directory Domain Services puede contener una lista de control de acceso del sistema (SACL). Una SACL contiene entradas de control de acceso (ACE) que especifican los tipos de intentos de acceso que generan registros de auditoría en el registro de eventos de seguridad de un controlador de dominio. Tenga en cuenta que una SACL genera entradas de registro solo en el controlador de dominio en el que se produjo el intento de acceso, no en todos los DC que contienen una réplica del objeto.

Para establecer u obtener la SACL de un descriptor de seguridad de objeto, el privilegio de **\_ \_ nombre de seguridad se** debe habilitar en el token de acceso del subproceso que lo solicita. El grupo administradores tiene este privilegio de forma predeterminada y se puede asignar a otros usuarios o grupos. Para obtener más información, consulte [derechos de acceso de SACL](/windows/desktop/SecAuthZ/sacl-access-right).

Para obtener y establecer la SACL de un objeto de directorio, use la interfaz [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . Con C++, el método [**IADsSecurityDescriptor:: get \_ SystemAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) devuelve un puntero [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Llame a **QueryInterface** en ese puntero **IDispatch** para obtener una interfaz [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) y use los métodos de esa interfaz para tener acceso a las ACE individuales en la SACL. Para obtener más información sobre el procedimiento para modificar una SACL, que es similar a la de modificar una DACL, consulte [configuración de derechos de acceso en un objeto](setting-access-rights-on-an-object.md).

Para enumerar las ACE en una SACL, use el método [**IADsAccessControlList:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) , que devuelve un puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Llame a **QueryInterface** en ese puntero **IUnknown** para obtener una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) . Use el método [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) para enumerar las ACE de la ACL. Cada ACE se devuelve como un **valor de tipo Variant** que contiene un puntero [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ; Tenga en cuenta que el miembro de **VT** es el **\_ envío de VT**. Llame a **QueryInterface** en ese puntero **IDispatch** para obtener una interfaz [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para la ACE. Use los métodos de la interfaz **IADsAccessControlEntry** para establecer u obtener los componentes de una ACE.

Para obtener más información acerca de las SACL, consulte:

-   [Listas de control de acceso (ACL)](/windows/desktop/SecAuthZ/access-control-lists)
-   [Generación de auditoría](/windows/desktop/SecAuthZ/audit-generation)

 

 