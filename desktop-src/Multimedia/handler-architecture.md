---
title: Arquitectura de controlador
description: Arquitectura de controlador
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b02d0184d364ce438dc28f8219beea01c4868
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075824"
---
# <a name="handler-architecture"></a>Arquitectura de controlador

La función interna de un controlador de archivo o secuencia se define mediante el propio controlador. Para una aplicación, un controlador de archivos aparece normalmente como un módulo para leer y escribir archivos AVI. Del mismo modo, un controlador de flujo aparece como un módulo para leer y escribir un tipo específico de flujo de datos. La interfaz de flujo coherente hace que el origen y el destino de la secuencia no sean importantes para la aplicación que utiliza el controlador.

Un controlador de archivos proporciona acceso a un origen de datos que consta de uno o varios flujos de datos. Los controladores de archivos proporcionan normalmente acceso a archivos de disco que contienen uno o más flujos de datos, y las funciones internas del controlador de archivos leen y escriben los datos multimedia. Sin embargo, los controladores de archivo pueden trabajar con cualquier origen de datos, como un canal de transmisión digital que contiene varios flujos de datos mezclados.

En cambio, un controlador de flujo procesa un tipo de datos y aparece como un flujo de datos en una aplicación. Un controlador de flujo puede proporcionar datos que fabrica o puede recuperar datos de un archivo o de un origen externo. Proporciona sus datos en un formato que pueda usar la aplicación.

 

 




