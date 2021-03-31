---
title: Usar la marca/Robust
description: Compile siempre los archivos. idl mediante el modificador/Robust.
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db395841842331d9297a782fdcd8ea7573139f9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995394"
---
# <a name="use-the-robust-flag"></a>Usar la marca/Robust

Compile siempre los archivos. idl mediante el modificador [**/Robust**](/windows/desktop/Midl/-robust) . El uso del modificador **/Robust** genera información adicional que permite que el motor de representación de datos de la red (NDR) realice la comprobación de errores en tiempo de ejecución en argumentos correlacionados en matrices dinámicas, uniones y en punteros de interfaz out en aplicaciones com y RPC. Si el software no se puede compilar con esta marca, el software está tan expuesto a los ataques que ningún esfuerzo en otras áreas pueda proteger.

 

 