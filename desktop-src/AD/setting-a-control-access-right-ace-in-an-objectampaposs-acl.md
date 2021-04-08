---
title: Establecer una ACE right de control de acceso en la ACL de un objeto
description: Con ADSI, se establece una ACE de derechos de acceso de control de la misma manera que una ACE específica de la propiedad, excepto que la propiedad IADsAccessControlEntry. ObjectType es el rightsGUID del derecho de acceso de control.
ms.assetid: 454dc372-47b0-457d-8660-644fcfa59be8
ms.tgt_platform: multiple
keywords:
- Establecer una ACE right de control de acceso en la ACL de un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b870ad3ed5432060fb51fe14c29a81ce4665
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995061"
---
# <a name="setting-a-control-access-right-ace-in-an-objects-acl"></a>Establecer una ACE right de control de acceso en la ACL de un objeto

Con ADSI, se establece una ACE de derechos de acceso de control de la misma manera que una ACE específica de la propiedad, excepto que la propiedad [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) es el **rightsGUID** del derecho de acceso de control. Tenga en cuenta que también puede usar las API de seguridad de Win32 para establecer ACL en objetos de directorio.

En la tabla siguiente se enumeran las propiedades de [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para los derechos de acceso de control que se pueden usar para establecer las propiedades de una ACE.



| Propiedad                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Para los derechos de acceso de control que controlan el acceso a los derechos extendidos a operaciones especiales, AccessMask debe contener la marca de **\_ \_ \_ \_ acceso de control DS derecho de ADS** . En el caso de los derechos de acceso de control que definen un conjunto de propiedades, AccessMask contiene los **anuncios \_ right \_ DS \_ Read \_ prop** y/o **ADS \_ right \_ DS \_ Write \_ prop**.<br/> Para los derechos de acceso de control que controlan las escrituras validadas, [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) contiene **ad \_ right \_ DS \_ Self**.<br/> |
| [**Marcas**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)      | Este valor debe incluir la **marca \_ \_ present de \_ tipo \_ de objeto de marca ADS** .                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) | Este valor debe ser el formato [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) del atributo **rightsGUID** del derecho de acceso de control. Tenga en cuenta que, en una ACE, la cadena de GUID debe incluir las llaves de inicio y de finalización, aunque el atributo **rightsGUID** del objeto **controlAccessRight** no incluya las llaves.                                                                                                                                     |
| [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | El **\_ \_ \_ \_ objeto permitido de ADS ACETYPE tiene acceso** para conceder al administrador de confianza el permiso de control de acceso o **ADS \_ ACETYPE \_ acceso \_ denegado \_** para denegar al administrador de confianza el derecho de acceso de control.                                                                                                                                                                                                                                                                                                     |
| [**Confianza**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)    | La entidad de seguridad, por ejemplo, usuario, grupo, equipo, etc., a la que se aplica la ACE.                                                                                                                                                                                                                                                                                                                                                                                              |



 

Para obtener más información sobre la creación de una ACE, consulte [configuración de derechos de acceso en un objeto](setting-access-rights-on-an-object.md).

Para obtener más información y un ejemplo de código para establecer una ACE, vea [código de ejemplo para establecer una ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).

 

