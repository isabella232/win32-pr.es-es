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
ms.openlocfilehash: 051e95bfb3f5ef8e39af31368227cf4918b897d2
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149084"
---
# <a name="using-custom-mutual-exclusion-types"></a>Usar tipos de exclusión mutua personalizados

Puede usar objetos de exclusión mutua en un perfil para satisfacer las necesidades de escenarios personalizados. Al pasar el valor de GUID \_ WMMUTEX \_ Unknown a [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), se informa al objeto de exclusión mutua de que se está usando un escenario personalizado.

Debe controlar manualmente la selección de flujos cuando lee un archivo con un valor de exclusión mutua personalizado. El objeto de lector usará la primera secuencia que agregue a la exclusión mutua como valor predeterminado.

Use los pasos siguientes para crear un objeto de exclusión mutua personalizado y agregarlo a un perfil:

1.  Cree un administrador de perfiles mediante una llamada a la función [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Comience con un perfil existente o cree uno totalmente nuevo.
    -   Si usa un perfil existente, llame a uno de los métodos Load de la interfaz [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . Después, vaya al paso 4.
    -   Si va a crear un perfil completamente nuevo, llame a [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).
3.  Agregue secuencias al nuevo perfil llamando a [**IWMProfile:: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream). Configure las secuencias según sea necesario mediante los métodos de [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig). También puede llamar a **QueryInterface** para tener acceso a otras interfaces en el objeto de configuración de la secuencia.

    **CreateNewStream** solo crea un objeto de configuración de flujo y no afecta al perfil. Después de configurar correctamente un flujo, debe llamar a [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) para agregar la secuencia al perfil.

4.  Cree un objeto de exclusión mutua mediante una llamada a [**IWMProfile:: CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).
5.  Agregue las secuencias deseadas al objeto de exclusión mutua mediante una llamada a [**IWMStreamList:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (disponible directamente desde [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), que hereda de [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).
6.  Establezca el tipo de exclusión mutua en personalizado mediante una llamada a [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype). Pase el CLSID \_ WMMUTEX \_ desconocido como el GUID de tipo.
7.  Agregue el objeto de exclusión mutua configurado al perfil mediante una llamada a [**IWMProfile:: AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**Interfaz IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interfaz IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Interfaz IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[**Interfaz IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[**Usar exclusión mutua**](using-mutual-exclusion.md)
</dt> <dt>

[**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




