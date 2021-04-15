---
title: Objeto del administrador de perfiles
description: Objeto del administrador de perfiles
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- SDK de Windows Media Format, objetos de administrador de perfiles
- Advanced Systems Format (ASF), objetos de administrador de perfiles
- ASF (formato de sistemas avanzados), objetos de administrador de perfiles
- objetos, objetos del administrador de perfiles
- perfiles, objetos
- perfiles, objetos de administrador de perfiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce3d77598f52e43a840c1b6b3ef58baa47f77bd
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105714347"
---
# <a name="profile-manager-object"></a>Objeto del administrador de perfiles

Un perfil es un conjunto de parámetros de medios que se usan para crear un archivo ASF. El objeto de administrador de perfiles crea objetos de perfil para su edición. Los objetos de perfil se pueden crear sin datos en ellos o compilados a partir de datos de perfil existentes. El objeto de administrador de perfiles también proporciona métodos para enumerar códecs admitidos y consultar los códecs para obtener información.

El objeto de administrador de perfiles se crea mediante la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) , que establece un puntero a una interfaz [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . Las demás interfaces del objeto de administrador de perfiles se pueden obtener llamando al método **QueryInterface** .

El objeto de administrador de perfiles admite las siguientes interfaces.



| Interfaz                                                      | Descripción                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | Recupera información acerca de los códecs admitidos y sus formatos.                                                                              |
| [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | Recupera los nombres de los códecs admitidos y las descripciones de sus formatos. Hereda todos los métodos de **IWMCodecInfo**.          |
| [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | Recupera las propiedades de códec y los códecs de consultas para las características admitidas. Hereda todos los métodos de **IWMCodecInfo** y **IWMCodecInfo2**. |
| [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | Crea nuevos perfiles, carga perfiles existentes y guarda perfiles personalizados.                                                                    |
| [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | Controla la versión de los perfiles del sistema enumerados por el administrador de perfiles. Hereda todos los métodos de **IWMProfileManager**.             |
| [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | Controla el idioma de los perfiles del sistema analizados por el administrador de perfiles.                                                                  |



 

## <a name="remarks"></a>Observaciones

Cuando se crea un objeto de administrador de perfiles, analiza todos los perfiles del sistema, lo que puede tardar varios segundos. La creación y liberación de un administrador de perfiles cada vez que se necesita usar, afectará negativamente al rendimiento. Debe crear un administrador de perfiles una vez en la aplicación y liberarlo solo cuando ya no tenga que usarlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**de la empresa**](objects.md)
</dt> <dt>

[**Objeto de perfil**](profile-object.md)
</dt> <dt>

[**Perfiles**](profiles.md)
</dt> </dl>

 

 




