---
title: Usar C/C++-preprocesador con MIDL
description: El compilador MIDL no procesa los archivos de código fuente.
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- 'MIDL del compilador de MIDL, C: preprocesador'
- MIDL del preprocesador C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5752bd64ee9a9b5fc26d586b5bc33c1a1fb96e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356994"
---
# <a name="using-cc-preprocessor-with-midl"></a>Usar C/C++-preprocesador con MIDL

El compilador MIDL no procesa los archivos de código fuente. En su lugar, el compilador MIDL usa un preprocesador disponible para preparar el flujo de entrada para el análisis. De forma predeterminada, MIDL utiliza el preprocesador para el compilador de C/C++ de Microsoft del mismo entorno de compilación que MIDL. El usuario puede indicar un preprocesador diferente que va a usar MIDL, si es necesario.

MIDL genera ejecuciones de preprocesador independientes para los archivos IDL y ACF de nivel superior, así como para cada archivo importado con la Directiva de importación de MIDL. El preprocesador controla directamente los archivos incluidos con la directiva **\# include** .

En los temas siguientes se describen diversos aspectos de las interacciones del preprocesador de MIDL:

-   [Requisitos del preprocesador de C para MIDL](c-preprocessor-requirements-for-midl.md)
-   [Comprobar las opciones del preprocesador](verifying-preprocessor-options.md)
-   [Guardar la salida del preprocesador](saving-preprocessor-output.md)
-   [Trabajar con \# definiciones en archivos IDL](dealing-with-defines-in-idl-files-2.md)

 

 




