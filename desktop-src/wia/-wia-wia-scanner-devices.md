---
description: El Windows escáner de adquisición de imágenes (WIA) se implementa como un árbol jerárquico de objetos IWiaItem.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: Dispositivos de wia scanner en WIA 1.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd22cc9fe330a3acf231034b61c72178f3b282cb9e66a1f455d4b6939a1c3cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592684"
---
# <a name="wia-scanner-devices-in-wia-10"></a>Dispositivos de wia scanner en WIA 1.0

> [!Note]  
> En este tema se describe el árbol de dispositivos del analizador para las aplicaciones que usan el servicio de adquisición de imágenes de Windows (WIA) 1.0 (que se admite en Windows XP o versiones anteriores). Para obtener información sobre el árbol de dispositivos de los elementos de Windows Image Acquisition (WIA) 2.0 (que se admiten en Windows Vista o versiones posteriores), vea [About the IWiaItem2 Item Tree](-wia-about-item-tree.md).

 

El Windows escáner de adquisición de imágenes (WIA) se implementa como un árbol jerárquico de [**objetos IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) Desde el elemento raíz, una aplicación puede:

-   Funcionalidades del analizador de consultas
-   Establecimiento de las propiedades del dispositivo del analizador
-   Control del feeder de documentos

Un dispositivo de escáner WIA es diferente de un dispositivo de cámara WIA porque, en general, no almacena varias imágenes en memoria.

Debajo del elemento raíz, un objeto de escáner típico tiene un único objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) que representa la funcionalidad de recopilación de datos del dispositivo, el elemento scan. Este elemento tiene la [**marca WiaItemTypeFile**](-wia-wia-item-type-flags.md) establecida para indicar que las transferencias de datos en este elemento son posibles. Una aplicación configura un examen estableciendo las propiedades del elemento de examen y, a continuación, realiza el examen y transfiere los datos mediante una interfaz de transferencia de datos.

En el diagrama siguiente se muestra la implementación de WIA para un escáner típico:

![wia implementación de un escáner típico](images/wiscantr.gif)

Un escáner dúplex típico se representa en WIA con un [**objeto IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) Se accede a los datos de front-and-back-page secuencialmente una transferencia de datos por página. Por lo tanto, la representación de un escáner dúplex es idéntica a la representación de un escáner típico.

Un escáner de diapositivas capaz de examinar varias diapositivas en una sola operación de examen representa cada imagen independiente como un [**objeto IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) independiente.

En el diagrama siguiente se muestra la representación de WIA de un escáner de diapositivas:

![escáner de diapositivas](images/wislscan.gif)

 

 



