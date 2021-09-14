---
title: Uso de la marca /robust
description: Compile siempre archivos .idl mediante el modificador /robust.
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db395841842331d9297a782fdcd8ea7573139f9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071375"
---
# <a name="use-the-robust-flag"></a>Uso de la marca /robust

Compile siempre archivos .idl mediante [**el modificador /robust.**](/windows/desktop/Midl/-robust) El uso del modificador **/robust** genera información adicional que permite al motor de representación de datos de red ( RAID) realizar la comprobación de errores en tiempo de ejecución en argumentos correlacionados en matrices dinámicas, uniones y punteros de interfaz de salida en aplicaciones COM y RPC. Si el software no se compila con esta marca, el software está tan expuesto a ataques que ningún esfuerzo en ninguna otra área puede protegerlo.

 

 