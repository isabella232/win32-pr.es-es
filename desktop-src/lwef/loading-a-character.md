---
title: Cargar un carácter
description: Cargar un carácter
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3590698040f40f8fbf0964177e12ba6ed253c37d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775913"
---
# <a name="loading-a-character"></a>Cargar un carácter

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Para animar un carácter, primero debe cargar el carácter. Use el método [**Load**](load-method.md) para cargar los datos del carácter. El agente de Microsoft admite dos formatos de datos de caracteres y de animación: un único archivo estructurado y archivos independientes. Normalmente, se usa el formato de archivo único (. ACS) cuando los datos se almacenan de forma local. El formato de varios archivos (. ACF,. ACA) funciona mejor cuando desea descargar animaciones de forma individual, por ejemplo, al tener acceso a animaciones desde un servidor HTTP.

Una aplicación cliente puede cargar una sola instancia del mismo carácter. Cualquier intento de cargar el mismo carácter más de una vez producirá un error. Sin embargo, una aplicación puede tener varias instancias del mismo carácter cargadas proporcionando conexiones independientes al agente de Microsoft. Por ejemplo, una aplicación podría cargar el mismo carácter de dos copias del control Microsoft Agent.

También puede definir sus propios caracteres para su uso con Microsoft Agent. Puede usar cualquier herramienta de representación que prefiera para crear las imágenes, siempre y cuando acabe con los archivos de formato de mapa de bits de Windows. Para ensamblar y compilar las imágenes de un carácter en animaciones para su uso con el agente de Microsoft, use el editor de caracteres del agente de Microsoft. Esta herramienta permite definir las propiedades predeterminadas de un carácter, así como definir animaciones para el carácter. El editor de caracteres del agente de Microsoft también permite seleccionar el formato de archivo adecuado al crear un carácter.

 

 




