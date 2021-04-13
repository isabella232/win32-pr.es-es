---
title: Acerca de la API de procesamiento de imágenes
description: Esta documentación se centra en una descripción de la implementación de Adapteci para Microsoft (IMAPIv1).
ms.assetid: 596ec3ea-17d1-4e60-8789-528ff00ae421
keywords:
- API de patrón de imágenes IMAPi, descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db1dc7846d2e47483abf2ca8856d593b874467f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104559697"
---
# <a name="about-the-image-mastering-api"></a>Acerca de la API de procesamiento de imágenes

Esta documentación se centra en una descripción de la implementación de Adapteci para Microsoft (IMAPIv1). Como tal, en este documento se incluyen las descripciones de los cuatro objetos COM principales y sus interfaces. Los cuatro objetos principales son los siguientes: **MSDiscMasterObj**, **MSDiscRecorderObj**, **MSDiscStashObj** y **MSBurnEngineObj**.

Puede haber varios objetos **MSDiscMasterObj** con instancias en un sistema, pero solo una aplicación puede acceder a la grabadora a la vez. **MSDiscMasterObj** implementa varias interfaces, tal y como se muestra en el siguiente diagrama de objetos.

![msdiscmasterobj implementa varias interfaces](images/imapi.png)

Las aplicaciones usan la interfaz [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) para realizar las siguientes tareas:

-   Abrir IMAPi
-   Enumerar formatos admitidos (Joliet y Redbook)
-   Seleccionar un formato
-   Obtener una lista de registros
-   Selección de una grabadora
-   Iniciar una grabación

Las interfaces [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) y [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) se devuelven a una aplicación a través de la interfaz [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) cuando se selecciona un formato. Estas interfaces controlan el contenido de un disco de datos o de audio, respectivamente. No se espera que todas las aplicaciones comprendan las interfaces de formato específicas. Las aplicaciones pueden tener acceso a las propiedades genéricas de la interfaz **IJolietDiscMaster** , como el nombre del volumen o el nombre del archivo heredado.

Se tiene acceso a los objetos **MSDiscRecorderObj** a través de la interfaz [**IDiscRecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) . Cada dispositivo CD-R o CD-RW compatible con IMAPi tiene un objeto **MSDiscRecorderObj** correspondiente. Una aplicación utiliza punteros a la interfaz **IDiscRecorder** en esos objetos para seleccionar qué dispositivo va a usar IMAPI para grabar un CD. Además, las aplicaciones pueden tener acceso a las propiedades genéricas de una grabadora a través de **IDiscRecorder**. Esto incluye propiedades como la velocidad del escritor u otros parámetros de grabación.

Los objetos restantes, **MSDiscStashObj** y **MSBurnEngineObj**, son objetos internos a los que tiene acceso IMAPI. Se mencionan aquí solo para aclarar la arquitectura de IMAPi. **MSDiscStashObj** representa (a través de la interfaz **IDiscStash** ) un archivo sin formato de hasta 800 MB de tamaño que usa **MSDiscMasterObj** para crear imágenes de audio o discos de datos que se van a grabar. El sistema intermedio se pasa a **MSBurnEngineObj** (a través de la interfaz **IMSBurnEngine** ) cuando se solicita una grabación desde el motor de nivel inferior. El objeto **MSBurnEngineObj** espera que el contenido de los contenidos provisionales esté en un formato conocido. En este sentido, **MSDiscMasterObj** y **MSBurnEngineObj** tienen un contrato con respecto al contenido del contenido provisional.

 

 




