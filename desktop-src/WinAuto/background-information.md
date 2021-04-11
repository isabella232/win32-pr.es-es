---
title: Información general
description: El componente de Microsoft Active Accessibility, oleacc.dll, crea objetos de proxy que implementan IAccessible en nombre de los controles estándar de Windows.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a9b044f8035a474f02b8457dc99ec39aca73c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148777"
---
# <a name="background-information"></a>Información general

El componente de Microsoft Active Accessibility, oleacc.dll, crea objetos de proxy que implementan [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en nombre de los controles estándar de Windows. Dado que estos proxies usan mensajes estándar de Windows y API específicas del control para recopilar información sobre cada control, no se ha producido ningún mecanismo directo para personalizar la información que estos proxies exponen a través de **IAccessible**.

Actualmente, puede personalizar una implementación de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existente mediante técnicas de subclase y ajuste. Sin embargo, estas técnicas son tediosas y propensas a errores. De hecho, la mayor parte del código escrito para invalidar una o dos propiedades está relacionada con la implementación de subclases y ajuste. solo una pequeña fracción realiza la tarea real de invalidar la información. La anotación dinámica mejora la situación al proporcionar funcionalidades similares sin necesidad de escribir código de subestado o de ajuste. En su lugar, puede centrarse en proporcionar código que proporcione la información correcta. La anotación dinámica permite a los desarrolladores pasar sugerencias y otra información útil a OLEACC para personalizar la información que expone. Esta capacidad solo reducirá el costo del soporte técnico de Microsoft Active Accessibility y permitirá a los desarrolladores mejorar considerablemente la accesibilidad de sus interfaces de usuario.

 

 




