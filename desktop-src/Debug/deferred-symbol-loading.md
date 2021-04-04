---
description: Para ahorrar tiempo y memoria cuando se trabaja con muchos archivos de símbolos, utilice la función SymSetOptions para establecer la opción de carga de símbolos diferida ( \_ cargas diferidas de SYMOPT \_ ).
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: Carga de símbolos diferidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64d05a3ad7ad0fe4017f1ba6fa99625af33c2cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998060"
---
# <a name="deferred-symbol-loading"></a>Carga de símbolos diferidos

Para conservar el tiempo y la memoria cuando se trabaja con muchos archivos de símbolos, utilice la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) para establecer la opción de carga de símbolos diferida ( \_ cargas diferidas \_ de SYMOPT) y, a continuación, use la función [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) o [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) para cargar símbolos aplazados para todos los módulos. El controlador de símbolos mostrará los símbolos que están disponibles para los módulos, pero no asignará la información de depuración en memoria hasta que se solicite. Este es el método preferido para usar los símbolos de depuración de forma eficaz. Todas las funciones que utilizan símbolos se ven afectadas por la carga de símbolos diferidos.

 

 



