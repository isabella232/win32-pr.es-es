---
title: Configuración común a todas las Secuencias
description: Configuración común a todas las Secuencias
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- profiles,configurations common to all streams
- streams,common configurations
- streams,names
- streams,connection names
- streams,numbers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1a398256da99092da45e83ebc91de713f9ab71
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571269"
---
# <a name="configuration-common-to-all-streams"></a>Configuración común a todas las Secuencias

A todas las secuencias, independientemente del tipo, se les debe asignar un nombre de secuencia, un nombre de conexión y un número de secuencia.

El nombre del flujo es simplemente un nombre descriptivo que se asigna a la secuencia. No es necesario que una secuencia tenga un nombre de secuencia, pero le ayuda a identificar la secuencia al editar el perfil más adelante. Puede establecer un nombre para la secuencia llamando a [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).

Cada secuencia debe tener un nombre de conexión, también denominado nombre de entrada. Al establecer el perfil en el objeto de escritor para escribir un archivo, el escritor asociará cada nombre de conexión a una entrada. Para identificar las entradas, debe llamar a [**IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) para recuperar el nombre de conexión. Los nombres de conexión típicos son descripciones sencillas del contenido, como "audio". Si el perfil contiene secuencias que se excluyen mutuamente por velocidad de bits, cada una de las secuencias mutuamente excluyentes debe tener el mismo nombre de conexión. Si no es así, el perfil no es válido y el escritor lo rechazará. Puede establecer un nombre de conexión llamando a [**IWMStreamConfig::SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).

El número de secuencia identifica la secuencia dentro del archivo. A diferencia de los números de entrada y de salida, los números de flujo comienzan en 1, no en 0. Un número de flujo es diferente de un índice de secuencia, que se usa al obtener secuencias en un perfil mediante [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream). El índice de secuencia es un número asignado a la secuencia por el objeto de perfil. Los índices de flujo oscilan entre 0 y uno menos que el número de secuencias recuperadas por [**IWMProfile::GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount). Los números de secuencia no deben ser secuenciales, aunque suelen ser y pueden oscilar entre 1 y 63. Puede establecer un número de secuencia llamando a [**IWMStreamConfig::SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> <dt>

[**Entradas, Secuencias salidas**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




