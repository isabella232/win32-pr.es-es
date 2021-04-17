---
description: Diferencias entre la e/s local y la e/s de red en Windows.
ms.assetid: 8a8f20bd-fa41-4f1a-b9bf-5f09683cd46c
title: Diferencias en la e/s local y de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30c4faf6b7358a1c7c134dccdeb12298309c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667703"
---
# <a name="differences-in-local-and-network-io"></a>Diferencias en la e/s local y de red

Hay algunas diferencias importantes entre la e/s local y la e/s de red en Windows:

-   La compatibilidad de e/s de red depende del redirector y del Protocolo de red.
-   El rendimiento de e/s de red depende del número de operaciones de e/s de red que se estén llevando a cabo y de la velocidad de la conexión de red. La aplicación debe ser capaz de controlar las operaciones de e/s de red con servidores que pueden ser mucho más rápidos o más lentos que el equipo local, así como cambios transitorios en la capacidad de la red. En estos casos, es posible que la aplicación necesite dejar más tiempo para que se complete la operación.
-   Las funciones que se usan para realizar la e/s de archivos locales pueden comportarse de forma diferente a través de la red. Por ejemplo, la operación de e/s de red que tarda mucho tiempo en completarse puede agotar el tiempo de espera. En algunas situaciones, es posible que los identificadores de archivo se queden abiertos de forma indefinida debido a esto. Otro ejemplo es que las funciones pueden devolver códigos de error de la aplicación para procesar que son específicos de la e/s de red.

 

 



