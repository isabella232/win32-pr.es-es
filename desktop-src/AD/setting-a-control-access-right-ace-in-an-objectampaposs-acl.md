---
title: Establecimiento de una ACE de derecho de acceso de control en la ACL de un objeto
description: Con ADSI, se establece una ACE de derecho de acceso de control igual que lo haría con una ACE específica de la propiedad, salvo que la propiedad IADsAccessControlEntry.ObjectType es el rightsGUID del derecho de acceso de control.
ms.assetid: 454dc372-47b0-457d-8660-644fcfa59be8
ms.tgt_platform: multiple
keywords:
- Establecimiento de una ACE de derecho de acceso de control en la ACL de un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09f4a4406bfa3d16a3e3be228bf4a0f131d77ad68cb99a6b9b2a8d328f15215e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024813"
---
# <a name="setting-a-control-access-right-ace-in-an-objects-acl"></a>Establecimiento de una ACE de derecho de acceso de control en la ACL de un objeto

Con ADSI, se establece una ACE de derecho de acceso de control igual que lo haría con una ACE específica de la propiedad, salvo que la propiedad [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) es **el rightsGUID** del derecho de acceso de control. Tenga en cuenta que también puede usar las API de seguridad de Win32 para establecer acl en objetos de directorio.

En la tabla siguiente se enumeran [**las propiedades IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para los derechos de acceso de control que se pueden usar para establecer las propiedades de una ACE.



| Propiedad                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Máscara de acceso**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Para los derechos de acceso de control que controlan el acceso de derechos extendidos a operaciones especiales, AccessMask debe contener la marca **\_ ADS RIGHT \_ DS CONTROL \_ \_ ACCESS.** Para los derechos de acceso de control que definen un conjunto de propiedades, AccessMask contiene **ADS \_ RIGHT \_ DS READ \_ \_ PROP** o **ADS RIGHT \_ \_ DS WRITE \_ \_ PROP**.<br/> Para los derechos de acceso de control que controlan las escrituras validadas, [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) contiene **ADS RIGHT \_ \_ DS \_ SELF**.<br/> |
| [**Banderas**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)      | Este valor debe incluir la marca **ADS FLAG OBJECT TYPE \_ \_ \_ \_ PRESENT.**                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Este valor debe tener el [**formato StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) del atributo **rightsGUID** del derecho de acceso de control. Tenga en cuenta que, en una ACE, la cadena GUID debe incluir las llaves de inicio y terminación, aunque el atributo **rightsGUID** del objeto **controlAccessRight** no incluya las llaves.                                                                                                                                     |
| [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | Ads **\_ ACETYPE \_ ACCESS ALLOWED \_ \_ OBJECT** para conceder al administrador de confianza el derecho de control de acceso o **ADS \_ ACETYPE ACCESS DENIED \_ \_ \_ OBJECT** para denegar al administrador de confianza el derecho de acceso de control.                                                                                                                                                                                                                                                                                                     |
| [**Fideicomisario**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | La entidad de seguridad, por ejemplo, usuario, grupo, equipo, y así sucesivamente, a la que se aplica la ACE.                                                                                                                                                                                                                                                                                                                                                                                              |



 

Para obtener más información sobre cómo crear una ACE, vea [Establecer derechos de acceso en un objeto](setting-access-rights-on-an-object.md).

Para obtener más información y un ejemplo de código para establecer una ACE, vea Ejemplo de código para establecer una [ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).

 

