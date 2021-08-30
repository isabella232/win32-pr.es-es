---
title: Invocación del compilador de MIDL
description: El compilador midl puede generar código para distintas plataformas y versiones del sistema. Consulte el modificador /target para obtener más información sobre los modificadores sugeridos y cómo generar código optimizado para una versión determinada.
ms.assetid: 57730efa-71c3-4746-83f4-c7e327888efc
keywords:
- MIDL del compilador MIDL, invocar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013dec774729a3567d321ae1394fb50b17134564bce50349977a95d2c669717d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086385"
---
# <a name="invoking-the-midl-compiler"></a>Invocación del compilador de MIDL

El compilador midl puede generar código para distintas plataformas y versiones del sistema. Consulte el [**modificador /target**](-target.md) para obtener más información sobre los modificadores sugeridos y cómo generar código optimizado para una versión determinada.

Ejecute el compilador MIDL desde la línea de comandos con el siguiente comando:

**midl**  *<* **opciones** _>_ **filename.idl**

donde *<* representa las opciones de línea de comandos que desea usar y Filename.idl es el nombre del archivo MIDL que se _>_ va a compilar.

Hay disponible una lista completa de las opciones y los modificadores del compilador de MIDL cuando se usa el compilador de MIDL [**/help**](-help-.md) y /? Interruptores. Los modificadores se organizan por categorías. Para obtener más información, vea [midl Command-Line referencia](midl-command-line-reference.md).

> [!NOTE]
> La nueva marca global **$(MIDL \_ OPTIMIZATION)** existe en win32.mak. Cuando se compila un archivo .idl con esta marca, el código auxiliar generado puede usar las características rpc más recientes disponibles en la plataforma especificada y mejorar potencialmente el rendimiento y la estabilidad de la aplicación. Se recomienda que las aplicaciones usen esta marca al usar MIDL.
>
> **midl** **$(MIDL \_ OPTIMIZATION)** **...**