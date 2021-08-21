---
title: Objeto del administrador de perfiles
description: Objeto del administrador de perfiles
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- Windows SDK de formato multimedia, objetos del administrador de perfiles
- Formato de sistemas avanzados (ASF),objetos del administrador de perfiles
- ASF (formato de sistemas avanzados),objetos del administrador de perfiles
- objects,profile manager objects
- profiles,objects
- profiles,profile manager objects
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce272067e98f787d5136cacc0a2d02f474264f14f14aa785b28162945ef1b41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084652"
---
# <a name="profile-manager-object"></a>Objeto del administrador de perfiles

Un perfil es un conjunto de parámetros multimedia que se usan para crear un archivo ASF. El objeto del administrador de perfiles crea objetos de perfil para su edición. Los objetos de perfil se pueden crear sin ningún dato en ellos o se pueden crear a partir de datos de perfil existentes. El objeto del administrador de perfiles también proporciona métodos para enumerar códecs admitidos y consultar esos códecs para obtener información.

La función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) crea el objeto del administrador de perfiles, que establece un puntero a una [**interfaz IWMProfileManager.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) Las demás interfaces del objeto del administrador de perfiles se pueden obtener llamando al **método QueryInterface.**

El objeto del administrador de perfiles admite las interfaces siguientes.



| Interfaz                                                      | Descripción                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | Recupera información sobre los códecs admitidos y sus formatos.                                                                              |
| [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | Recupera los nombres de los códecs admitidos y las descripciones de sus formatos. Hereda todos los métodos de **IWMCodecInfo**.          |
| [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | Recupera las propiedades del códec y consulta los códecs para las características admitidas. Hereda todos los métodos de **IWMCodecInfo** **e IWMCodecInfo2**. |
| [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | Crea nuevos perfiles, carga perfiles existentes y guarda perfiles personalizados.                                                                    |
| [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | Controla la versión de los perfiles del sistema enumeradas por el administrador de perfiles. Hereda todos los métodos de **IWMProfileManager**.             |
| [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | Controla el idioma de los perfiles del sistema que analiza el administrador de perfiles.                                                                  |



 

## <a name="remarks"></a>Comentarios

Cuando se crea un objeto de administrador de perfiles, analiza todos los perfiles del sistema, lo que puede tardar varios segundos. La creación y publicación de un administrador de perfiles cada vez que necesite usarlo afectará negativamente al rendimiento. Debe crear un administrador de perfiles una vez en la aplicación y liberarlo solo cuando ya no necesite usarlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto de perfil**](profile-object.md)
</dt> <dt>

[**Perfiles**](profiles.md)
</dt> </dl>

 

 




