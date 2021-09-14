---
title: Interfaz de IWMProfile
description: La interfaz IWMProfile es la interfaz principal de un objeto de perfil.
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- Formato multimedia de windows de la interfaz IWMProfile
- IWMProfile interface windows Media Format , descrito
topic_type:
- apiref
api_name:
- IWMProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- wmsdkidl.h
ms.openlocfilehash: f814df820bd50a36abf2ee8e453549f46c9c5c9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256239"
---
# <a name="iwmprofile-interface"></a>Interfaz de IWMProfile

La **interfaz IWMProfile** es la interfaz principal de un objeto [*de*](wmformat-glossary.md) perfil. Un objeto de perfil se usa para configurar perfiles personalizados. Puede usar **IWMProfile para** crear, eliminar o modificar objetos de configuración de flujo y objetos de exclusión mutua. También puede establecer y recuperar información general sobre el perfil. Para acceder a todas las características del objeto de perfil, debe usar [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), que hereda de **IWMProfile** e [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).

**IWMProfile** también es accesible a través del objeto reader, donde puede usarlo para obtener información sobre las secuencias de un archivo que se carga en el lector. Al acceder **a IWMProfile** desde el lector, puede realizar cambios en el perfil, pero ninguno de los cambios se puede guardar en el archivo. A menudo resulta útil usar el perfil de un archivo existente como base de un nuevo perfil. El lector sincrónico **admite IWMProfile** de la misma manera que el lector.

La información de perfil obtenida a través del lector o lector sincrónico no procede de un archivo .prx. El lector usa la información del archivo ASF para ensamblar las configuraciones de flujo. Por lo tanto, cierta información de perfil, como el nombre y la descripción, no están disponibles a través del lector.

Hay varias maneras de obtener un puntero a una **interfaz IWMProfile.** El administrador de perfiles tiene métodos para crear un nuevo perfil y acceder a los perfiles existentes. Todos estos métodos establecen un **puntero IWMProfile.** Al leer un archivo, se puede obtener un puntero a **IWMProfile** llamando al **método QueryInterface** de cualquier interfaz de lector. Del mismo modo, cualquier interfaz del objeto de lector sincrónico puede obtener un puntero con una llamada a **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).

## <a name="members"></a>Members

La **interfaz IWMProfile** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMProfile** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMProfile** tiene estos métodos.



| Método                                                                  | Descripción                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)             | Agrega un objeto de exclusión mutua al perfil.<br/>                                   |
| [**AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)                               | Agrega una secuencia al perfil.<br/>                                                    |
| [**CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | Crea un objeto de exclusión mutua para el perfil.<br/>                               |
| [**CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)                   | Crea un objeto de configuración de flujo para el perfil.<br/>                           |
| [**GetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription)                     | Recupera la descripción del perfil.<br/>                                        |
| [**GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | Recupera un objeto de exclusión mutua del perfil.<br/>                            |
| [**GetMutualExclusionCount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount)   | Recupera el número de objetos de exclusión mutua en el perfil.<br/>                 |
| [**GetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getname)                                   | Recupera el nombre del perfil.<br/>                                               |
| [**GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | Recupera una secuencia, mediante un número de índice, del perfil.<br/>                     |
| [**GetStreamByNumber**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | Recupera una secuencia, utilizando el número de la secuencia, del perfil.<br/>            |
| [**GetStreamCount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | Recupera el número de secuencias del perfil.<br/>                                  |
| [**GetVersion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | Recupera el número de versión de Microsoft Servicios de Windows Media en el perfil.<br/> |
| [**ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | Permite que los cambios realizados en una configuración de flujo se incluyan en el perfil.<br/>    |
| [**RemoveMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | Quita un objeto de exclusión mutua del perfil.<br/>                              |
| [**RemoveStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | Quita una secuencia del perfil.<br/>                                               |
| [**RemoveStreamByNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | Quita una secuencia del perfil.<br/>                                               |
| [**SetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | Especifica la descripción del perfil.<br/>                                        |
| [**SetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | Especifica el nombre del perfil.<br/>                                               |



 

Para obtener información sobre qué interfaces se pueden obtener mediante el método QueryInterface de esta interfaz, vea el tema del objeto en el que se implementa esta interfaz.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaces**](interfaces.md)
</dt> <dt>

[**IWMProfileManager (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Objeto del administrador de perfiles**](profile-manager-object.md)
</dt> <dt>

[**Objeto del lector**](reader-object.md)
</dt> <dt>

[**Objeto del lector sincrónico**](synchronous-reader-object.md)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

