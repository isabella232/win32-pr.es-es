---
title: Perfiles del sistema localizados
description: Perfiles del sistema localizados
ms.assetid: 2c218ab4-ecdb-414c-aa42-b71a42e340e5
keywords:
- Windows Media Format SDK, perfiles del sistema
- Advanced Systems Format (ASF), perfiles del sistema
- ASF (formato de sistemas avanzados), perfiles del sistema
- SDK de Windows Media Format, perfiles de sistema localizados
- Advanced Systems Format (ASF), perfiles de sistema localizados
- ASF (formato de sistemas avanzados), perfiles de sistema localizados
- perfiles del sistema, localizados
- perfiles del sistema localizados, lista de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aaeecdf1d1d62d78df18e0ac1c5bffbf39f9778
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077272"
---
# <a name="localized-system-profiles"></a>Perfiles del sistema localizados

En la tabla siguiente se enumeran los archivos de Perfil de sistema localizados que se incluyen con el SDK de Windows Media Format y los lenguajes asociados a cada uno de ellos. Estos archivos se instalan en \[ la \] \\ carpeta SDKRoot WMSDK \\ WMFSDK9 \\ LocalizedProfiles Para tener acceso a un archivo determinado con los métodos **IWMProfileManagerLanguage** , debe moverlo al directorio raíz del sistema junto con los archivos de Perfil de sistema predeterminados.



| Idioma              | Nombre de archivo    |
|-----------------------|--------------|
| Árabe                | WMPrfAra. prx |
| Chino (simplificado)  | WMPrfCHS. prx |
| Chino (tradicional) | WMPrfCHT. prx |
| Checo                 | WMPrfCsy. prx |
| Danés                | WMPrfDan. prx |
| Neerlandés                 | WMPrfNld. prx |
| Finés               | WMPrfFin. prx |
| Francés                | WMPrfFra. prx |
| Alemán                | WMPrfDeu. prx |
| Griego                 | WMPrfEll. prx |
| Hebreo                | WMPrfHeb. prx |
| Húngaro             | WMPrfHun. prx |
| Italiano               | WMPrfIta. prx |
| Japonés              | WMPrfJpn. prx |
| Coreano                | WMPrfKor. prx |
| Noruego             | WMPrfNor. prx |
| Polaco                | WMPrfPlk. prx |
| Portugués – Brasil   | WMPrfPtb. prx |
| Portugués – Portugal | WMPrfPtg. prx |
| Ruso               | WMPrfRus. prx |
| Eslovaco                | WMPrfSky. prx |
| Esloveno             | WMPrfSlv. prx |
| Español               | WMPrfEsp. prx |
| Sueco               | WMPrfSve. prx |
| Turco               | WMPrfTrk. prx |



 

Puede establecer el idioma del objeto de administrador de perfiles llamando al método [**IWMProfileManagerLanguage:: SetUserLanguageID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanagerlanguage-setuserlanguageid) . Para la mayoría de los lenguajes, solo se examina el identificador de idioma principal del LANGID. Las excepciones son para los idiomas chino y portugués, donde también se utiliza el identificador de idioma secundario. En la tabla siguiente se muestra cómo crear un LANGID para especificar en el método **SetUserLanguageID** .



| Idioma principal-secundario | MAKELANGID (macro)                                             |
|----------------------------|--------------------------------------------------------------|
| Chino simplificado       | MAKELANGID (LANG \_ chino, sublang \_ chino \_ simplificado)     |
| Chino tradicional      | MAKELANGID (LANG \_ chino, sublang \_ chino \_ Singapur)      |
| Portugués (Brasil)        | MAKELANGID (LANG \_ Portugués, sublang \_ Portugués \_ brasileño) |
| Portugués (Portugal)      | MAKELANGID (LANG \_ Portugués, sublang \_ Portugués)            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](programming-reference.md)
</dt> <dt>

[**Perfiles del sistema**](system-profiles.md)
</dt> </dl>

 

 




