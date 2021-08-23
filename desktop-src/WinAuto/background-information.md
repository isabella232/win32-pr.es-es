---
title: Información general
description: El Microsoft Active Accessibility, oleacc.dll, crea objetos proxy que implementan IAccessible en nombre de los controles Windows estándar.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d154beb5d824bc722e713346129258c2d294d678a92c1b66d12035ce390f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052963"
---
# <a name="background-information"></a>Información general

El Microsoft Active Accessibility, oleacc.dll, crea objetos proxy que implementan [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en nombre de los controles Windows estándar. Dado que estos servidores proxy usan mensajes Windows estándar y API específicas del control para recopilar información sobre cada control, no ha habido ningún mecanismo directo para personalizar la información que estos servidores proxy exponen a través de **IAccessible.**

Actualmente, puede personalizar una implementación existente de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) mediante técnicas de subclases y ajuste. Sin embargo, estas técnicas son tediosas y propensas a errores. De hecho, la mayoría del código escrito para invalidar una o dos propiedades se refiere a la implementación de subclases y ajuste; solo una fracción pequeña lleva a cabo la tarea real de invalidar la información. Anotación dinámica mejora la situación al proporcionar funcionalidades similares sin necesidad de escribir subclases ni ajustar código. En su lugar, puede centrarse en proporcionar código que proporcione la información correcta. La anotación dinámica permite a los desarrolladores pasar sugerencias y otra información útil a OLEACC para personalizar la información que expone. Esta funcionalidad por sí sola reducirá el costo de admitir Microsoft Active Accessibility y permitirá a los desarrolladores mejorar considerablemente la accesibilidad de sus interfaces de usuario.

 

 




