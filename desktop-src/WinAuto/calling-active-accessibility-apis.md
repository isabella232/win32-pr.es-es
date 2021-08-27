---
title: Llamada a Active Accessibility API
description: Microsoft Active Accessibility proporciona interfaces de programación de aplicaciones (API) para clientes y servidores.
ms.assetid: c40441d2-7294-4c76-8b42-08ed66eccb7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6a54bc297af42546a081c3478ef109be137d8af19a37ea39415e8b0d2c06ccc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122245"
---
# <a name="calling-active-accessibility-apis"></a>Llamada a Active Accessibility API

Microsoft Active Accessibility proporciona interfaces de programación de aplicaciones (API) para clientes y servidores. La mayoría se implementan en la biblioteca de vínculos dinámicos de Microsoft Active Accessibility, Oleacc.dll, pero [**NotifyWinEvent,**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)y [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) se implementan en user32.dll, que es un componente básico del sistema operativo Microsoft Windows.

Los equipos que ejecutan Windows 95 o Microsoft Windows NT 4.0 no tienen Oleacc.dll y la versión correcta de user32.dll instalada porque Microsoft Active Accessibility se incorporó en fases en versiones posteriores de Windows. Como resultado, las aplicaciones que se ejecutan en estas plataformas se vinculan explícitamente a Oleacc.dll en tiempo de ejecución mediante la función [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) en lugar de depender de bibliotecas de importación. Active Accessibility 1.3 admite Windows 95 y Microsoft Windows NT 4.0. Las versiones anteriores de Windows no son compatibles con Microsoft Active Accessibility.

Las aplicaciones de servidor usan [**la función GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para recuperar la dirección de una función Microsoft Active Accessibility y, a continuación, realizar la llamada a través de un puntero de función. Si se llama a una función que se implementó en Oleacc.dll, las aplicaciones de servidor usan el identificador devuelto por [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) en la llamada a **GetProcAddress**. Si se llama a una función definida en user32.dll, las aplicaciones de servidor llaman a [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) especificando "USER32" y usan el identificador de módulo devuelto en la llamada a **GetProcAddress**.

Por ejemplo, si una aplicación usa [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), llama a [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) mediante el identificador de módulo de user32.dll para obtener la dirección de la función. Si la llamada se realiza correctamente (lo que significa que esta versión de Windows admite Microsoft Active Accessibility), la aplicación establece una marca que indica que es seguro llamar a **NotifyWinEvent**. La dirección recibida de **GetProcAddress** se almacena en una variable de puntero de función y se usa en todo el código.

 

 