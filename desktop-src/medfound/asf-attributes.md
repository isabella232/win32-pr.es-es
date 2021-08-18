---
description: Atributos de ASF
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: Atributos de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babbb8697126ae6882c11526ed9e6cb31e2233b81685c820d200fbd21bab08c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975034"
---
# <a name="asf-attributes"></a>Atributos de ASF

### <a name="profile-attributes"></a>Atributos de perfil

Los atributos siguientes se aplican a los perfiles de ASF.



| Atributo                                                                      | Descripción                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**MF \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) | Especifica el tamaño máximo de paquete para un archivo ASF, en bytes. |
| [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) | Especifica el tamaño mínimo del paquete para un archivo ASF, en bytes. |



 

### <a name="stream-configuration-attributes"></a>Atributos de configuración de flujo

Los atributos siguientes se aplican al objeto de configuración de flujo de ASF.



| Atributo                                                                              | Descripción                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) | Establece el promedio de parámetros de "depósito filtrado" para codificar un Windows archivo multimedia. |
| [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) | Establece los parámetros máximos del "cubo de fugas" para codificar un Windows archivo multimedia.    |



 

### <a name="media-buffer-attributes"></a>Atributos de búfer multimedia

Los atributos siguientes se aplican a los búferes multimedia para los paquetes ASF.



| Atributo                                                                          | Descripción                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**LÍMITE DE PAQUETES MFASFSPLITTER \_ \_**](mfasfsplitter-packet-boundary-attribute.md) | Especifica si un búfer contiene el inicio de un paquete de formato de sistemas avanzados (ASF). |



 

### <a name="presentation-descriptor-attributes"></a>Atributos del descriptor de presentación

Para obtener una lista de los atributos que se aplican a los descriptores de presentación de ASF, vea [Atributos del descriptor de presentación](presentation-descriptor-attributes.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 



