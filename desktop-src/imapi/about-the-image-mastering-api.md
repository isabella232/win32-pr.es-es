---
title: Acerca de Image Mastering API
description: Esta documentación se centra en una descripción de la implementación adaptec de IMAPI para Microsoft (IMAPIv1).
ms.assetid: 596ec3ea-17d1-4e60-8789-528ff00ae421
keywords:
- Image Mastering API IMAPI ,described
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb16ab8c542e7c4686c7a3f4d027169a520495a8d3fab9927f11ed974deeef6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451914"
---
# <a name="about-the-image-mastering-api"></a>Acerca de Image Mastering API

Esta documentación se centra en una descripción de la implementación adaptec de IMAPI para Microsoft (IMAPIv1). Por lo tanto, en este documento se incluyen descripciones de los cuatro objetos COM principales y sus interfaces. Los cuatro objetos principales son los siguientes: **MSDiscMasterObj,** **MSDiscRecorderObj,** **MSDiscStashObj** y **MSEngineEngineObj**.

Puede haber varias instancias **de objetos MSDiscMasterObj** en un sistema, pero solo una aplicación puede acceder a una grabadora a la vez. **MSDiscMasterObj implementa** varias interfaces, como se muestra en el siguiente diagrama de objetos.

![msdiscmasterobj implementa varias interfaces](images/imapi.png)

Las aplicaciones usan [**la interfaz IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) para realizar las siguientes tareas:

-   Apertura de IMAPI
-   Enumerar los formatos admitidos (Joliet y Redbook)
-   Selección de un formato
-   Obtener una lista de grabadoras
-   Selección de una grabadora
-   Iniciar una grabación

Las [**interfaces IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) e [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) se devuelven a una aplicación a través de la interfaz [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) cuando se selecciona un formato. Estas interfaces controlan el contenido de un disco de datos o audio, respectivamente. No se espera que todas las aplicaciones comprendan las interfaces de formato específicas. Las aplicaciones pueden acceder a propiedades genéricas de **la interfaz IJolietDiscMaster,** como el nombre del volumen o el nombre de archivo heredado.

Se accede a los objetos **MSDiscRecorderObj** a través de la [**interfaz IDiscRecorder.**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) Cada dispositivo CD-R o CD-RW compatible con IMAPI tiene un objeto **MSDiscRecorderObj** correspondiente. Una aplicación usa punteros a la **interfaz IDiscRecorder** en esos objetos para seleccionar qué dispositivo usará IMAPI para grabar un CD. Además, las aplicaciones pueden acceder a las propiedades genéricas de una grabadora a través **de IDiscRecorder**. Esto incluye propiedades como la velocidad del escritor u otros parámetros de grabación.

Los objetos restantes, **MSDiscStashObj** y **MSEngineEngineObj**, son objetos internos a los que accede IMAPI. Aquí solo se mencionan para aclarar la arquitectura IMAPI. **MSDiscStashObj** representa (a través de la interfaz **IDiscStash)** un archivo sin formato de hasta 800 MB de tamaño que **MSDiscMasterObj** usa para crear imágenes de audio o discos de datos que se va a grabar. El stash se pasa a **MSEngineObj** (a través de la interfaz **IMSEngine)** cuando se solicita una grabación desde el motor de nivel inferior. El **objeto MSEngineObj** espera que el contenido del stash esté en un formato conocido. En este sentido, **MSDiscMasterObj** y **MSEngineEngineObj** tienen un contrato con respecto al contenido del stash.

 

 




