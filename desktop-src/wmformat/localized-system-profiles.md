---
title: Perfiles del sistema localizados
description: Perfiles del sistema localizados
ms.assetid: 2c218ab4-ecdb-414c-aa42-b71a42e340e5
keywords:
- Windows SDK de formato multimedia, perfiles del sistema
- Formato de sistemas avanzados (ASF), perfiles del sistema
- ASF (formato de sistemas avanzados),perfiles del sistema
- Windows SDK de formato multimedia, perfiles del sistema localizados
- Formato de sistemas avanzados (ASF), perfiles de sistema localizados
- ASF (formato de sistemas avanzados), perfiles de sistema localizados
- perfiles del sistema, localizados
- perfiles del sistema localizados, lista de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aaeecdf1d1d62d78df18e0ac1c5bffbf39f9778
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267055"
---
# <a name="localized-system-profiles"></a>Perfiles del sistema localizados

En la tabla siguiente se enumeran los archivos de perfil del sistema localizados incluidos con Windows SDK de formato multimedia y los idiomas asociados a cada uno. Estos archivos se instalan en la \[ carpeta SDKRoot \] \\ WMSDK \\ WMFSDK9 \\ LocalizedProfiles. Para acceder a un archivo determinado con los métodos **IWMProfileManagerLanguage,** debe moverlo al directorio raíz del sistema junto con los archivos de perfil del sistema predeterminados.



| Idioma              | Nombre de archivo    |
|-----------------------|--------------|
| Árabe                | WMPrfAra.prx |
| Chino simplificado  | WMPrfCHS.prx |
| Chino: tradicional | WMPrfCHT.prx |
| Checo                 | WMPrfCsy.prx |
| Danés                | WMPrfDan.prx |
| Neerlandés                 | WMPrfNld.prx |
| Finés               | WMPrfFin.prx |
| Francés                | WMPrfFra.prx |
| Alemán                | WMPrfDeu.prx |
| Griego                 | WMPrfEll.prx |
| Hebreo                | WMPrfHeb.prx |
| Húngaro             | WMPrfHun.prx |
| Italiano               | WMPrfIta.prx |
| Japonés              | WMPrfMetern.prx |
| Coreano                | WMPrfCore.prx |
| Noruego             | WMPrfNor.prx |
| Polaco                | WMPrfPlk.prx |
| Portugués – Brasil   | WMPrfPtb.prx |
| Portugués – Portugal | WMPrfPtg.prx |
| Ruso               | WMPrfRus.prx |
| Eslovaco                | WMPrfSky.prx |
| Esloveno             | WMPrfSlv.prx |
| Español               | WMPrfEsp.prx |
| Sueco               | WMPrfSve.prx |
| Turco               | WMPrfTrk.prx |



 

Puede establecer el idioma del objeto del administrador de perfiles llamando al método [**IWMProfileManagerLanguage::SetUserLanguageID.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanagerlanguage-setuserlanguageid) Para la mayoría de los idiomas, solo se examina el identificador de idioma principal del LANGID. Las excepciones son para los idiomas chino y portugués, donde también se usa el identificador de idioma secundario. En la tabla siguiente se muestra cómo crear un LANGID para especificarlo en el **método SetUserLanguageID.**



| Idioma principal y secundario | MakeLANGID (Macro)                                             |
|----------------------------|--------------------------------------------------------------|
| Chino simplificado       | MAKELANGID( LANG \_ CHINESE, SUBLANG \_ CHINESE \_ SIMPLIFIED)     |
| Chino tradicional      | MAKELANGID( LANG \_ CHINESE, SUBLANG \_ CHINESE \_ SINGAPORE)      |
| Portugués (Brasil)        | MAKELANGID(LANG \_ PORTUGUÉS, SUBLANG \_ PORTUGUÉS PORTUGUÉS \_ BRASIL) |
| Portugués (Portugal)      | MAKELANGID(LANG \_ PORTUGUÉS, SUBLANG \_ PORTUGUÉS)            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> <dt>

[**Perfiles del sistema**](system-profiles.md)
</dt> </dl>

 

 




