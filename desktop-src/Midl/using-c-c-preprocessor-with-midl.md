---
title: Uso de C/C++-Preprocesador con MIDL
description: El compilador MIDL no preprocesa los archivos de origen.
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- MIDL del compilador MIDL, preprocesador de C
- MIDL del preprocesador de C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac3952a342b101f0366d2bce8810426e758c4aa5b32fa267e685bc6d658f034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382799"
---
# <a name="using-cc-preprocessor-with-midl"></a>Uso de C/C++-Preprocesador con MIDL

El compilador MIDL no preprocesa los archivos de origen. En su lugar, el compilador MIDL usa un preprocesador disponible para preparar el flujo de entrada para el análisis. De forma predeterminada, MIDL usa el preprocesador para el compilador de Microsoft C/C++ del mismo entorno de compilación que MIDL. El usuario puede indicar un preprocesador diferente que midL usará, si es necesario.

MIDL genera ejecuciones de preprocesador independientes para archivos IDL y ACF de nivel superior, y para cada archivo importado con la directiva de importación MIDL. El preprocesador **\# controla** directamente los archivos incluidos con la directiva include.

En los temas siguientes se describen varios aspectos de las interacciones del preprocesador MIDL:

-   [Requisitos de preprocesador de C para MIDL](c-preprocessor-requirements-for-midl.md)
-   [Comprobación de las opciones del preprocesador](verifying-preprocessor-options.md)
-   [Guardar la salida del preprocesador](saving-preprocessor-output.md)
-   [Trabajar con \# define en archivos IDL](dealing-with-defines-in-idl-files-2.md)

 

 




