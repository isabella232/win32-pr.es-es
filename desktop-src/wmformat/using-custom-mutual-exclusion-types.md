---
title: Usar tipos de exclusión mutua personalizados
description: Usar tipos de exclusión mutua personalizados
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- IWMMutualExclusion
- exclusión mutua, interfaz IWMMutualExclusion
- exclusión mutua, tipos personalizados
- perfiles, tipos de exclusión mutua personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7162b8d0588031e934e55425af03cd0d2e8d0a58524b19251521ec2ab6848094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845083"
---
# <a name="using-custom-mutual-exclusion-types"></a>Usar tipos de exclusión mutua personalizados

Puede usar objetos de exclusión mutua en un perfil para satisfacer las necesidades de escenarios personalizados. Al pasar el valor DE GUID CLSID \_ WMMUTEX \_ Unknown to [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), se informa al objeto de exclusión mutua de que se usa un escenario personalizado.

Debe controlar manualmente la selección de secuencias al leer un archivo con un valor de exclusión mutua personalizado. El objeto lector usará la primera secuencia que agregue a la exclusión mutua como valor predeterminado.

Siga estos pasos para crear un objeto de exclusión mutua personalizado y agregarlo a un perfil:

1.  Cree un administrador de perfiles mediante una llamada a [**la función WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
2.  Comience con un perfil existente o cree uno completamente nuevo.
    -   Si usa un perfil existente, llame a uno de los métodos de carga de la [**interfaz IWMProfileManager.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) A continuación, vaya al paso 4.
    -   Si va a crear un perfil completamente nuevo, llame a [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).
3.  Agregue secuencias al nuevo perfil mediante una llamada [**a IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream). Configure las secuencias según sea necesario mediante los métodos [**de IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig). También puede llamar a **QueryInterface para acceder** a otras interfaces en el objeto de configuración de flujo.

    **CreateNewStream** crea solo un objeto de configuración de flujo y no afecta al perfil. Una vez configurada correctamente una secuencia, debe llamar a [**IWMProfile::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) para agregar la secuencia al perfil.

4.  Cree un objeto de exclusión mutua llamando [**a IWMProfile::CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).
5.  Agregue las secuencias deseadas al objeto de exclusión mutua llamando a [**IWMStreamList::AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (disponible directamente desde [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), que hereda de [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).
6.  Establezca el tipo de exclusión mutua en personalizado mediante una [**llamada a IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype). Pase CLSID \_ WMMUTEX \_ Unknown como GUID de tipo.
7.  Agregue el objeto de exclusión mutua configurado al perfil mediante una llamada [**a IWMProfile::AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**IWMProfile (interfaz)**](iwmprofile.md)
</dt> <dt>

[**IWMProfileManager (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Interfaz IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[**IWMStreamList (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[**Uso de la exclusión mutua**](using-mutual-exclusion.md)
</dt> <dt>

[**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




