---
title: Alta resolución de PPP para aplicaciones de escritorio en Windows 8.1
description: Alta resolución de PPP para aplicaciones de escritorio en Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6c223e9dc39cda9a109280926a5eb47a8fffcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704981"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a>Alta resolución de PPP para aplicaciones de escritorio en Windows 8.1

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8.1  
Servidores: Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

En Windows 8.1 se espera que las aplicaciones de escritorio se ejecuten en pantallas con un ajuste de escala del 200%, además de los 100%, 125% y el escalado de 150% que se admite en Windows 8. Además, las aplicaciones de escritorio se escalan por monitor en lugar de a un único factor de escala aplicado a todas las pantallas. Los desarrolladores también pueden llamar a nuevas API en Windows 8.1 para obtener los factores de escala de cada monitor.

## <a name="manifestations"></a>Manifestaciones

Los usuarios pueden usar nuevas pantallas de alta densidad con Windows 8.1 para disfrutar de una experiencia visual increíble que aprovecha los datos de píxeles más altos. Si las aplicaciones no controlan los PPP altos, Windows las escalará para el usuario. Además, los usuarios pueden usar una combinación de pantallas de densidad alta y baja en el mismo equipo, y Windows escalará el contenido de forma adecuada para cada pantalla. Se trata de una mejora respecto a Windows 8, donde el contenido puede ser demasiado grande en algunas pantallas.

## <a name="mitigation"></a>Mitigación

Puesto que Windows escalará las aplicaciones que no se escalan por sí mismas, los desarrolladores no suelen tener que realizar trabajo adicional, pero los desarrolladores que invierten en la escritura de aplicaciones que admiten un alto nivel de PPP tendrán una ventaja competitiva, ya que esas aplicaciones tendrán un aspecto mejor en los nuevos portátiles y monitores de escritorio altos de PPP.

## <a name="solution"></a>Solución

La realización de una aplicación que puede aprovechar las ventajas de los PPP altos es una tarea compleja de diseño e implementación. Vea los vínculos siguientes para obtener información del tutorial, compilar contenido de presentación y compatibilidad similar.

## <a name="tests"></a>Pruebas

Aunque los desarrolladores no decidan que sus aplicaciones aprovechen las ventajas de un alto nivel de PPP, deben probar su aplicación en 100%, 125%, 150% y el escalado de 200% para asegurarse de que la experiencia del usuario final es satisfactoria y competitiva.

## <a name="resources"></a>Recursos

-   [Notas del producto y tutorial sobre la alta resolución de PPP en Windows 8.1](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [Programas de ejemplo de escritorio de Windows](https://www.microsoft.com/?ref=go)
-   [Sesión de división de compilación 2013 en alta resolución de PPP en Windows 8.1](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 