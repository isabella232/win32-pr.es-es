---
title: Algunos paneles de entrada del software IME de Asia Oriental ahora envían vKey
description: Algunos paneles de entrada del software IME de Asia Oriental ahora envían vKey
ms.assetid: 5E3BE112-D962-4C11-B31E-229584191FAE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c444091e4498582cccc4378dfa2f17216cbf810
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903908"
---
# <a name="some-east-asian-ime-software-input-panels-now-send-vkey"></a>Algunos paneles de entrada del software IME de Asia Oriental ahora envían vKey

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8.1  
Servidores: Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descripción

En Windows 8, si uno de los IME de Asia oriental está seleccionado, al presionar una tecla de panel de entrada de software no se envía vKeys.

En Windows 8.1, se envían vKeys para las siguientes configuraciones:



| Idioma            | IME                                 | Tienda Windows | Escritorio |
|---------------------|-------------------------------------|---------------|---------|
| Chino simplificado  | Microsoft pinyin, Microsoft Wubi    | Sí           | Sí     |
| Chino tradicional | Microsoft Changlie, Microsoft Quick | Sí           | Sí     |
| Chino tradicional | Microsoft Bopomofo                  | No            | No      |
| Coreano              | Microsoft IME                       | Sí           | No      |
| Japonés            | Microsoft IME                       | No            | No      |



 

## <a name="manifestations"></a>Manifestaciones

Si el usuario elige un IME que no envía vKeys, las funciones desencadenadas por vKey no funcionan.

## <a name="solution"></a>Solución

Las aplicaciones que no usan una de las configuraciones de IME anteriores deben diseñarse para que los usuarios puedan completar la tarea deseada sin usar funciones que requieran vKeys.

Si el usuario elige un IME que envía vKeys, pero la aplicación se diseñó sin esa expectativa, se debe cambiar la aplicación para reconocer qué versión de Windows se está ejecutando y responder según corresponda.

 

 




