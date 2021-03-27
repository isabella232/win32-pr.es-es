---
title: Vinculación dinámica
description: A veces, los desarrolladores de gráficos crean sombreadores grandes y de uso general que se pueden usar en una amplia variedad de elementos de la escena.
ms.assetid: 2f5f7852-0f0a-4fad-a412-9a0d634c73b6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5cd10bab8e2b4a28458cad1050847e0184ce43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776398"
---
# <a name="dynamic-linking"></a>Vinculación dinámica

A veces, los desarrolladores de gráficos crean sombreadores grandes y de uso general que se pueden usar en una amplia variedad de elementos de la escena. En tiempo de ejecución, el sombreador ejecuta condicionalmente el código adecuado para la situación determinada. Desafortunadamente, estos grandes sombreadores de uso general usan registros de uso general (GPRs) de manera ineficaz y pueden ser mucho más lentos que los más pequeños y más específicos.

El modelo de sombreador 5 soluciona este problema de rendimiento al introducir la vinculación dinámica del sombreador. La vinculación dinámica separa los fragmentos de código del sombreador mediante el uso de interfaces y funciones virtuales y permite que la aplicación Seleccione el fragmento que se va a usar en el momento de la hora de dibujo. Esto mejora el rendimiento al enlazar solo el código del sombreador necesario y no todo el sombreador de uso general grande.

## <a name="in-this-section"></a>En esta sección



| Elemento                                                                                                                                                                                                                                                                                                                         | Descripción                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Almacenar variables y tipos para los sombreadores que se van a compartir](storing-variables-and-types-for-shaders-to-share.md)<br/> | Describe el objeto de vinculación de clases para almacenar variables y tipos que pueden compartir varios sombreadores.<br/> |
| <span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfaces y clases](overviews-direct3d-11-hlsl-dynamic-linking-class.md)<br/>                                                                                                         | Describe el uso de interfaces y clases HLSL para implementar la vinculación dinámica.<br/>                           |
| <span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Restricciones de uso de la interfaz](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)<br/>                                                                            | Describe las restricciones en el uso de interfaces en el código del sombreador.<br/>                                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[HLSL](overviews-direct3d-11-hlsl.md)
</dt> </dl>

 

 





