---
title: Valores altos de PPP para aplicaciones de escritorio en Windows 8.1
description: Valores altos de PPP para aplicaciones de escritorio en Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbef80ce11de41ca50b7cf5ce4076b294b9331b62be417686f7ba0a3a63b98dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852431"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a>Valores altos de PPP para aplicaciones de escritorio en Windows 8.1

## <a name="platforms"></a>Plataformas

<dl> Clientes: Windows 8.1  
Servidores: Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

En Windows 8.1 se espera que las aplicaciones de escritorio se ejecuten en pantallas con un escalado del 200 %, además del escalado del 100 %, el 125 % y el 150 % que se admite en Windows 8. Además, las aplicaciones de escritorio se escalan por monitor en lugar de a un único factor de escala aplicado a todas las pantallas. Los desarrolladores también pueden llamar a nuevas API en Windows 8.1 para obtener factores de escala por monitor.

## <a name="manifestations"></a>Manifestaciones

Los usuarios pueden usar nuevas pantallas de alta densidad Windows 8.1 una experiencia visual increíble que aproveche los datos de píxeles más altos. Si las aplicaciones no controlan valores altos de PPP, Windows los escalará para el usuario. Además, los usuarios pueden usar una combinación de pantallas de alta y baja densidad en el mismo equipo, y Windows escalará el contenido adecuadamente para cada pantalla. Se trata de una mejora con respecto a Windows 8, donde el contenido puede ser demasiado grande en algunas pantallas.

## <a name="mitigation"></a>Mitigación

Dado que Windows escalará aplicaciones que no se escalan por sí mismos, los desarrolladores generalmente no tienen que realizar trabajo adicional, pero los desarrolladores que invierten en escribir aplicaciones que admiten valores altos de PPP tendrán una ventaja competitiva, ya que esas aplicaciones se verán mejor en los nuevos portátiles con valores altos de PPP y monitores de escritorio.

## <a name="solution"></a>Solución

Crear una aplicación que pueda aprovechar los valores altos de PPP es una tarea compleja de diseño e implementación. Consulte los vínculos siguientes para obtener información del tutorial, crear contenido de presentación y compatibilidad similar.

## <a name="tests"></a>Pruebas

Aunque los desarrolladores no decidan hacer que sus aplicaciones aprovechen los valores altos de PPP, deben probar su aplicación con un escalado del 100 %, del 125 %, del 150 % y del 200 % para asegurarse de que la experiencia del usuario final sea satisfactoria y competitiva.

## <a name="resources"></a>Recursos

-   [Documento técnico y tutorial sobre valores altos de PPP en Windows 8.1](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [Windows de ejemplo de escritorio](https://www.microsoft.com/?ref=go)
-   [Sesión de interrupción de BUILD 2013 con valores altos de PPP en Windows 8.1](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 