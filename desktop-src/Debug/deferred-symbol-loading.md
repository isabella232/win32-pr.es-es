---
description: Para ahorrar tiempo y memoria al trabajar con muchos archivos de símbolos, use la función SymSetOptions para establecer la opción de carga diferida de símbolos (CARGAS \_ DIFERIDAS \_ DE SYMOPT).
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: Carga diferida de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8682de9ac8eaea78e037bf85ea8a17cd88e63bb56468ab39df3d1887fcc66801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957154"
---
# <a name="deferred-symbol-loading"></a>Carga diferida de símbolos

Para ahorrar tiempo y memoria al trabajar con muchos archivos de símbolos, use la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) para establecer la opción de carga diferida de símbolos (CARGAS DIFERIDAS DE SYMOPT) y, a continuación, use las funciones \_ \_ [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) o [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) para cargar símbolos diferidos para todos los módulos. El controlador de símbolos enumerará los símbolos que están disponibles para los módulos, pero no asignará la información de depuración a la memoria hasta que se solicite. Este es el método preferido para usar eficazmente símbolos de depuración. Todas las funciones que usan símbolos se ven afectadas por la carga diferida de símbolos.

 

 



