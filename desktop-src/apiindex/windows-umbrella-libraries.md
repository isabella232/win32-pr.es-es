---
description: Una biblioteca de paraguas es una sola biblioteca de vínculos estáticos que exporta un subconjunto de API de Win32. Por ejemplo, una biblioteca paraguas denominada OneCore.lib proporciona las exportaciones para el subconjunto de API de Win32 que son comunes a todos los Windows 10 dispositivos.
ms.assetid: A323B5D1-3235-4BBA-96BF-A7DFEBB85C89
title: Bibliotecas de paraguas de Windows
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 8714f7054e11e488c61a01fd3f010faaae8c1403efdce6727e88dc26a9d5f133
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737622"
---
# <a name="windows-umbrella-libraries"></a>Bibliotecas de paraguas de Windows

Una *biblioteca de paraguas* es una sola biblioteca de vínculos estáticos que exporta un subconjunto de API de Win32. Por ejemplo, una biblioteca de paraguas denominada **OneCore.lib** proporciona las exportaciones para el subconjunto de API de Win32 que son comunes a todos los Windows 10 dispositivos.

Las API de una biblioteca de paraguas se pueden implementar en una variedad de módulos (ya sea un conjunto de [API](windows-apisets.md) o un archivo DLL), pero la biblioteca paraguas abstrae ese detalle de usted, lo que hace que la aplicación sea más portátil en las versiones del sistema operativo. Simplemente vincule la aplicación de escritorio o el controlador con la biblioteca de paraguas que contiene el conjunto de API que le interesan, y eso es todo lo que necesita hacer. 

| Biblioteca | Descripción |
|------------------------|-------------------------|
| OneCore.lib | Esta biblioteca proporciona las exportaciones para el subconjunto de API de Win32 que son comunes a todos los Windows 10 dispositivos. Vincule la aplicación de escritorio o el controlador con OneCore.lib (y ninguna otra biblioteca) para acceder a estas API. Si vincula la aplicación o el controlador a OneCore.lib y solo llama a las API de Win32 en esa biblioteca, la aplicación o el controlador se cargarán correctamente en todos los dispositivos Windows 10.         |
| OneCore_apiset.lib | Esta biblioteca proporciona la misma cobertura que OneCore.lib, pero usa el [reenvío directo del conjunto de API.](api-set-loader-operation.md#direct-forwarding) Tenga en cuenta que el uso de esta biblioteca solo será compatible con la versión Windows 10 especificada por la versión del SDK de destino o superior.  |
| OneCoreUap.lib | Esta biblioteca proporciona las exportaciones para el subconjunto de API de Win32 que son comunes a todos los dispositivos Windows 10 que admiten Windows Runtime (WinRT). Vincule la aplicación de escritorio o el controlador con OneCoreUap.lib (y ninguna otra biblioteca) para acceder a estas API. Si vincula la aplicación o el controlador a OneCoreUap.lib y solo llama a las API de Win32 en esa biblioteca, la aplicación o el controlador se cargarán correctamente en todos los dispositivos Windows 10 compatibles con UWP. |
| OneCoreUAP_apiset.lib | Esta biblioteca proporciona la misma cobertura que OneCoreUAP.lib, pero usa la técnica de [reenvío directo del conjunto de API.](api-set-loader-operation.md#direct-forwarding) Tenga en cuenta que el uso de esta biblioteca solo será compatible con la versión Windows 10 especificada por el SDK de destino o superior.  |
