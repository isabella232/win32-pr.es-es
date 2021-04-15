---
title: Elección de una interfaz para el enlace
description: Cuando se enlaza un objeto de directorio, el autor de la llamada especifica el tipo de interfaz ADSI deseada.
ms.assetid: 3c86e136-6d82-4baf-9c76-27dac8ad68ac
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usar, elegir una interfaz para el enlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444bd41d1567849d5bf3a85ac3ec22f317ced5d3
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421403"
---
# <a name="choosing-an-interface-for-binding"></a>Elección de una interfaz para el enlace

Cuando se enlaza un objeto de directorio, el autor de la llamada especifica el tipo de interfaz ADSI deseada. Todos los objetos de directorio ADSI admiten la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . Un objeto ADSI también puede admitir otras interfaces. Las interfaces reales que admite el objeto dependen de la clase de objeto. Por ejemplo, un objeto de usuario es compatible con la interfaz [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) , pero no admite la interfaz [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) .

Los clientes de automatización deben usar las interfaces de **IADs \*** porque son interfaces duales que proporcionan un mayor nivel de abstracción y proporcionan datos mediante el tipo de datos [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .

Además de las interfaces **IADs \*** , los clientes de C/C++ pueden usar las interfaces [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) . Estas interfaces no son interfaces duales y no admiten la automatización. Estas interfaces proporcionan un mayor control sobre los atributos que se van a recuperar y permiten el acceso a los datos sin procesar almacenados en una propiedad. Por ejemplo, cuando se usa el método [**IADs:: get**](/windows/desktop/api/Iads/nf-iads-iads-get) para recuperar el atributo **ntSecurityDescriptor** de un objeto, el método **IADs:: get** proporciona un puntero de interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que admite la interfaz [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) . ADSI proporciona la interfaz **IADsSecurityDescriptor** para representar un descriptor de seguridad. En comparación, cuando se usa el método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) para recuperar el atributo **ntSecurityDescriptor** , **IDirectoryObject:: GetObjectAttributes** proporciona una matriz de bytes que se puede convertir en una estructura de [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . Las API de seguridad de Win32 se pueden usar con estos datos para manipular el descriptor de seguridad.

 

 