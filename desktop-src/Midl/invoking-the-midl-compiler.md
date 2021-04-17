---
title: Invocar el compilador MIDL
description: El compilador MIDL puede generar código para distintas plataformas y versiones del sistema. Consulte el modificador/Target para obtener más información acerca de los modificadores sugeridos y cómo generar código optimizado para una versión determinada.
ms.assetid: 57730efa-71c3-4746-83f4-c7e327888efc
keywords:
- MIDL del compilador MIDL, invocar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7e03abc49007b823f509acb35bd34ce6e47d80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/15/2019
ms.locfileid: "105651324"
---
# <a name="invoking-the-midl-compiler"></a>Invocar el compilador MIDL

El compilador MIDL puede generar código para distintas plataformas y versiones del sistema. Consulte el modificador [**/target**](-target.md) para obtener más información acerca de los modificadores sugeridos y cómo generar código optimizado para una versión determinada.

Ejecute el compilador MIDL desde la línea de comandos con el siguiente comando:

 *<  opciones >* de MIDL **filename. idl**

donde *< ***Options*** >* representa las opciones de línea de comandos que desea utilizar y FILENAME. idl es el nombre del archivo MIDL que se va a compilar.

Hay disponible una lista completa de las opciones y los modificadores del compilador MIDL cuando se usa el compilador de MIDL [**/Help**](-help-.md) y/? centrales. Los modificadores están organizados por categorías. Para obtener más información, vea la [referencia de Command-Line de MIDL](midl-command-line-reference.md).

> [!NOTE]
> La nueva marca global **$ (optimización de MIDL \_ )** existe en Win32. Mak. Cuando se compila un archivo. idl con esta marca, el código auxiliar generado puede utilizar las características de RPC más recientes disponibles en la plataforma especificada y, potencialmente, mejorar el rendimiento y la estabilidad de la aplicación. Se recomienda que las aplicaciones usen esta marca al usar MIDL.
>
> **MIDL** **$ (optimización de MIDL \_ )** **...**