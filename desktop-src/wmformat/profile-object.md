---
title: Objeto De perfil
description: Objeto De perfil
ms.assetid: ec42889e-580e-4a65-9fe6-4a5f15c97eb0
keywords:
- Windows SDK de formato multimedia, objetos de perfil
- Formato de sistemas avanzados (ASF), objetos de perfil
- ASF (formato de sistemas avanzados), objetos de perfil
- objects,profile objects
- profiles,objects
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6763d098819bde7d5db404aeffef3cd333d9b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266943"
---
# <a name="profile-object"></a>Objeto De perfil

Un objeto de perfil administra la configuración de un perfil. Los objetos de perfil se pueden crear para los datos de perfil existentes o se pueden crear vacíos, listos para recibir nuevos datos. El objeto de lector (y el objeto de lector sincrónico) también crea un objeto de perfil cuando se carga un archivo para su lectura. En este caso, el objeto se rellena con la información de perfil almacenada en el encabezado del archivo.

Para guardar el contenido de un objeto de perfil, debe llamar a [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).

Un perfil contiene varios objetos que controlan varios aspectos del perfil (como secuencias). Todos estos objetos están subordinados al objeto de perfil. Estos objetos no se crean con funciones de creación como lo haría con los objetos principales de este SDK. En su lugar, las interfaces del objeto de perfil contienen métodos que crean los objetos subordinados.

Para crear un objeto de perfil, llame a uno de los métodos siguientes.



| Método                                                                                | Descripción                                                                                                                                                     |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) | Crea un objeto de perfil sin datos de perfil.                                                                                                              |
| [**IWMProfileManager::LoadProfileByData**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)   | Crea un objeto de perfil rellenado con datos de un perfil guardado como una cadena. Esta es la única manera de crear un objeto de perfil con datos de un perfil personalizado. |
| [**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)       | Crea un objeto de perfil rellenado con datos de un perfil del sistema. Usa el GUID para identificar el perfil de sistema deseado.                                       |
| [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)   | Crea un objeto de perfil rellenado con datos de un perfil del sistema. Usa el índice de perfil para identificar el perfil de sistema deseado.                              |



 

Todos los métodos de la tabla anterior establecen un puntero a una **interfaz IWMProfile.** Las demás interfaces del objeto de perfil se pueden obtener llamando al **método QueryInterface.**

Todos los objetos de perfil admiten las interfaces siguientes.



| Interfaz                                  | Descripción                                                                                                                                       |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) | Administra una lista de idiomas admitidos por un archivo ASF.                                                                                             |
| [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)     | Controla el tamaño máximo de paquetes de un archivo.                                                                                                   |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)   | Controla el tamaño mínimo de los paquetes de un archivo. Hereda todos los métodos de **IWMPacketSize**.                                                 |
| [**IWMProfile**](iwmprofile.md)           | Controla la configuración básica y los objetos incluidos en un perfil.                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)         | Recupera el identificador único global (GUID) asociado al perfil. Hereda todos los métodos de **IWMProfile**.                       |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)         | Controla el uso compartido de ancho de banda y la información de priorización de flujos en un perfil. Hereda todos los métodos de **IWMProfile** **e IWMProfile2.** |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto del administrador de perfiles**](profile-manager-object.md)
</dt> <dt>

[**Perfiles**](profiles.md)
</dt> </dl>

 

 




