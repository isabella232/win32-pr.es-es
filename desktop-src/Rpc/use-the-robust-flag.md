---
title: Uso de la marca /robust
description: Compile siempre archivos .idl mediante el modificador /robust.
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3d6a7c93cbd97e2c65cc83e6933b3204dddbcf2c0e088dfbc0d98bbdb6628d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010893"
---
# <a name="use-the-robust-flag"></a>Uso de la marca /robust

Compile siempre archivos .idl mediante [**el modificador /robust.**](/windows/desktop/Midl/-robust) El uso del modificador **/robust** genera información adicional que permite al motor de representación de datos de red ( RAID) realizar la comprobación de errores en tiempo de ejecución en argumentos correlacionados en matrices dinámicas, uniones y punteros de interfaz de entrada en aplicaciones COM y RPC. Si el software no se compila con esta marca, el software está tan expuesto a ataques que ningún esfuerzo en ninguna otra área puede protegerlo.

 

 