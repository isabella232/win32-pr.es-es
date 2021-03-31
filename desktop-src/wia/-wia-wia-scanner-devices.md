---
description: El dispositivo de analizador de adquisición de imágenes de Windows (WIA) se implementa como un árbol jerárquico de objetos IWiaItem.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: Dispositivos WIA Scanner en WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443277b0b580a481b523739cd5bc21642d827252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809968"
---
# <a name="wia-scanner-devices-in-wia-10"></a>Dispositivos WIA Scanner en WIA 1,0

> [!Note]  
> En este tema se describe el árbol de dispositivos del escáner para las aplicaciones que usan el servicio de adquisición de imágenes de Windows (WIA) 1,0 (que es compatible con Windows XP o versiones anteriores). Para obtener información sobre el árbol de dispositivos de elementos de adquisición de imágenes de Windows (WIA) 2,0 (que son compatibles con Windows Vista o versiones posteriores), consulte [acerca del árbol de elementos IWiaItem2](-wia-about-item-tree.md).

 

El dispositivo de analizador de adquisición de imágenes de Windows (WIA) se implementa como un árbol jerárquico de objetos [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . En el elemento raíz, una aplicación puede:

-   Capacidades del analizador de consultas
-   Establecer propiedades de dispositivo de escáner
-   Controlar el alimentador de documentos

Un dispositivo WIA Scanner es diferente de un dispositivo de cámara WIA porque, en general, no almacena varias imágenes en la memoria.

Debajo del elemento raíz, un objeto Scanner típico tiene un objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) único que representa la funcionalidad de recopilación de datos del dispositivo, el elemento de examen. Este elemento tiene la marca [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) establecida para indicar que las transferencias de datos en este elemento son posibles. Una aplicación configura un examen mediante el establecimiento de las propiedades del elemento de análisis y, a continuación, realiza el análisis y transfiere los datos mediante una interfaz de transferencia de datos.

En el diagrama siguiente se ilustra la implementación de WIA para un escáner típico:

![implementación de WIA de un escáner típico](images/wiscantr.gif)

Un escáner dúplex normal se representa en WIA con un objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) . Se tiene acceso a los datos de la página frontal y posterior secuencialmente una transferencia de datos por página. Por lo tanto, la representación de un escáner dúplex es idéntica a la representación de un escáner típico.

Un escáner de diapositivas capaz de digitalizar varias diapositivas en una sola operación de examen representa cada imagen independiente como un objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) independiente.

En el diagrama siguiente se muestra la representación de WIA de un escáner de diapositivas:

![escáner de diapositivas](images/wislscan.gif)

 

 



