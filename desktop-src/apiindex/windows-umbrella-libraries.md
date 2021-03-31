---
description: Una biblioteca de paraguas es una biblioteca de vínculos estáticos única que exporta un subconjunto de las API de Win32. Por ejemplo, un lib de paraguas denominado OneCore. lib proporciona las exportaciones para el subconjunto de las API de Win32 que son comunes a todos los dispositivos de Windows 10.
ms.assetid: A323B5D1-3235-4BBA-96BF-A7DFEBB85C89
title: Bibliotecas de paraguas de Windows
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 86a8f9b8f3bef5081bd7e0e64300b9295fd85401
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/24/2020
ms.locfileid: "103797236"
---
# <a name="windows-umbrella-libraries"></a>Bibliotecas de paraguas de Windows

Una *biblioteca de paraguas* es una biblioteca de vínculos estáticos única que exporta un subconjunto de las API de Win32. Por ejemplo, una biblioteca de paraguas denominada **OneCore. lib** proporciona las exportaciones para el subconjunto de las API de Win32 que son comunes a todos los dispositivos de Windows 10.

Las API de una biblioteca paraguas se pueden implementar en un intervalo de módulos (ya sea un [conjunto de API](windows-apisets.md) o un archivo dll), pero la biblioteca de paraguas abstrae ese detalle, lo que hace que la aplicación sea más portátil en las distintas versiones del sistema operativo. Simplemente vincule la aplicación o el controlador de escritorio con la biblioteca de paraguas que contiene el conjunto de API que le interesa, y eso es todo lo que necesita hacer. 

| Biblioteca | Descripción |
|------------------------|-------------------------|
| OneCore. lib | Esta biblioteca proporciona las exportaciones para el subconjunto de las API de Win32 que son comunes a todos los dispositivos de Windows 10. Vincule la aplicación o el controlador de escritorio con OneCore. lib (y ninguna otra biblioteca) para tener acceso a estas API. Si vincula la aplicación o el controlador a OneCore. lib y solo llama a las API de Win32 en esa biblioteca, la aplicación o el controlador se cargarán correctamente en todos los dispositivos de Windows 10.         |
| OneCore_apiset. lib | Esta biblioteca proporciona la misma cobertura que OneCore. lib, pero utiliza el [reenvío directo de conjunto de API](api-set-loader-operation.md#direct-forwarding). Tenga en cuenta que el uso de esta biblioteca solo será compatible con la versión de Windows 10, tal como se especifica en la versión del SDK de destino, o superior.  |
| OneCoreUap. lib | Esta biblioteca proporciona las exportaciones para el subconjunto de las API de Win32 que son comunes a todos los dispositivos de Windows 10 que admiten el Windows Runtime (WinRT). Vincule la aplicación o el controlador de escritorio con OneCoreUap. lib (y ninguna otra biblioteca) para tener acceso a estas API. Si vincula la aplicación o el controlador a OneCoreUap. lib y solo llama a las API de Win32 en esa biblioteca, la aplicación o el controlador se cargarán correctamente en todos los dispositivos de Windows 10 que admitan UWP. |
| OneCoreUAP_apiset. lib | Esta biblioteca proporciona la misma cobertura que OneCoreUAP. lib, pero usa la técnica de [reenvío directo de conjunto de API](api-set-loader-operation.md#direct-forwarding) . Tenga en cuenta que el uso de esta biblioteca solo será compatible con la versión de Windows 10, tal como se especifica en el SDK al que está destinada, o superior.  |
