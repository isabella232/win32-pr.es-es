---
description: Atributos ASF
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: Atributos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ccf09542c8b96cc262cbe029111d3cb74e5b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696188"
---
# <a name="asf-attributes"></a>Atributos ASF

### <a name="profile-attributes"></a>Atributos de perfil

Los siguientes atributos se aplican a los perfiles ASF.



| Atributo                                                                      | Descripción                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**MF \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) | Especifica el tamaño de paquete máximo para un archivo ASF, en bytes. |
| [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) | Especifica el tamaño mínimo de paquete para un archivo ASF, en bytes. |



 

### <a name="stream-configuration-attributes"></a>Atributos de configuración de secuencia

Los siguientes atributos se aplican al objeto de configuración de secuencia ASF.



| Atributo                                                                              | Descripción                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) | Establece los parámetros de "cubo de fugas" promedio para codificar un archivo de Windows Media. |
| [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) | Establece los parámetros de límite máximo de "depósito de fugas" para codificar un archivo de Windows Media.    |



 

### <a name="media-buffer-attributes"></a>Atributos de búfer de medios

Los siguientes atributos se aplican a los búferes de medios para los paquetes ASF.



| Atributo                                                                          | Descripción                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_límite de paquetes de MFASFSPLITTER \_**](mfasfsplitter-packet-boundary-attribute.md) | Especifica si un búfer contiene el inicio de un paquete de formato de sistema avanzado (ASF). |



 

### <a name="presentation-descriptor-attributes"></a>Atributos de descriptor de presentación

Para obtener una lista de los atributos que se aplican a los descriptores de presentación ASF, vea [atributos de descriptor de presentación](presentation-descriptor-attributes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



