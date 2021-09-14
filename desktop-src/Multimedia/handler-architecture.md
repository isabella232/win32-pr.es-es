---
title: Arquitectura del controlador
description: Arquitectura del controlador
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b02d0184d364ce438dc28f8219beea01c4868
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062910"
---
# <a name="handler-architecture"></a>Arquitectura del controlador

El propio controlador define la función interna de un controlador de archivos o secuencias. En una aplicación, un controlador de archivos suele aparecer como un módulo para leer y escribir archivos AVI. De forma similar, un controlador de flujo aparece como un módulo para leer y escribir un tipo específico de flujo de datos. La interfaz de flujo coherente hace que el origen y el destino de la secuencia no sean importantes para la aplicación que usa el controlador.

Un controlador de archivos proporciona acceso a un origen de datos que consta de uno o varios flujos de datos. Los controladores de archivos suelen proporcionar acceso a los archivos de disco que contienen uno o varios flujos de datos, y las funciones internas del controlador de archivos leen y escriben los datos multimedia. Sin embargo, los controladores de archivos pueden trabajar con cualquier origen de datos, como un canal de transmisión digital que contiene varios flujos de datos entremezados.

Por el contrario, un controlador de flujo procesa un tipo de datos y aparece como un flujo de datos a una aplicación. Un controlador de flujo puede proporcionar datos que fabrica, o puede recuperar datos de un archivo o un origen externo. Proporciona sus datos en un formato que la aplicación puede usar.

 

 




