---
title: Cargar un carácter
description: Cargar un carácter
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78d796df5c1699b405e8cae1dbae0e7d7d8d37932aa50534fa7331a458dc54a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748408"
---
# <a name="loading-a-character"></a>Cargar un carácter

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Para animar un carácter, primero debe cargarlo. Use el [**método Load**](load-method.md) para cargar los datos del carácter. Microsoft Agent admite dos formatos para los datos de caracteres y animación: un único archivo estructurado y archivos independientes. Normalmente, se usa el formato de archivo único (. ACS) cuando los datos se almacenan localmente. Formato de varios archivos (. Acf. ACA) funciona mejor cuando desea descargar animaciones individualmente, como al acceder a animaciones desde un servidor HTTP.

Una aplicación cliente solo puede cargar una única instancia del mismo carácter. Cualquier intento de cargar el mismo carácter más de una vez producirá un error. Sin embargo, una aplicación puede tener varias instancias del mismo carácter cargadas proporcionando conexiones independientes a Microsoft Agent. Por ejemplo, una aplicación podría cargar el mismo carácter desde dos copias del control Microsoft Agent.

También puede definir sus propios caracteres para usarlos con Microsoft Agent. Puede usar cualquier herramienta de representación que prefiera para crear las imágenes, siempre que termine con Windows formato de mapa de bits. Para ensamblar y compilar imágenes de un carácter en animaciones para usarlas con Microsoft Agent, use el Editor de caracteres de Microsoft Agent. Esta herramienta permite definir las propiedades predeterminadas de un carácter, así como definir animaciones para el carácter. El Editor de caracteres de Microsoft Agent también permite seleccionar el formato de archivo adecuado al crear un carácter.

 

 




