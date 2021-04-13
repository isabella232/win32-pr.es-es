---
title: Crear descriptores de seguridad para nuevos objetos de directorio
description: Puede usar ADSI para crear un descriptor de seguridad y establecerlo como la propiedad nTSecurityDescriptor de un objeto nuevo o usarlo para reemplazar la propiedad nTSecurityDescriptor de un objeto existente.
ms.assetid: b9ff626f-17f1-4fc1-9d6e-4f47e29a5aeb
ms.tgt_platform: multiple
keywords:
- Crear un descriptor de seguridad para un nuevo objeto de directorio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78265d27c52023d669e27fc9890fd2d5273e2ffd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487475"
---
# <a name="creating-security-descriptors-for-new-directory-objects"></a>Crear descriptores de seguridad para nuevos objetos de directorio

Puede usar ADSI para crear un descriptor de seguridad y establecerlo como la propiedad **ntSecurityDescriptor** de un objeto nuevo o usarlo para reemplazar la propiedad **ntSecurityDescriptor** de un objeto existente.

Para crear un descriptor de seguridad para un objeto:

1.  Use [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el objeto com ADSI para el nuevo descriptor de seguridad y obtener un puntero de interfaz [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) a ese objeto. Tenga en cuenta que el ID. de clase es el **\_ SecurityDescriptor de CLSID**.
2.  Use el método de [**\_ propietario IADsSecurityDescriptor::p UT**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para establecer el propietario del objeto. El administrador de confianza es un usuario, un grupo u otra entidad de seguridad. Una aplicación debe usar el valor de la propiedad adecuada del objeto de usuario o grupo del administrador de confianza al que se va a aplicar la ACE.
3.  Use el método de [**\_ control IADsSecurityDescriptor::p UT**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para controlar si el objeto hereda DACL y SACL de su contenedor primario.
4.  Use [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el objeto com ADSI para la DACL para el nuevo descriptor de seguridad y obtener un puntero de interfaz [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) a ese objeto. Tenga en cuenta que el identificador de clase es **CLSID \_ AccessControlList**.
5.  Para cada ACE que se va a agregar a la DACL, use [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para crear el objeto com ADSI para la nueva ACE y obtener un puntero de interfaz [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) a ese objeto. Tenga en cuenta que el identificador de clase es CLSID \_ AccessControlEntry.
6.  Para cada ACE que se va a agregar a la DACL, establezca las propiedades de la ACE mediante los métodos de propiedad del objeto [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) de la ACE. Para obtener más información sobre las propiedades que se deben establecer en una ACE, vea [establecer derechos de acceso en un objeto](setting-access-rights-on-an-object.md).
7.  Para cada ACE que se va a agregar a la DACL, use el método **QueryInterface** en el objeto [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para obtener un puntero [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . El método [**IADsAccessControlList:: AddAce**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace) requiere un puntero de interfaz **IDISPATCH** a la ACE.
8.  Para cada ACE que se va a agregar a la DACL, use [**IADsAccessControlList:: AddAce**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-addace) para agregar la nueva ACE a la DACL. Tenga en cuenta que el orden de las ACE dentro de la ACL puede afectar a la evaluación del acceso al objeto. El acceso correcto al objeto puede requerir que cree una nueva ACL, que agregue las ACE de la ACL existente en el orden correcto a la nueva ACL y que, a continuación, reemplace la ACL existente en el descriptor de seguridad por la nueva ACL. Para obtener más información, vea [orden de las ACE en una DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).
9.  Siga los pasos del 4-8 para crear la SACL para el nuevo descriptor de seguridad.
10. Use el método [**IADsSecurityDescriptor::p UT \_ DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para establecer la DACL. Para obtener más información acerca de las DACL, vea [DACL NULL y DACL vacías](null-dacls-and-empty-dacls.md).
11. Use el método [**IADsSecurityDescriptor::p UT \_ SystemAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para establecer la SACL.
12. Convierta el objeto [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) en una [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) mediante el método **QueryInterface** del objeto **IADsSecurityDescriptor** para obtener una interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . A continuación, establezca el miembro **VT** de la **variante** en el **\_ envío de VT** y establezca el miembro **pdispVal** de la **variante** igual al puntero **IDispatch** .
13. Obtener un puntero de interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) al objeto.
14. Use el método [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) con "nTSecurityDescriptor" y la [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) creada anteriormente para escribir el nuevo descriptor de seguridad en la caché de propiedades.
15. Use el método [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para actualizar la propiedad en el objeto en el directorio.

 

 