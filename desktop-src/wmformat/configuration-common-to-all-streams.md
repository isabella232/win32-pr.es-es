---
title: Configuración común para todos los flujos
description: Configuración común para todos los flujos
ms.assetid: 63e655b7-a4ef-4580-a0f3-03cedd2cbf9a
keywords:
- perfiles, configuraciones comunes a todos los flujos
- flujos, configuraciones comunes
- flujos, nombres
- flujos, nombres de conexión
- secuencias, números
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1a398256da99092da45e83ebc91de713f9ab71
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "104420475"
---
# <a name="configuration-common-to-all-streams"></a>Configuración común para todos los flujos

A todas las secuencias, independientemente del tipo, se les debe asignar un nombre de flujo, un nombre de conexión y un número de secuencia.

El nombre del flujo es simplemente un nombre descriptivo que se asigna a la secuencia. No es necesario que una secuencia tenga un nombre de flujo, pero ayuda a identificar la secuencia al editar el perfil en un momento posterior. Puede establecer un nombre para la secuencia mediante una llamada a [**IWMStreamConfig:: SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname).

Cada secuencia debe tener un nombre de conexión, también denominado nombre de entrada. Al establecer el perfil en el objeto de escritor para escribir un archivo, el escritor asociará cada nombre de conexión con una entrada. Para identificar las entradas, debe llamar a [**IWMInputMediaProps:: GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname) para recuperar el nombre de la conexión. Los nombres de conexión típicos son descripciones simples del contenido, como "audio". Si el perfil contiene secuencias que se excluyen mutuamente mediante la velocidad de bits, cada una de las secuencias mutuamente excluyentes debe tener el mismo nombre de conexión. Si no es así, el perfil no es válido y el escritor lo rechazará. Puede establecer un nombre de conexión llamando a [**IWMStreamConfig:: SetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname).

El número de secuencia identifica la secuencia dentro del archivo. A diferencia de los números de entrada y de salida, los números de flujo comienzan en 1, no en 0. Un número de secuencia es diferente de un índice de flujo, que se usa al obtener secuencias en un perfil mediante [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream). El índice de la secuencia es un número asignado a la secuencia por el objeto de perfil. Los índices de secuencia oscilan entre 0 y uno menos que el número de flujos recuperados por [**IWMProfile:: GetStreamCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount). Los números de secuencia no deben ser secuenciales, aunque normalmente son, y pueden oscilar entre 1 y 63. Puede establecer un número de secuencia mediante una llamada a [**IWMStreamConfig:: SetStreamNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamnumber).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de secuencias**](configuring-streams.md)
</dt> <dt>

[**Entradas, secuencias y salidas**](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




