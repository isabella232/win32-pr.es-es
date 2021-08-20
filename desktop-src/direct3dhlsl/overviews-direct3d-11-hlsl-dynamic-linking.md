---
title: Vinculación dinámica
description: Los desarrolladores de gráficos a veces crean sombreadores grandes de uso general que pueden usar una amplia variedad de elementos de escena.
ms.assetid: 2f5f7852-0f0a-4fad-a412-9a0d634c73b6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cb445d657997d0ed4e3dbc7c550dc3af63640cbf8b54b17f4c918bdd6f554214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906652"
---
# <a name="dynamic-linking"></a>Vinculación dinámica

Los desarrolladores de gráficos a veces crean sombreadores grandes de uso general que pueden usar una amplia variedad de elementos de escena. En tiempo de ejecución, el sombreador ejecuta condicionalmente el código adecuado para la situación dada. Desafortunadamente, estos sombreadores grandes de uso general usan registros de uso general (GPR) de forma ineficaz y pueden ser mucho más lentos que los sombreadores más pequeños y más dirigidos.

El modelo de sombreador 5 soluciona este problema de rendimiento mediante la introducción de la vinculación dinámica del sombreador. La vinculación dinámica separa los fragmentos de código del sombreador mediante interfaces y funciones virtuales y permite a la aplicación seleccionar el fragmento que se usará en el momento del dibujo. Esto mejora el rendimiento al enlazar solo el código de sombreador necesario y no todo el sombreador grande de uso general.

## <a name="in-this-section"></a>En esta sección



| Elemento                                                                                                                                                                                                                                                                                                                         | Descripción                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Almacenar variables y tipos para que los sombreadores los compartan](storing-variables-and-types-for-shaders-to-share.md)<br/> | Describe el objeto de vinculación de clase para almacenar variables y tipos que pueden compartir varios sombreadores.<br/> |
| <span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfaces y clases](overviews-direct3d-11-hlsl-dynamic-linking-class.md)<br/>                                                                                                         | Describe el uso de interfaces y clases HLSL para implementar la vinculación dinámica.<br/>                           |
| <span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Restricciones de uso de la interfaz](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)<br/>                                                                            | Describe las restricciones en el uso de interfaces en el código del sombreador.<br/>                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[HLSL](overviews-direct3d-11-hlsl.md)
</dt> </dl>

 

 





