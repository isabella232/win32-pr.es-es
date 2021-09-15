---
description: Procesamiento de códecs DMO entrada y salida
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: Procesamiento de códecs DMO entrada y salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c6781d877f4c863161537fcc5b6a746691cfe1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474035"
---
# <a name="processing-codec-dmo-input-and-output"></a>Procesamiento de códecs DMO entrada y salida

Cuando haya configurado el tipo de entrada y el tipo de salida para un DMO, puede empezar a procesar ejemplos de datos. Se pasan ejemplos al DMO para su procesamiento mediante el método **IMediaObject::P rocessInput** y, a continuación, se recupera el ejemplo procesado llamando a **IMediaObject::P rocessOutput**. Debe establecer marcas de tiempo y duraciones precisas para todas las muestras de entrada pasadas. Las marcas de tiempo no son estrictamente necesarias, pero ayudan a mantener la sincronización de audio y vídeo. Si no tiene las marcas de tiempo de los ejemplos, es mejor dejarlos fuera que usar valores no seguros.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con DDO de códec](workingwithcodecdmos.md)
</dt> </dl>

 

 



